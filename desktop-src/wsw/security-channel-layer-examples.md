---
title: Beispiele für Sicherheits Kanal Ebenen
description: In den folgenden Beispielen wird die Sicherheit in der Kanal Ebene veranschaulicht.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- Sicherheits Beispiele
- Sicherheits Beispiele, Setup
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340224"
---
# <a name="security-channel-layer-examples"></a>Beispiele für Sicherheits Kanal Ebenen

In den folgenden Beispielen wird die Sicherheit in der [Kanal Ebene](channel-layer-overview.md) veranschaulicht.

Windows-Transportsicherheit über TCP: Client: [requestreplytcpclientwithwindowstransportsecurityexample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [requestreplytcpserverwithwindowstransportsecurityexample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows-Transportsicherheit über Named Pipes: Client: [requestreplynamedpipesclientwithwindowstransportsecurityexample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [requestreplynamedpipesserverwithwindowstransportsecurityexample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

SSL-Transportsicherheit: Client: [httpclientwithsslexample](httpclientwithsslexample.md), Server: [httpserverwithsslexample](httpserverwithsslexample.md).

Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpclientwithusernameoversslexample](httpclientwithusernameoversslexample.md), Server: [httpserverwithusernameoversslexample](httpserverwithusernameoversslexample.md).

Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpclientwithkerberosoversslexample](httpclientwithkerberosoversslexample.md), Server: [httpserverwithkerberosoversslexample](httpserverwithkerberosoversslexample.md).

Benutzername über SSL-Sicherheit im gemischten Modus: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Ausgestelltes Token über SSL-Sicherheit im gemischten Modus: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). X509-Zertifikat über SSL-Sicherheit im gemischten Modus: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time Setup für Sicherheits Beispiele

Zum Ausführen von wwsapi-Sicherheits Beispielen müssen Sie sowohl die Client-als auch die Server Zertifikate für SSL sowie ein lokales Benutzerkonto für die HTTP-Header Authentifizierung einrichten. Bevor Sie beginnen, benötigen Sie die folgenden Tools:

-   MakeCert.exe (verfügbar im Windows 7 SDK.)
-   CertUtil.exe oder CertMgr.exe (CertUtil.exe ist in den Windows sdert ab Windows Server 2003 verfügbar. CertMgr.exe ist im Windows 7 SDK verfügbar. Sie benötigen nur eines dieser Tools.)
-   HttpCfg.exe: (Dies ist nur erforderlich, wenn Sie Windows 2003 oder Windows XP verwenden. Dieses Tool ist in den Windows XP SP2-Support Tools verfügbar und enthält auch die Windows Server 2003 Resource Kit-Tools-CD.)

Wenn Sie die wwsapi-Beispiele erhalten, indem Sie das Windows 7 SDK installieren, finden Sie die MakeCert.exe und CertMgr.exe unter% Program Files% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.

Führen Sie die folgende fünfstufige Einrichtung von der Eingabeaufforderung aus (erweitert, wenn Sie Windows Vista und höher verwenden):

1.  Generieren eines selbst signierten Zertifikats als Zertifizierungsstelle (Certificate Authority, ca) oder Aussteller: **MakeCert.exe-SS root-SR LocalMachine-n "CN = Fake-Test-ca"-CY Authority-r-SK "cakeycontainer"**
2.  Generieren Sie ein Serverzertifikat mit dem vorherigen Zertifikat als Aussteller: **MakeCert.exe-SS My-SR LocalMachine-n "CN = localhost"-Sky Exchange-is root-IR LocalMachine-in Fake-Test-ca-SK "serverkeycontainer"**
3.  Suchen Sie den Fingerabdruck (ein SHA-1-Hash mit 40 Zeichen) des Serverzertifikats, indem Sie einen der folgenden Befehle ausführen und nach dem Zertifikat mit dem Namen "localhost" mit dem Aussteller "Fake-Test-ca" suchen:
    -   **"Localhost"CertUtil.exe speichern**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  Registrieren Sie den Fingerabdruck des Serverzertifikats? s ohne Leerzeichen HTTP.SYS:
    -   Unter Windows Vista und höher (die "AppID"-Option ist eine beliebige GUID): **Netsh.exe http Add sslcert IPPort = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-aabbccddeeff}** CertHash =<40charakterithumbprint>
    -   Unter Windows XP oder 2003: **HttpCfg.exe Set SSL-i 0.0.0.0:8443-h <40charakterithumbprint>**
5.  Erstellen Sie einen lokalen Benutzer: **net user "testuserforbasicauth" "TstPWD@ \* 4bsic"/Add**

Führen Sie die folgenden Befehle aus, um die Zertifikate, die SSL-Zertifikat Bindung und das Benutzerkonto, die in den vorherigen Schritten erstellt wurden, zu bereinigen. Hinweis Wenn mehrere Zertifikate mit demselben Namen vorhanden sind, müssen CertMgr.exe vor dem Löschen die Eingabe benötigen.

-   **CertMgr.exe-del-c-n Fake-Test-ca-s-r LocalMachine root**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe HTTP DELETE sslcert IPPort = 0.0.0.0:8443 (oder HttpCfg.exe DELETE SSL-i 0.0.0.0:8443)**
-   **NET User "testuserforbasicauth"/Delete**

Stellen Sie sicher, dass nur ein Stamm Zertifikat mit dem Namen "Fake-Test-ca" vorhanden ist. Wenn Sie sich nicht sicher sind, können Sie versuchen, diese Zertifikate mithilfe der oben aufgeführten Bereinigungs Befehle zu bereinigen (und Fehler ignorieren), bevor Sie die fünfstufige Einrichtung starten.

 

 




