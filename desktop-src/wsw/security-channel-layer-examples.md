---
title: Beispiele für Die Sicherheitskanalebene
description: Die folgenden Beispiele veranschaulichen die Sicherheit in der Kanalebene.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- Sicherheitsbeispiele
- Sicherheitsbeispiele, Setup
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d130bc7e0e4250107c6e331a43f7d5a13786929c37bd998177ee587c2f29049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192771"
---
# <a name="security-channel-layer-examples"></a>Beispiele für Die Sicherheitskanalebene

Die folgenden Beispiele veranschaulichen die Sicherheit in der [Kanalebene.](channel-layer-overview.md)

Windows Transportsicherheit über TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows Transportsicherheit über Named Pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

SSL-Transportsicherheit: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

Sicherheit im gemischten SSL-Modus: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Sicherheit im gemischten SSL-Modus: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Benutzername über SSL-Sicherheit im gemischten Modus: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Ausgestelltes Token über SSL-Sicherheit im gemischten Modus: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). X509-Zertifikat über SSL-Sicherheit im gemischten Modus: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time Setup für Sicherheitsbeispiele

Zum Ausführen von WWSAPI-Sicherheitsbeispielen müssen Sie die Client- und Serverzertifikate für SSL sowie ein lokales Benutzerkonto für die HTTP-Headerauthentifizierung einrichten. Bevor Sie beginnen, benötigen Sie die folgenden Tools:

-   MakeCert.exe (verfügbar im Windows 7 SDK.)
-   CertUtil.exe oder CertMgr.exe (CertUtil.exe ist ab Windows Server 2003 in den Windows SDKs verfügbar. CertMgr.exe ist im SDK Windows 7 verfügbar. Sie benötigen nur eines dieser Tools.)
-   HttpCfg.exe: (Sie benötigen dies nur, wenn Sie Windows 2003 oder Windows XP verwenden. Dieses Tool ist in Windows XP SP2-Supporttools verfügbar und enthält auch die Windows Server 2003 Resource Kit Tools CD.)

Wenn Sie die WWSAPI-Beispiele erhalten, indem Sie das Windows 7 SDK installieren, finden Sie die MakeCert.exe und CertMgr.exe unter %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v7.0 \\ bin.

Führen Sie das folgende fünfstufige Setup über die Eingabeaufforderung aus (mit erhöhten Rechten, wenn Sie Windows Vista und höher verwenden):

1.  Generieren Sie ein selbstsigniertes Zertifikat als Zertifizierungsstelle oder Aussteller: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**
2.  Generieren Sie ein Serverzertifikat mit dem vorherigen Zertifikat als Aussteller: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**
3.  Suchen Sie den Fingerabdruck (einen SHA-1-Hash mit 40 Zeichen) des Serverzertifikats, indem Sie einen der folgenden Befehle ausführen und nach dem Zertifikat mit dem Namen localhost mit dem Aussteller Fake-Test-CA suchen:
    -   **CertUtil.exe -store My localhost**
    -   **CertMgr.exe -s -r LocalMachine My**
4.  Registrieren Sie den Fingerabdruck des Serverzertifikats ohne Leerzeichen mit HTTP.SYS:
    -   Unter Windows Vista und höher (die Option "appid" ist eine beliebige GUID): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint>
    -   Auf Windows XP oder 2003:HttpCfg.exe ssl **-i 0.0.0.0:8443 -h <40CharacterThumbprint>**
5.  Erstellen eines lokalen Benutzers: **Net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic" /add**

Führen Sie die folgenden Befehle aus, um die Zertifikate, die SSL-Zertifikatbindung und das Benutzerkonto zu bereinigen, das Sie in den vorherigen Schritten erstellt haben. Hinweis: Wenn mehrere Zertifikate mit demselben Namen vorhanden sind, benötigen CertMgr.exe Ihre Eingabe, bevor sie gelöscht werden.

-   **CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**
-   **CertMgr.exe -del -c -n localhost -s -r LocalMachine My**
-   **Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (oder HttpCfg.exe delete ssl -i 0.0.0.0:8443)**
-   **Net user "TestUserForBasicAuth" /delete**

Stellen Sie sicher, dass es nur ein Stammzertifikat mit dem Namen Fake-Test-CA gibt. Wenn Sie sich nicht sicher sind, ist es immer sicher, diese Zertifikate mithilfe der oben genannten Bereinigungsbefehle zu bereinigt (und Fehler zu ignorieren), bevor Sie mit der fünfstufigen Einrichtung beginnen.

 

 




