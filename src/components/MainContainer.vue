<template>
  <div class="main-container">
    <div class="container">
      <div class="mini-banner-wrapper">
        <p>Gratis Ebook 9 Cara Cerdas Menggunakan Domain <a href="#">[ x ]</a></p>
        <div class="contacts">
          <span><i class="bi bi-telephone-fill"></i>0274-5305505</span>
          <span><i class="bi bi-chat-right-text"></i>Live Chat</span>
          <span><i class="bi bi-person-circle"></i>Member Area</span>
        </div>
      </div>
    </div>
    <div class="navbar-wrapper">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
          <a class="navbar-brand" href="#">
            <img :src="require('../assets/images/niagahoster-logo.png')" alt="logo" style="width: 200px !important" />
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#list-menu-items"
            aria-controls="list-menu-items" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="list-menu-items">
            <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Hosting</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Domain</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Server</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Website</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Afiliasi</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Promo</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Pembayaran</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Review</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Kontak</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Blog</a>
              </li>
            </ul>
          </div>
        </nav>
      </div>
    </div>

    <div class="highlights-products">
      <div class="container">
        <div class="row">
          <div class="col-sm">
            <div class="features">
              <div class="title">PHP Hosting</div>
              <div class="descriptions">Cepat, handal, penuh dengan <br />modul PHP yang anda butuhkan</div>
              <div class="products-values">
                <span><i class="bi bi-check-circle-fill"></i>Solusi PHP untuk performa query yang lebih cepat</span>
                <span><i class="bi bi-check-circle-fill"></i>Konsumsi memori yang lebih rendah.</span>
                <span><i class="bi bi-check-circle-fill"></i>Support PHP 5.3, PHP 5.4, PHP 5.5, PHP 5.6 dan PHP 7</span>
                <span><i class="bi bi-check-circle-fill"></i>Fitur Enkripsi IonCube dan Zend Guards Loaders </span>
              </div>
            </div>
          </div>
          <div class="col-sm">
            <div class="banner-right">
              <img style="height: 250px;" :src="require('../assets/svg/illustration banner PHP hosting-01.svg')" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="tools-manager">
        <div class="tools-item">
          <div class="tools-item-image">
            <embed :src="require('../assets/svg/zendguard.svg')" alt="zenguard" style="width: 200px !important" />
          </div>
          <div class="title">PHP Zend Guard Loader</div>
        </div>
        <div class="tools-item">
          <div class="tools-item-image">
            <embed :src="require('../assets/svg/icon-composer.svg')" alt="composer" style="width: 150px !important" />
          </div>
          <div class="title">PHP Composer</div>
        </div>
        <div class="tools-item">
          <div class="tools-item-image">
            <embed :src="require('../assets/svg/icon-php-hosting-ioncube.svg')" alt="ioncube" style="width: 200px !important" />
          </div>
          <div class="title">PHP ionCube Loader</div>
        </div>
      </div>
    </div>
    <div class="products-promo">
      <div class="promo-title">Paket Hosting Singapura Yang Tepat</div>
      <div class="promo-description"> Diskon 40% + Domain dan SSL Gratis untuk Anda</div>
    </div>
    <div class="pricing-list">
      <div class="container">
        <div class="row pricing-item">
          <div class="col-sm" v-for="(price, index) in priceLists.data" :key="index">
            <div class="row" v-bind:class="{active: price.is_best_seller}">
              <div class="col-12">
                <div class="packet-name">{{price.packet_name}}</div>
              </div>
              <div class="col-12">
                <div class="original-price">Rp {{price.original_price}}</div>
                <div class="discount-price">
                  <div class="currency">Rp </div>
                  <div class="thousand">{{Math.floor(price.discount_price/1000)}}</div>
                  <div class="hundreds">.{{(price.discount_price%1000)}}</div>  / bln
                </div>              
              </div>
              <div class="col-12">
                <div class="total-user">{{formatter(price.total_users)}} Pengguna Terdaftar</div>
              </div>
              <div class="col-12">
                <div class="descriptions">
                  <p v-for="(feature, indexFeature) in price.features" :key="indexFeature" 
                    v-bind:class="{'business-star': `${feature}`.startsWith('★')}">
                    {{feature}}
                  </p>
                </div>
                <div class="action">
                  <div class="btn btn-secondary btn-selected-packet">
                    Pilih Sekarang
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="benefits pages">
      <div class="container">
        <h3>Powerful dengan Limit PHP yang Lebih Besar</h3>
        <div class="row">
          <div class="col-sm-4">
            <div class="row">
              <div class="col-sm-2">
                <i class="bi bi-check-circle-fill"></i>
              </div>
              <div class="col-sm-8">
                max execution time 300s
              </div>
            </div>
            <div class="row">
              <div class="col-sm-2">
                <i class="bi bi-check-circle-fill"></i>
              </div>
              <div class="col-sm-8">
                max execution time 300s
              </div>
            </div>
            <div class="row">
              <div class="col-sm-2">
                <i class="bi bi-check-circle-fill"></i>
              </div>
              <div class="col-sm-8">
                php memory limit 1024
              </div>
            </div>
          </div>
          <div class="col-sm-4">
            <div class="row">
              <div class="col-sm-2">
                <i class="bi bi-check-circle-fill"></i>
              </div>
              <div class="col-sm-8">
                post max size 128 MB
              </div>
            </div>
            <div class="row">
              <div class="col-sm-2">
                <i class="bi bi-check-circle-fill"></i>
              </div>
              <div class="col-sm-8">
                upload max filesize 128MB
              </div>
            </div>
            <div class="row">
              <div class="col-sm-2">
                <i class="bi bi-check-circle-fill"></i>
              </div>
              <div class="col-sm-8">
                Max Input Vars 2500
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <span class="divided"></span>
    <div class="default-features pages">
      <div class="container">
        <h3>Semua Paket Hosting Sudah Termasuk</h3>
        <div class="row">
          <div class="col-sm">
            <embed :src="require('../assets/svg/icon PHP Hosting_PHP Semua Versi.svg')" />
            <b>PHP Semua Versi</b>
            <p>Pilih Semua dari versi PHP 5.3 s/d PHP 7. Ubah sesuka Anda</p>
          </div>
          <div class="col-sm">
            <embed :src="require('../assets/svg/icon PHP Hosting_My SQL.svg')" />
            <b>MySQL Versi 5.6</b>
            <p>Nikmati MySQL versi terbaru, tercepat dan kaya akan fitur</p>
          </div>
          <div class="col-sm">
            <embed :src="require('../assets/svg/icon PHP Hosting_CPanel.svg')" />
            <b>Panel Hosting cPanel</b>
            <p>Kelola website dengan panel canggih yang familiar di hati anda</p>
          </div>
        </div>
        <div class="row">
          <div class="col-sm">
            <embed :src="require('../assets/svg/icon PHP Hosting_garansi uptime.svg')" />
            <b>Garansi Uptime 99.9%</b>
            <p>Data center yang mendukung kelangsungan website Anda 24/7</p>
          </div>
          <div class="col-sm">
            <embed :src="require('../assets/svg/icon PHP Hosting_InnoDB.svg')" />
            <b>Database InnoDB Unlimited</b>
            <p>Jumlag dan ukuran database yang tumbuh sesuai kebutuhan anda</p>
          </div>
          <div class="col-sm">
            <embed :src="require('../assets/svg/icon PHP Hosting_My SQL remote.svg')" />
            <b>Wildcard Remote MySQL</b>
            <p>Mendukung s/d 25 max_user_connections dan 100 max_connections</p>
          </div>
        </div>
      </div>
    </div>
    <span class="divided"></span>
    <div class="pages">
      <div class="container">
        <h3>Mendukung Penuh Framework Laravel</h3>
        <div class="row">
          <div class="col-sm banner-left">
            <p class="banner-top-description">
              Tak Perlu menggunakan dedicated server ataupun VPS
              yang mahal. Layanan PHP hosting murah kami mendukung Penuh
              framework favorit anda
            </p>
            <div class="products-values">
              <span><i class="bi bi-check-circle-fill"></i>Install Laravel <b>1 klik</b> dengan Softacuous Installer</span>
              <span><i class="bi bi-check-circle-fill"></i>Mendukung ekstensi PHP MCrypt, phar, mbstring, json dan fileinfo</span>
              <span><i class="bi bi-check-circle-fill"></i>Tersedia Composer dan SSH untuk menginstall packages pilihan anda</span>
            </div>
            <small class="notes">Nb. Composer dan SSH hanya tersedia pada paket Personal dan Bisnis</small>
            <div class="action">
              <div class="btn btn-secondary btn-selected-packet">
                Pilih Hosting Anda
              </div>
            </div>
          </div>
          <div class="col-sm banner-right">
            <img height="300px" :src="require('../assets/svg/illustration banner support laravel hosting.svg')" />
          </div>
        </div>
      </div>
    </div>
    <div class="pages">
      <div class="container">
        <h3>Powerful dengan Limit PHP yang Lebih Besar</h3>
        <div class="libraries-installed">        
          <p class="break-text">IcePHP apc apcu apm ares bcmath bcompiler big_int bitset bloomy bz2_filter clamav coin_acceptor crack dba</p>
          <p class="break-text">http huffman idn igbinary imagick imap inclued inotify interbase intl ioncubeloader ioncubeloader_4 jsmin json Idap</p>
          <p class="break-text">nd_pdo_mys oauth oci8 odbc opcache pdf pdo pdo_dblib pdo_firebird pdo_mysql pdo_odbc pdo_pgsql pdo_sqlite pgsql phalcon</p>
          <p class="break-text">stats stem stomp suhosin sybase_ct sysvmsg sysysem sysyshm tidy timezonedb trader translit upload progress uri_template uuid</p>        
        </div>
        <div class="action button-center">
          <div class="btn btn-secondary btn-selected-packet">
            Selengkapnya
          </div>
        </div>
      </div>
    </div>
    <div class="highlights-products" style="padding-bottom: 0px;">
      <div class="container">
        <div class="row">
          <div class="col-sm">
            <div class="features banner-left">
              <div class="descriptions">Linux Hosting yang Stabil<br /> dengan Teknologi LVE</div>
              <p class="detail">SuperMicro <b>Intel Xeon 24-Cores</b> server dengan RAM <b>128 GB</b> dan teknologi <b>LVE CloudLinux</b> untuk stabilitas server Anda. Dilengkapi dengan <b>SSD</b> untuk kecepatan <b>MySQL</b> dan caching, Apache load balancer berbasis LiteSpeed Technologies, <b>CageFS</b> security, <b>Raid-10</b> protection dan auto backup untuk keamanan website PHP Anda.</p>
              <div class="action">
                <div class="btn btn-secondary btn-selected-packet">
                  Pilih Hosting Anda
                </div>
              </div>
            </div>
          </div>
          <div class="col-sm">
            <div class="banner-right">
              <img style="height: 300px;" :src="require('../assets/images/Image support.png')" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="pages share-content">
      <div class="container">
        <div class="row">
          <div class="col-sm">
            <p>Bagikan jika Anda Menyukai Halaman Ini</p>
          </div>
          <div class="col-sm">
            <div class="content-center">
              <img height="30px" :src="require('../assets/images/share-content.png')">
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="pages services-and-support">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-sm display-flex-row">
            <h2>Perlu <b>Bantuan?</b> Hubungi Kami: <b>0274-5305505</b></h2>
            <div class="separator"> </div>
            <div>
              <div class="btn btn-secondary btn-chat">
                <i class="bi bi-chat-left"></i>Live Chat
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-pages">
      <div class="container">
        <div class="row mt-5">
          <div class="col-sm">
            <p class="block-name"><b>HUBUNGI KAMI</b></p>
            <p>0274-5305505<br />Senin - Minggu<br /> 24 Jam Nonstop <br /><br />JI. Selokan Mataram Monjali<br /> Karangjati MT 1/304<br />Sinduadi, Mlati, Sleman<br />Yogyakarta 55284 </p>
          </div>
          <div class="col-sm">
            <p class="block-name"><b>LAYANAN</b></p>
            <p>Domain<br />Shared Hosting<br />Cloud VPS Hosting<br />Managed VPS Hosting<br />Web Builder<br />Keamanan SSL / HTTPS<br />Jasa Pembuatan Website<br />Program Affiliasi</p>
          </div>
          <div class="col-sm">
            <p class="block-name"><b>SERVICE HOSTING</b></p>
            <p>Hosting Murah<br />Hosting Indonesia<br />Hosting Singapura SG<br />Hosting PHP<br />Hosting Wordpress<br />Hosting Laravel</p>
          </div>
          <div class="col-sm">
            <p class="block-name"><b>TUTORIAL</b></p>
            <p>Knowledgebase<br />Blog<br />Cara Pembayaran</p>
          </div>
        </div>
        <div class="row mt-3">
          <div class="col-sm">
            <p class="block-name"><b>TENTANG KAMI</b></p>
            <p>Tim Niagahoster<br />Karir<br />Events<br />Penawaran & Promo Spesial<br />Kontak Kami </p>
          </div>
          <div class="col-sm">
            <p class="block-name"><b>KENAPA PILIH NIAGAHOSTER? </b></p>
            <p>Support Terbaik<br />Garansi Harga Termurah<br />Domain Gratis Selamanya<br />Datacenter Hosting Terbaik<br />Review Pelanggan</p>
          </div>
          <div class="col-sm">
            <p class="block-name"><b>NEWSLETTER</b></p>
            <div class="newsletter">
              <input class="form-control form-control-lg" type="text" placeholder="Email" aria-label="Email">
              <div class="btn btn-secondary btn-chat">
                Berlangganan
              </div>
              <small>Dapatkan promo dan konten menarik dari penyedia hosting terbaik anda</small>
            </div>
          </div>
          <div class="col-sm">
            <div class="btn radius-outline">
              <img :src="require('../assets/svg/facebook.svg')" height="27px" style="right: 8px;position: absolute;top: 10px;" />
            </div>
            <div class="btn radius-outline">
              <img :src="require('../assets/svg/twitter.svg')" height="27px" style="right: 8px;position: absolute;top: 10px;" />
            </div>
            <div class="btn radius-outline">
              <img :src="require('../assets/svg/google-plus.svg')" height="27px" style="right: 8px;position: absolute;top: 10px;" />
            </div>
          </div>
        </div>
        <div class="row mt-3">
          <div class="col-sm">
            <p class="block-name">PEMBAYARAN</p>
            <div class="payment-list__icon-wrapper">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/bca.svg" class="payment-list__icon img-fluid" loading="lazy" width="91" height="35" alt="Pembayaran via BCA">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/mandiri.svg" class="payment-list__icon img-fluid" loading="lazy" width="103" height="35" alt="Pembayaran via Mandiri">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/bni.svg" class="payment-list__icon img-fluid" loading="lazy" width="102" height="35" alt="Pembayaran via BNI">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/visa.svg" class="payment-list__icon img-fluid" loading="lazy" width="98" height="35" alt="Pembayaran via Visa">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/master.svg" class="payment-list__icon img-fluid" loading="lazy" width="98" height="35" alt="Pembayaran via Master Card">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/atm-bersama.svg" class="payment-list__icon img-fluid" loading="lazy" width="64" height="35" alt="Pembayaran via ATM Bersama">            
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/alto.svg" class="payment-list__icon img-fluid" loading="lazy" width="46" height="35" alt="Pembayaran via Alto">
              <img src="https://www.niagahoster.co.id/assets/images/2019/payment-gateway/bri.svg" class="payment-list__icon img-fluid" loading="lazy" width="127" height="35" alt="Pembayaran via BRI">
            </div>
          </div>
          <small style="color: #8e8e8e;">Aktivasi instan dengan e-Payment Hosting dan domain langsung aktif</small>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import priceLists from "../dummy-data/price-lists";
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => ({
    priceLists: priceLists
  }),
  methods: {
    formatter(value) {
      return (value.toLocaleString()).split(",").join(".");
    }
  },
  mounted() {
    console.log(priceLists)
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '../assets/css/custom-styles.css';
</style>
