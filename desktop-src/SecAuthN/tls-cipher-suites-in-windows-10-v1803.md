---
description: Erfahren Sie mehr über TLS-Verschlüsselungssammlungen in Windows 10 v1803. Verschlüsselungssammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen.
title: TLS-Verschlüsselungssammlungen in Windows 10 v1803
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 3656ae05209b040385b512bf738cc9d01e4a5af2a3c3b0319f40e4c10400f63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916149"
---
# <a name="tls-cipher-suites-in-windows-10-v1803"></a>TLS-Verschlüsselungssammlungen in Windows 10 v1803

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Verschlüsselungssammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen. Die höchste unterstützte TLS-Version wird immer im TLS-Handshake bevorzugt.

Die Verfügbarkeit von Verschlüsselungssammlungen sollte auf zwei Arten gesteuert werden:

-   Die Standardprioritätsreihenfolge wird überschrieben, wenn eine Prioritätsliste konfiguriert ist. Verschlüsselungssammlungen, die nicht in der Prioritätsliste enthalten sind, werden nicht verwendet.
-   Zulässig, wenn die Anwendung SCH \_ USE STRONG CRYPTO übergibt: Der Microsoft \_ \_ Schannel-Anbieter filtert bekannte schwache Verschlüsselungssammlungen heraus, wenn die Anwendung das FLAG SCH \_ USE STRONG CRYPTO \_ \_ verwendet. RC4-, DES-, Export- und NULL-Verschlüsselungssammlungen werden herausgefiltert.

> [!IMPORTANT]
> HTTP/2-Webdienste schlagen mit nicht HTTP/2-kompatiblen Verschlüsselungssammlungen fehl. Um sicherzustellen, dass Ihre Webdienste mit HTTP/2-Clients und -Browsern funktionieren, lesen Sie [Bereitstellen einer benutzerdefinierten Verschlüsselungssammlungsreihenfolge.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

Die FIPS-Konformität wurde komplexer, da die Spalte mit aktivierten FIPS-Modus in früheren Versionen dieser Tabelle durch das Hinzufügen von elliptischen Kurven irreführend wurde. Beispielsweise ist eine Verschlüsselungssammlung wie TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 nur FIPS-konform, wenn NIST-Elliptic Curves verwendet werden. Informationen dazu, welche Kombinationen aus elliptischen Kurven und Verschlüsselungssammlungen im FIPS-Modus aktiviert werden, finden Sie im Abschnitt 3.3.1 der [Richtlinien für die Auswahl, Konfiguration und Verwendung von TLS-Implementierungen.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Für Windows 10 Version 1803 sind die folgenden Verschlüsselungssammlungen aktiviert und verwenden standardmäßig den Microsoft Schannel-Anbieter in dieser Prioritätsreihenfolge:



| Verschlüsselungssammlungszeichenfolge                                                                                 | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                              | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                              | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                       | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                       | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                      | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA256 <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/> | Nein<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert.<br/>    | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Die folgenden Verschlüsselungssammlungen werden vom Microsoft Schannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:



| Verschlüsselungssammlungszeichenfolge                                                                               | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                               | Ja<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ SHA<br/>                                                          | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ MD5<br/>                                                          | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA MIT DES \_ \_ \_ CBC \_ SHA<br/>                                                          | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ MIT DES \_ \_ CBC \_ SHA<br/>                                                     | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ WITH DES \_ \_ CBC SHA No TLS \_ 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/>   | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA MIT NULL \_ \_ \_ MD5 <br/> Wird nur verwendet, wenn die Anwendung explizit anfordert. <br/> | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ MIT \_ RC4 \_ 56 \_ SHA<br/>                                               | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT \_ WITH \_ RC4 \_ 40 \_ MD5<br/>                                                   | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA<br/>                                              | Nein<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Die folgenden PSK-Verschlüsselungssammlungen sind mithilfe des Microsoft Schannel-Anbieters standardmäßig aktiviert und in dieser Prioritätsreihenfolge:



| Verschlüsselungssammlungszeichenfolge                              | Zulässig durch SCH \_ USE \_ STRONG \_ CRYPTO | TLS/SSL-Protokollversionen |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ MIT \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ MIT \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ MIT \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ MIT \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ MIT NULL \_ \_ SHA384<br/>          | Nein<br/>                       | TLS 1.2<br/>        |
| TLS \_ PSK \_ MIT NULL \_ \_ SHA256<br/>          | Nein<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Standardmäßig sind keine PSK-Verschlüsselungssammlungen aktiviert. Anwendungen müssen PSK nur mit SCH \_ USE \_ PRESHAREDKEY \_ anfordern. Weitere Informationen zu Schannel-Flags finden Sie unter [**SCHANNEL \_ CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Um Verschlüsselungssammlungen hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:

-   Um Gruppenrichtlinien zu verwenden, konfigurieren Sie ssl cipher Suite Order unter Computerkonfiguration > Administrative Vorlagen > Netzwerk > SSL-Konfiguration Einstellungen mit der Prioritätsliste für alle Verschlüsselungssammlungen, die Sie aktivieren möchten.
-   Informationen zur Verwendung von PowerShell finden Sie unter [TLS-Cmdlets.](/powershell/module/tls/?view=win10-ps)

> [!Note]  
> Vor Windows 10 wurden Verschlüsselungssammlungszeichenfolgen mit der elliptischen Kurve angefügt, um die Kurvenpriorität zu bestimmen. Windows 10 unterstützt eine Prioritätsreihenfolgeeinstellung für elliptische Kurven, sodass das Suffix der elliptischen Kurve nicht erforderlich ist und durch die neue Prioritätsreihenfolge der elliptischen Kurve überschrieben wird, wenn dies bereitgestellt wird, damit Organisationen gruppenrichtlinien verwenden können, um verschiedene Versionen von Windows mit denselben Verschlüsselungssammlungen zu konfigurieren.

 

 

 
