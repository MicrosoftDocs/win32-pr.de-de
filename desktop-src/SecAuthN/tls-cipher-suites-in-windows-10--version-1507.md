---
description: Erfahren Sie mehr über TLS-Verschlüsselungssammlungen in Windows 10 v1507. Verschlüsselungssammlungen können nur für TLS-Versionen ausgehandelt werden, die sie unterstützen.
ms.assetid: 58A47273-D2D3-449D-891C-C9502012C557
title: TLS-Verschlüsselungssammlungen in Windows 10 v1507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c974f03c1f7dbe8314820224b70f14ea7121b9
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262542"
---
# <a name="tls-cipher-suites-in-windows-10-v1507"></a>TLS-Verschlüsselungssammlungen in Windows 10 v1507

Verschlüsselungssammlungen können nur für TLS-Versionen ausgehandelt werden, die sie unterstützen. Die höchste unterstützte TLS-Version wird im TLS-Handshake immer bevorzugt. Beispielsweise kann SSL CK RC4 128 WITH MD5 nur verwendet werden, wenn sowohl der Client als auch der Server \_ \_ TLS \_ \_ \_ 1.2, 1.1 & 1.0 oder SSL 3.0 nicht unterstützen, da es nur mit SSL 2.0 unterstützt wird.

Die Verfügbarkeit von Verschlüsselungssammlungen sollte auf zwei Arten gesteuert werden:

-   Die Standardprioritäts reihenfolge wird überschrieben, wenn eine Prioritätsliste konfiguriert ist. Verschlüsselungssammlungen, die nicht in der Prioritätsliste enthalten sind, werden nicht verwendet.
-   Zulässig, wenn die Anwendung SCH USE STRONG CRYPTO besteht: Der \_ Microsoft \_ \_ Schannel-Anbieter filtert bekannte schwache Verschlüsselungssammlungen heraus, wenn die Anwendung das FLAG SCH \_ USE STRONG CRYPTO \_ \_ verwendet. In Windows 10 Version 1507 werden RC4-Verschlüsselungssammlungen herausgefiltert.

> [!IMPORTANT]
> HTTP/2-Webdienste führen bei nicht HTTP/2-kompatiblen Verschlüsselungssammlungen zu einem Fehler. Um sicherzustellen, dass Ihre Webdienste mit HTTP/2-Clients und -Browsern funktionieren, lesen Sie How to deploy custom cipher suite ordering (Bereitstellen einer [benutzerdefinierten Verschlüsselungssammlungsbestellung).](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

Die FIPS-Konformität wurde durch das Hinzufügen elliptischer Kurven komplexer, wodurch die Spalte fips mode enabled (FIPS-Modus aktiviert) in früheren Versionen dieser Tabelle irreführend wurde. Beispielsweise ist eine Verschlüsselungssammlung wie TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 nur FIPS-schwer, wenn elliptische NIST-Kurven verwendet werden. Informationen dazu, welche Kombinationen aus elliptischen Kurven und Verschlüsselungssammlungen im FIPS-Modus aktiviert werden, finden Sie in Abschnitt 3.3.1 der Richtlinien für die Auswahl, Konfiguration und Verwendung von [TLS-Implementierungen.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Für Windows 10 Version 1507 sind die folgenden Verschlüsselungssammlungen aktiviert und standardmäßig mithilfe des Microsoft Schannel-Anbieters in dieser Prioritäts reihenfolge:



| Verschlüsselungssammlungszeichenfolge                                                                                            | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                        | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                        | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                                        | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                        | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                           | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                           | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                      | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                      | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                                      | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                      | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                         | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                         | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ SHA<br/>                                                                       | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ MD5<br/>                                                                       | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA256 <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/>            | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/>               | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ MIT \_ MD5 <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/>            | Nein<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC MIT \_ \_ MD5 <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/> | Ja<br/>                      | SSL 2.0<br/>                            |



 

Die folgenden Verschlüsselungssammlungen werden vom Microsoft Schannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:



| Verschlüsselungssammlungszeichenfolge                                                                  | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen                     |
|--------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ RSA MIT DES \_ \_ \_ CBC \_ SHA<br/>                                             | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ MIT \_ RC4 \_ 56 \_ SHA<br/>                                  | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA<br/>                                 | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT \_ WITH \_ RC4 \_ 40 \_ MD5<br/>                                      | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA WITH NULL \_ \_ \_ MD5 Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/> | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ MIT DES \_ \_ CBC \_ SHA<br/>                                        | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA<br/>                            | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC MIT \_ \_ MD5<br/>                                          | Ja<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MIT \_ MD5<br/>                                    | Nein<br/>                       | SSL 2.0<br/>                            |



 

Um Verschlüsselungssammlungen hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:

-   Um Gruppenrichtlinien zu verwenden, konfigurieren Sie ssl cipher Suite Order unter Computerkonfiguration > Administrative Vorlagen > Netzwerk > SSL-Konfigurationseinstellungen mit der Prioritätsliste für alle Verschlüsselungssammlungen, die Sie aktivieren möchten.
-   Informationen zur Verwendung von PowerShell finden Sie unter [TLS-Cmdlets.](/powershell/module/tls/?view=win10-ps)

> [!Note]  
> Vor Windows 10 wurden Verschlüsselungssammlungszeichenfolgen mit der elliptischen Kurve angefügt, um die Kurvenpriorität zu bestimmen. Windows 10 unterstützt eine Prioritätsreihenfolgeeinstellung für elliptische Kurve, sodass das Suffix der elliptischen Kurve nicht erforderlich ist und von der neuen Prioritätsreihenfolge der elliptischen Kurve überschrieben wird, sofern angegeben, damit Organisationen gruppenrichtlinien verwenden können, um verschiedene Versionen von Windows mit denselben Verschlüsselungssammlungen zu konfigurieren.

 

> [!IMPORTANT]
> HTTP/2-Webdienste sind nicht mit benutzerdefinierten TLS-Verschlüsselungssammlungsaufträgen kompatibel. Weitere Informationen finden Sie unter [Bereitstellen von benutzerdefinierten Verschlüsselungssammlungsreihenfolge.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

 

 
