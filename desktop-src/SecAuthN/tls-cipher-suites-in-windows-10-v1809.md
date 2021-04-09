---
description: Verschlüsselungs Sammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen. Die höchste unterstützte TLS-Version wird beim TLS-Handshake immer bevorzugt.
title: TLS-Verschlüsselungs Sammlungen in Windows 10 v1809
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 4b39e99dd97ee9f0faa7c69354f7bd977b42a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867451"
---
# <a name="tls-cipher-suites-in-windows-10-v1809"></a>TLS-Verschlüsselungs Sammlungen in Windows 10 v1809

Verschlüsselungs Sammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen. Die höchste unterstützte TLS-Version wird beim TLS-Handshake immer bevorzugt.

Die Verfügbarkeit von Verschlüsselungs Sammlungen sollte auf eine von zwei Arten gesteuert werden:

-   Die Standard Prioritäts Reihenfolge wird überschrieben, wenn eine Prioritäts Liste konfiguriert wird. Verschlüsselungs Sammlungen, die nicht in der Prioritäts Liste enthalten sind, werden nicht verwendet.
-   Zulässig, wenn die Anwendung Sch \_ die \_ starke \_ kryptografieverschlüsselung verwendet: der Microsoft SChannel-Anbieter filtert bekannte schwache Verschlüsselungs Sammlungen heraus, wenn die Anwendung das Sch-Flag für die starke Verschlüsselung verwendet \_ \_ \_ . RC4-, des-, Export-und NULL-Verschlüsselungs Sammlungen werden herausgefiltert.

> [!IMPORTANT]
> HTTP/2-Webdienste schlagen mit nicht-http/2-kompatiblen Verschlüsselungs Sammlungen fehl. Informationen zum sicherstellen, dass Ihre Webdienste mit http/2-Clients und-Browsern funktionieren, finden Sie unter Bereitstellen einer [benutzerdefinierten Chiffre Sammlungs Bestellung](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

Die Kompatibilität mit der Kompatibilität mit der Funktion "PPS-Konformität" ist komplexer geworden, und es werden elliptische Kurven hinzugefügt Beispielsweise ist eine Verschlüsselungs Sammlung, z. b. TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256, nur FIPS-Beschwerde, wenn NIST-elliptische Kurven verwendet werden. Informationen dazu, welche Kombinationen aus elliptischen Kurven und Verschlüsselungs Sammlungen im FIPS-Modus aktiviert werden, finden Sie im Abschnitt 3.3.1 von [Richtlinien für die Auswahl, Konfiguration und Verwendung von TLS-Implementierungen]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Für Windows 10, Version 1809, sind die folgenden Verschlüsselungs Sammlungen aktiviert, und in dieser Prioritäts Reihenfolge wird standardmäßig der Microsoft SChannel-Anbieter verwendet:



| Chiffre Sammlungs Zeichenfolge                                                                                 | Zugelassen von Sch \_ verwenden \_ starker \_ Kryptografie | TLS/SSL-Protokoll Versionen                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ with \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ with \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                              | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                              | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                       | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                       | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                      | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS- \_ RSA \_ mit NULL- \_ \_ SHA256 <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird.<br/> | Nein<br/>                       | TLS 1.2<br/>                            |
| TLS- \_ RSA \_ mit NULL- \_ \_ SHA <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird.<br/>    | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Die folgenden Verschlüsselungs Sammlungen werden vom Microsoft SChannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:



| Chiffre Sammlungs Zeichenfolge                                                                               | Zugelassen von Sch \_ verwenden \_ starker \_ Kryptografie | TLS/SSL-Protokoll Versionen                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ dhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                               | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ RC4 \_ 128 \_ SHA<br/>                                                          | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ RC4 \_ 128 \_ MD5<br/>                                                          | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ des \_ CBC \_ SHA<br/>                                                          | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ mit \_ des \_ CBC \_ SHA<br/>                                                     | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ EXPORT1024 \_ mit \_ des \_ CBC \_ SHA No TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/>   | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ NULL \_ MD5 <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird. <br/> | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA- \_ EXPORT1024 \_ mit \_ RC4 \_ 56 \_ SHA<br/>                                               | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA- \_ Export \_ mit \_ RC4 \_ 40 \_ MD5<br/>                                                   | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA- \_ EXPORT1024 \_ mit \_ des \_ CBC \_ SHA<br/>                                              | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Die folgenden PSK-Verschlüsselungs Sammlungen sind aktiviert, und in dieser Prioritäts Reihenfolge wird standardmäßig der Microsoft SChannel-Anbieter verwendet:



| Chiffre Sammlungs Zeichenfolge                              | Zugelassen von Sch \_ verwenden \_ starker \_ Kryptografie | TLS/SSL-Protokoll Versionen |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ mit \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ mit \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ mit \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Ja<br/>                      | TLS 1.2<br/>        |
| TLS- \_ PSK \_ mit \_ NULL- \_ SHA384<br/>          | Nein<br/>                       | TLS 1.2<br/>        |
| TLS- \_ PSK \_ mit \_ NULL- \_ SHA256<br/>          | Nein<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Standardmäßig sind keine PSK-Verschlüsselungs Sammlungen aktiviert. Anwendungen müssen PSK mithilfe von Sch anfordern \_ . verwenden Sie \_ nur PresharedKey \_ . Weitere Informationen zu SChannel-Flags finden Sie unter [**SChannel | \_ d**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Um Verschlüsselungs Sammlungen hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:

-   Um die Gruppenrichtlinie zu verwenden, konfigurieren Sie die Reihenfolge der SSL-Verschlüsselungs Sammlung unter Computer Konfiguration > administrative Vorlagen > Netzwerk > SSL-Konfigurationseinstellungen mit der Prioritäts Liste für alle Verschlüsselungs Sammlungen, die Sie aktivieren möchten.
-   Informationen zur Verwendung von PowerShell finden Sie unter [TLS-Cmdlets](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Vor Windows 10 wurden Chiffre Sammlungs Zeichenfolgen mit der elliptischen Kurve angehängt, um die Kurven Priorität zu bestimmen. Windows 10 unterstützt eine Einstellung für die Prioritäts Reihenfolge der elliptischen Kurven, damit das elliptische Kurven Suffix nicht erforderlich ist und von der neuen Priorität der elliptischen Kurven Priorität außer Kraft gesetzt wird, um Organisationen die Verwendung von Gruppenrichtlinien zum Konfigurieren verschiedener Versionen von Windows mit denselben Verschlüsselungs Sammlungen zu ermöglichen.

 

 

 
