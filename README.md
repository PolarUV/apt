### Add repo key

```bash
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://polaruv.github.io/apt/pubkey.asc | sudo tee /etc/apt/keyrings/polaruv.asc >/dev/null
```

### Add repo

| :warning: WARNING                                      |
|:-------------------------------------------------------|
| Do not forget to change __\<distro>__ to your actual distro |

| Distro       | codename |
|:-------------|:---------|
| Ubuntu 22.04 | jammy    |
| Ubuntu 24.04 | noble    |
| Ubuntu 26.04 | resolute |
| debian 12    | bookworm |
| debian 13    | trixie   |

```bash
echo "deb [signed-by=/etc/apt/keyrings/polaruv.asc] https://polaruv.github.io/apt/ <distro> main" | sudo tee /etc/apt/sources.list.d/polaruv.list
```


### install
for polaruv
```bash
sudo apt update && sudo apt install polaruv
```

for client
```bash
sudo apt update && sudo apt install puv-client
```