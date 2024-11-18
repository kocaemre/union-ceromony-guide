

# Union Ceromony

## Masaüstü Ortamını Kurun
Paket listesini güncelleyin ve XFCE masaüstü ortamını kurun:

```bash
sudo apt-get update
sudo apt install xfce4 xfce4-goodies -y
```

## xrdp'yi Kurun
xrdp'yi kurun:

```bash
sudo apt install xrdp -y
```

xrdp'yi otomatik başlatma için etkinleştirin ve başlatın:

```bash
sudo systemctl enable xrdp
sudo systemctl start xrdp
```

## xrdp'yi Xfce ile Yapılandırın
xrdp'yi Xfce oturumunu kullanacak şekilde ayarlayın:

```bash
echo "xfce4-session" >~/.xsession
```

## Güvenlik Duvarını Yapılandırın
RDP bağlantıları için 3389 portunu açın:

```bash
sudo ufw allow 3389/tcp
```

## Firefox Tarayıcısını RDP Bağlantısında Kullanın
Firefox'u yükleyin:

```bash
sudo apt install firefox -y
```

### RDP İstemcisi İndirin
Örneğin, Microsoft Remote Desktop'ı kullanabilirsiniz:

1. **Add** (Ekle) seçeneğine tıklayın.
2. **PCs** (Bilgisayarlar) seçeneğini seçin.
3. Sunucunuzun IP adresini **PC name** (Bilgisayar adı) olarak girin.
4. Yeni bir kullanıcı hesabı oluşturmak için **+** simgesine tıklayın.  
   - **Kullanıcı Adı**: `root`  
   - **Şifre**: Sunucunuzun şifresini girin.
5. Ayarları kaydedin ve bağlanın.

### Firefox'u Bulun
RDP ile bağlandıktan sonra Firefox'u şu şekilde bulun:

1. **Applications** (Uygulamalar) menüsüne tıklayın.
2. **Internet** (İnternet) veya **Web Tarayıcıları** kategorisini seçin ve Firefox simgesini bulun.
3. Firefox simgesine tıklayarak tarayıcıyı açın.
4. Menüde görünmüyorsa, terminali açın ve şu komutu çalıştırın:

```bash
firefox
```

## Katılın
1. [https://ceremony.union.build/](https://ceremony.union.build/) adresine gidin.
2. GitHub veya Google hesabınızla giriş yapın.
3. **Linux** seçeneğini seçin ve verilen kodu kopyalayın.

## VPS'ye Bağlanın ve Oturumu Hazırlayın
1. RDP aracılığıyla VPS'ye bağlanın ve oturumu kesmeden devam edin.
2. Bir screen oturumu başlatın:

```bash
apt install screen
screen -S unicr
```

3. Kopyalanan kodu yapıştırın. Docker kurulu değilse, bir hata mesajı ve kurulum talimatları görüntülenir. Bu talimatları izleyerek Docker'ı kurun ve kodu tekrar girin:
```bash
apt install docker.io
```
4. "Switch to browser" (Tarayıcıya geçin) mesajını gördüğünüzde, screen oturumunu ayırın:

```bash
Ctrl+A+D
```

## RDP'de Firefox ile Devam Edin
1. İşleme Firefox'ta devam edin.
2. Bir dosya indirildiğinde şu dizine kaydedin:

```plaintext
/root/Downloads
```

3. Keplr'dan Cosmos adresini sağlayarak işleme devam edin.
4. Törene katılın.

## Bağlantıyı Kes ve Yeniden Bağlan
1. Firefox'u kapatmayın. RDP oturumunu sağ üst köşeden **X** düğmesi ile kapatın.
2. Daha sonra tekrar bağlandığınızda, Firefox açık kalmış olacaktır.

İyi şanslar!

**cc:** Zeska
