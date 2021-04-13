---
description: TLS-Verschlüsselungs Sammlungen in Windows 8.1
ms.assetid: 48A515C2-96D3-4CBF-A48F-3F0B91F0CB2C
title: TLS-Verschlüsselungs Sammlungen in Windows 8.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14580b70168fd032005e7fa6bc418f1eff9e9593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484294"
---
# <a name="tls-cipher-suites-in-windows-81"></a>TLS-Verschlüsselungs Sammlungen in Windows 8.1

Verschlüsselungs Sammlungen können nur für TLS-Versionen ausgehandelt werden, die diese unterstützen. Die höchste unterstützte TLS-Version wird beim TLS-Handshake immer bevorzugt. Beispielsweise kann SSL \_ CK \_ RC4 \_ 128 \_ mit \_ MD5 nur verwendet werden, wenn sowohl der Client als auch der Server TLS 1,2, 1,1 & 1,0 oder SSL 3,0 nicht unterstützen, da es nur mit SSL 2,0 unterstützt wird.

Die Verfügbarkeit von Verschlüsselungs Sammlungen sollte auf eine von zwei Arten gesteuert werden:

-   Die Standard Prioritäts Reihenfolge wird überschrieben, wenn eine Prioritäts Liste konfiguriert wird. Verschlüsselungs Sammlungen, die nicht in der Prioritäts Liste enthalten sind, werden nicht verwendet.
-   Zulässig, wenn die Anwendung \_ Sch \_ \_ die starke kryptografieverschlüsselung verwendet: der Microsoft SChannel-Anbieter filtert bekannte schwache Verschlüsselungs Sammlungen heraus, wenn die Anwendung das Sch-fähige \_ \_ \_ kryptografieflag verwendet. In Windows 8.1 werden RC4-Verschlüsselungs Sammlungen herausgefiltert.

> [!IMPORTANT]
> HTTP/2-Webdienste schlagen mit nicht-http/2-kompatiblen Verschlüsselungs Sammlungen fehl. Informationen zum sicherstellen, dass Ihre Webdienste mit http/2-Clients und-Browsern funktionieren, finden Sie unter Bereitstellen einer [benutzerdefinierten Chiffre Sammlungs Bestellung](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

Die Kompatibilität mit der Kompatibilität mit der Funktion "PPS-Konformität" ist komplexer geworden, und es werden elliptische Kurven hinzugefügt Beispielsweise ist eine Verschlüsselungs Sammlung, z. b. TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256, nur FIPS-Beschwerde, wenn NIST-elliptische Kurven verwendet werden. Informationen dazu, welche Kombinationen aus elliptischen Kurven und Verschlüsselungs Sammlungen im FIPS-Modus aktiviert werden, finden Sie im Abschnitt 3.3.1 von [Richtlinien für die Auswahl, Konfiguration und Verwendung von TLS-Implementierungen]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Windows 8.1 und Windows Server 2012 R2 werden aktualisiert, Windows Update indem das [Update 2919355](https://support.microsoft.com/kb/2919355) angewendet wird, mit dem die neuen Verschlüsselungs Sammlungen hinzugefügt werden und die Prioritäts Reihenfolge geändert wird. Die folgenden Verschlüsselungs Sammlungen werden standardmäßig vom Microsoft SChannel-Anbieter aktiviert und in dieser Reihenfolge in der Priorität aufgeführt:



| Chiffre Sammlungs Zeichenfolge                                                                                            | Zugelassen von Sch \_ verwenden \_ starker \_ Kryptografie | TLS/SSL-Protokoll Versionen                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                     | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                     | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>                                                     | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>                                                     | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ with \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ with \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                   | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                   | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>                                                   | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>                                                   | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                                 | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                            | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ RC4 \_ 128 \_ SHA<br/>                                                                       | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ RC4 \_ 128 \_ MD5<br/>                                                                       | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit NULL- \_ \_ SHA256 <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird.<br/>            | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS- \_ RSA \_ mit NULL- \_ \_ SHA <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird.<br/>               | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ mit \_ MD5 <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird.<br/>            | Nein<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ mit \_ MD5 <br/> Wird nur verwendet, wenn explizit von der Anwendung angefordert wird.<br/> | Ja<br/>                      | SSL 2.0<br/>                            |



 

Die folgenden Verschlüsselungs Sammlungen werden vom Microsoft SChannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:



| Chiffre Sammlungs Zeichenfolge                                             | Zugelassen von Sch \_ verwenden \_ starker \_ Kryptografie | TLS/SSL-Protokoll Versionen                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>      | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>      | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Ja<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>    | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>    | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS- \_ RSA \_ mit \_ des \_ CBC \_ SHA<br/>                        | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA- \_ EXPORT1024 \_ mit \_ RC4 \_ 56 \_ SHA<br/>             | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA- \_ EXPORT1024 \_ mit \_ des \_ CBC \_ SHA<br/>            | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA- \_ Export \_ mit \_ RC4 \_ 40 \_ MD5<br/>                 | Nein<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ NULL \_ MD5<br/>                            | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ mit \_ des \_ CBC \_ SHA<br/>                   | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ EXPORT1024 \_ mit \_ des \_ CBC \_ SHA<br/>       | Ja<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ des \_ 64 \_ CBC \_ mit \_ MD5<br/>                     | Ja<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ mit \_ MD5<br/>               | Nein<br/>                       | SSL 2.0<br/>                            |



 

Um Verschlüsselungs Sammlungen hinzuzufügen, verwenden Sie die Gruppenrichtlinien Einstellung SSL-Verschlüsselungs Sammlungs Reihe unter Computer Konfiguration > administrative Vorlagen > Netzwerk > SSL-Konfigurationseinstellungen, um eine Prioritäts Liste für alle Verschlüsselungs Sammlungen zu konfigurieren, die aktiviert werden sollen.

 

 




