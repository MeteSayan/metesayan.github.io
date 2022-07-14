---
layout: post
title: Neden Lambda servisleri tercih ediliyor?
date: 2017-09-12 13:32:20 +0300
description: Lambda servislerinin ne işe yaradığından ve neden tercih edildiğinden bahsedeceğim.
img: lambda-icon.jpg 
fig-caption: 
tags: [Lambda, AWS, Serverless]
---

## Serverless
Serverless konsepti bütün dünyada yükselen bir trend olarak dikkat çekmektedir. Servis sağlayıcılarının, sizi herhangi bir sunucu yapılandırması ile uğraştırmadan kod yazabilmenizi sağlayan bir yapıdır. Bu sayede test ettiğiniz kodlarınızı hızlıca prod ortama geçirebilmenizi sağlamaktadır. Ayrıca kullandığın kadar öde politikası sayesinde gereksiz maliyetlerinde önüne geçilmektedir.

Serverless yapıda yazdığınız her endpoint birbirinden bağımsız çalışır. Yani her servisi bir fonksiyon olarak düşünebilirsiniz. Bir serviste yapmış olduğunuz hata diğer servislerin çalışmasını engellemez veya bütün servislerin down olmasına sebep olamaz. Her servis ayrı şekilde çalışır ve işlemini tamamlayıp kendini kapatır. Bu sayede hatalı servisi bulması ve diğer servislerin işlevlerine devam edebilmesi daha kolay bir hal alır.  
<hr />

## Lambda Servisi
Lambda servisi ise AWS'nin sağladığı serverless yapıdır. Lambda servisinin gücü diğer AWS servisleri ile ortak çalışabilmesinden ve iyi bir dokümantasyona sahip olmasından geliyor.

Lambda servisinin sunduğu özelliklerin birkaçından bahsedecek olursak.

* AWS SAM CLI ile hızlıca template indirip ilk servisinizi yazabilirsiniz. template.yaml dosyası içerisinde yapacağınız konfigürasyonlardan sonra sizin için herşeyi AWS yapacaktır (Başka bir yazımda detaylı anlatacağım).
* Yazdığınız back end servislerini AWS API Gateway üzerinden veya ELB (Elastic Load Balancing) ile çalıştırabilirsiniz.
* Yazdığınız kodların loglarına Amazon CloudWatch üzerinden istediğiniz zaman ulaşabilirsiniz. AWS sizin için otomatik olarak bu loglamayı yapmakta ve log takibini çok kolaylaştırmaktadır.
* S3 servisi üzerindeki dosyalarda rahatlıkla ve hızlı bir şekilde işlem yapılabilmekte.
* Cron servisler tanımlayarak rapor gönderme gibi belli aralıklarla sürekli yapılması gereken işlemler yapılabilmektedir.
* Dynamodb üzerinden işlemler yapılabilmekte.
* Güvenlik için detaylı konfigurasyon yapılabilmekte.

<hr />

## Lambda Servisinin Desteklediği Diller
Lambda birçok popüler dili desteklemektedir. Lambda, runtime yapısı ile farklı dillerin kullanılabilmesini sağlıyor. Bu diller:

* .Net 6 (C#/PowerShell)
* .Net Core 3.1 (C#/PowerShell)
* Go 1.x
* Java 11 (Corretto)
* Node.js 16.x
* Python 3.9
* Ruby 2.7

Ayrıca bu diller için bazı eski versiyonlarada destek vermeye devam etmektedir. Bu versiyonlar:

* Java 8 on Amazon Linux 1
* Java 8 on Amazon Linux 2
* Node.js 12.x
* Node.js 14.x
* Python 3.6
* Python 3.7
* Python 3.8

![Lambda Languages]({{site.baseurl}}/assets/img/lambda-languages.jpg)

