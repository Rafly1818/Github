## How To FIX `error: failed to push some ref to [remote repo]`

*Untuk mengatasi masalah ini, jalankan perintah git pull pada repositori lokal Anda. Hal ini seharusnya memungkinkan Anda untuk melakukan push ke origin lagi.*

```git
git pull origin [branch]
git push origin [branch]
```
___
*Jika Anda mendapatkan kesalahan master (non-fast-forward) dengan pesan error "failed to push some refs to", ini berarti pointer ref telah dipindahkan maju dalam commit history. Namun, jika kode Anda bercabang sebelum mencapai commit terbaru, hal ini dapat menyebabkan masalah non-fast-forward dan menyebabkan kesalahan "failed to push some refs to".*

*Untuk mengatasi masalah ini, Anda dapat melakukan pull dengan menggunakan opsi `--rebase`. `--rebase` akan memungkinkan Anda untuk memindahkan file yang dimaksud ke commit terbaru dari kode yang Anda tarik.*

```
git pull --rebase origin [branch]
git push -u origin [branch]
```
___

> :warning: **Warning:** Menggunakan `--force` untuk mencoba memperbaiki kesalahan "failed to push some refs to" hanya akan menghasilkan lebih banyak kesalahan dalam jangka panjang. Ini terjadi karena `--force` menggunakan metode kekerasan yang menjadikan kode Anda saat ini dan ref head-nya sebagai sumber kebenaran.

<br>

> :memo: **Note:** Akibatnya, perubahan di remote dapat ditimpa oleh apa yang telah Anda dorong, menghapus fitur atau pembaruan yang mungkin telah dikomit oleh pengembang lain.

<br>

> :bulb: **Tip:** Hanya gunakan `--force` jika Anda nyaman dengan fitur yang tidak ada di lokal Anda akan ditimpa dengan apa yang Anda miliki saat ini. Gunakan opsi `--force` jika Anda yakin bahwa repositori lokal Anda dalam keadaan yang benar saat ini.

---

<h3 align="left">Socials</h3>
<p align="center"> 
  <a href="https://www.github.com/Rafly1818" target="_blank" rel="noreferrer"> 
    <picture> 
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github-dark.svg" /> 
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github.svg" /> 
      <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github.svg" width="32" height="32" alt="GitHub" /> 
    </picture> 
  </a> 
  <a href="http://www.instagram.com/flyyr_" target="_blank" rel="noreferrer"> 
    <picture> 
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/instagram-dark.svg" /> 
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/instagram.svg" /> 
      <img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/instagram.svg" width="32" height="32" alt="Instagram" /> 
    </picture> 
  </a>
</p>