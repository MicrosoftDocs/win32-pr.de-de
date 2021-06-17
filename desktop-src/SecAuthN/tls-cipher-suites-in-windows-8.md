---
description: Erfahren Sie mehr über TLS-Verschlüsselungssammlungen in Windows 8. Verschlüsselungssammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen.
ms.assetid: F37C3596-E273-4144-87B9-D589EBB82C0B
title: TLS-Verschlüsselungssammlungen in Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a204fabb91ddafc6b4d55c10b58503b4b81ca45
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262352"
---
# <a name="tls-cipher-suites-in-windows-8"></a>TLS-Verschlüsselungssammlungen in Windows 8

Verschlüsselungssammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen. Die höchste unterstützte TLS-Version wird immer im TLS-Handshake bevorzugt. BEISPIELSWEISE kann SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5 nur verwendet werden, wenn sowohl der Client als auch der Server TLS 1.2, 1.1 & 1.0 oder SSL 3.0 nicht unterstützen, da es nur mit SSL 2.0 unterstützt wird.

Die Verfügbarkeit von Verschlüsselungssammlungen sollte auf zwei Arten gesteuert werden:

-   Die Standardprioritätsreihenfolge wird überschrieben, wenn eine Prioritätsliste konfiguriert ist. Verschlüsselungssammlungen, die nicht in der Prioritätsliste enthalten sind, werden nicht verwendet.
-   Zulässig, wenn die Anwendung SCH \_ USE STRONG CRYPTO übergibt: Der Microsoft \_ \_ Schannel-Anbieter filtert bekannte schwache Verschlüsselungssammlungen heraus, wenn die Anwendung das FLAG SCH \_ USE STRONG CRYPTO \_ \_ verwendet. In Windows 8 werden RC4-Verschlüsselungssammlungen herausgefiltert.

> [!IMPORTANT]
> HTTP/2-Webdienste schlagen mit nicht HTTP/2-kompatiblen Verschlüsselungssammlungen fehl. Um sicherzustellen, dass Ihre Webdienste mit HTTP/2-Clients und -Browsern funktionieren, lesen Sie [Bereitstellen einer benutzerdefinierten Verschlüsselungssammlungsreihenfolge.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

Die FIPS-Konformität wurde komplexer, da die Spalte mit aktivierten FIPS-Modus in früheren Versionen dieser Tabelle durch das Hinzufügen von elliptischen Kurven irreführend wurde. Beispielsweise ist eine Verschlüsselungssammlung wie TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 nur FIPS-konform, wenn NIST-Elliptic Curves verwendet werden. Informationen dazu, welche Kombinationen aus elliptischen Kurven und Verschlüsselungssammlungen im FIPS-Modus aktiviert werden, finden Sie im Abschnitt 3.3.1 der [Richtlinien für die Auswahl, Konfiguration und Verwendung von TLS-Implementierungen.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Windows 7, Windows 8 und Windows Server 2012 werden vom Windows Update durch das Update 3042058 aktualisiert, das die Prioritätsreihenfolge ändert. Weitere Informationen finden Sie in der [Microsoft-Sicherheitsempfehlung 3042058.](/security-updates/SecurityAdvisories/2015/3042058) Die folgenden Verschlüsselungssammlungen werden vom Microsoft Schannel-Anbieter standardmäßig in dieser Prioritätsreihenfolge aktiviert:



| Verschlüsselungssammlungszeichenfolge                                                                                            | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>                                                     | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>                                                     | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>                                                     | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>                                                     | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>                                                   | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>                                                   | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>                                                   | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>                                                   | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ SHA<br/>                                                                       | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ MD5<br/>                                                                       | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA256 <br/> Wird nur verwendet, wenn die Anwendung explizit anforderungen.<br/>            | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA <br/> Wird nur verwendet, wenn die Anwendung explizit anforderungen.<br/>               | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ MIT \_ MD5 <br/> Wird nur verwendet, wenn die Anwendung explizit anforderungen.<br/>            | Nein<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC MIT \_ \_ MD5 <br/> Wird nur verwendet, wenn die Anwendung explizit anforderungen.<br/> | Ja<br/>                      | SSL 2.0<br/>                            |



 

Die folgenden Verschlüsselungssammlungen werden vom Microsoft Schannel-Anbieter unterstützt, aber standardmäßig nicht aktiviert:



| Verschlüsselungssammlungszeichenfolge                                             | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>      | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>      | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>    | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>    | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA MIT DES \_ \_ \_ CBC \_ SHA<br/>                        | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ MIT \_ RC4 \_ 56 \_ SHA<br/>             | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA<br/>            | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT \_ WITH \_ RC4 \_ 40 \_ MD5<br/>                 | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA MIT NULL \_ \_ \_ MD5<br/>                            | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ MIT DES \_ \_ CBC \_ SHA<br/>                   | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA<br/>       | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC MIT \_ \_ MD5<br/>                     | Ja<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MIT \_ MD5<br/>               | Nein<br/>                       | SSL 2.0<br/>                            |



 

Verwenden Sie zum Hinzufügen von Verschlüsselungssammlungen die Gruppenrichtlinieneinstellung SSL Cipher Suite Order unter Computer configuration > Administrative Vorlagen > Network > SSL Configuration Settings (Computerkonfiguration > SSL-Konfigurationseinstellungen), um eine Prioritätsliste für alle Verschlüsselungssammlungen zu konfigurieren, die Sie aktivieren möchten.

 

 
