---
title: Gegenseitige Authentifizierung in einem Windows Sockets Service mit SCP
description: Die Themen in diesem Abschnitt enthalten Codebeispiele, die zeigen, wie die gegenseitige Authentifizierung mit einem Dienst durchgeführt wird, der sich selbst mithilfe eines Dienstverbindungspunkts (Service Connection Point, SCP) veröffentlicht.
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in einem Windows Sockets Service mit einem SCP AD
- Active Directory, verwenden, gegenseitige Authentifizierung, Windows Sockets-Dienst mit einem SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ede3f05744e402cb483e46d6eb116f653e20d9e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881373"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Gegenseitige Authentifizierung in einem Windows Sockets Service mit SCP

Die Themen in diesem Abschnitt enthalten Codebeispiele, die zeigen, wie die gegenseitige Authentifizierung mit einem Dienst durchgeführt wird, der sich selbst mithilfe eines Dienstverbindungspunkts (Service Connection Point, SCP) veröffentlicht. Die Beispiele basieren auf einem Microsoft Windows Sockets-Dienst, der ein SSPI-Paket verwendet, um die gegenseitige Authentifizierungsaushandlung zwischen einem Client und dem Dienst zu verarbeiten. Verwenden Sie die folgenden Verfahren, um die gegenseitige Authentifizierung innerhalb dieses Szenarios zu implementieren.

**So registrieren Sie SPNs in einem Verzeichnis, wenn ein Dienst installiert wird**

1.  Rufen Sie die [**DsGetSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) auf, um Dienstprinzipalnamen (SPNs) für den Dienst zu erstellen.
2.  Rufen Sie die [**DsWriteAccountSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) auf, um die SPNs für das Dienstkonto oder Computerkonto zu registrieren, in dessen Kontext der Dienst ausgeführt wird. Dieser Schritt muss von einem Domänenadministrator ausgeführt werden. Eine Ausnahme besteht darin, dass ein Dienst, der unter dem LocalSystem-Konto ausgeführt wird, seinen SPN im Format <service class> / &lt; &gt; "host" auf dem Computerkonto des Diensthosts registrieren kann.

**So überprüfen Sie die Konfiguration beim Dienststart**

-   Überprüfen Sie, ob die entsprechenden SPNs für das Konto registriert sind, unter dem der Dienst ausgeführt wird. Weitere Informationen finden Sie unter [Wartungstasks für Anmeldekonten.](logon-account-maintenance-tasks.md)

**So authentifizieren Sie den Dienst beim Clientstart**

1.  Rufen Sie Verbindungsdaten vom Dienstverbindungspunkt des Diensts ab.
2.  Stellen Sie eine Verbindung mit dem Dienst her.
3.  Rufen Sie die [**DsMakeSpn-Funktion**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) auf, um einen SPN für den Dienst zu erstellen. Erstellen Sie den SPN aus der bekannten Dienstklassenzeichenfolge und die vom Dienstverbindungspunkt abgerufenen Daten. Diese Daten enthalten den Hostnamen des Servers, auf dem der Dienst ausgeführt wird. Beachten Sie, dass der Hostname ein DNS-Name sein muss.
4.  Verwenden Sie ein SSPI-Sicherheitspaket, um die Authentifizierung durchzuführen:
    1.  Rufen Sie die [**AcquireCredentialsHandle-Funktion**](../SecAuthN/acquirecredentialshandle--general.md) auf, um die Anmeldeinformationen des Clients zu erhalten.
    2.  Übergeben Sie die Clientanmeldeinformationen und den SPN an die [**InitializeSecurityContext-Funktion,**](../SecAuthN/initializesecuritycontext--general.md) um ein Sicherheitsblob zu generieren, das zur Authentifizierung an den Dienst gesendet werden soll. Legen Sie das **ISC \_ REQ \_ MUTUAL \_ AUTH-Flag** fest, um gegenseitige Authentifizierung anzufordern.
    3.  Exchange Blobs mit dem Dienst, bis die Authentifizierung abgeschlossen ist.
5.  Überprüfen Sie die zurückgegebene Funktionenmaske für das **ISC \_ REQ \_ MUTUAL \_ AUTH-Flag,** um zu überprüfen, ob die gegenseitige Authentifizierung durchgeführt wurde.
6.  Wenn die Authentifizierung erfolgreich war, tauschen Sie Datenverkehr mit dem authentifizierten Dienst aus. Verwenden Sie digitale Signatur, um sicherzustellen, dass Nachrichten zwischen Client und Dienst nicht manipuliert wurden. Verwenden Sie die Verschlüsselung, sofern die Leistungsanforderungen nicht schwerwiegend sind. Weitere Informationen und ein Codebeispiel, das zeigt, wie die Funktionen [**MakeSignature,**](/windows/desktop/api/sspi/nf-sspi-makesignature) [**VerifySignature,**](/windows/desktop/api/sspi/nf-sspi-verifysignature) [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)und [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) in einem SSPI-Paket verwendet werden, finden Sie unter Sicherstellen der [Kommunikationsintegrität während Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**So authentifizieren Sie den Client vom Dienst, wenn ein Client eine Verbindung herstellt**

1.  Laden Sie ein SSPI-Sicherheitspaket, das die gegenseitige Authentifizierung unterstützt.
2.  Wenn ein Client eine Verbindung herstellt, verwenden Sie das Sicherheitspaket, um die Authentifizierung durchzuführen:
    1.  Rufen Sie die [**AcquireCredentialsHandle-Funktion**](../SecAuthN/acquirecredentialshandle--general.md) auf, um die Dienstanmeldeinformationen zu erhalten.
    2.  Übergeben Sie die Dienstanmeldeinformationen und das vom Client empfangene Sicherheitsblob an die [**AcceptSecurityContext-Funktion,**](../SecAuthN/acceptsecuritycontext--general.md) um ein Sicherheitsblob zu generieren, das an den Client zurücksenden soll.
    3.  Exchange Blobs mit dem Client, bis die Authentifizierung abgeschlossen ist.
3.  Überprüfen Sie die zurückgegebene Funktionenmaske für das **ASC \_ RET \_ MUTUAL \_ AUTH-Flag,** um zu überprüfen, ob die gegenseitige Authentifizierung durchgeführt wurde.
4.  Wenn die Authentifizierung erfolgreich war, tauschen Sie Datenverkehr mit dem authentifizierten Client aus. Verwenden Sie digitale Signatur und Verschlüsselung, es sei denn, die Leistung ist ein Problem.

Weitere Informationen und ein Codebeispiel für dieses Szenario mit gegenseitiger Authentifizierung finden Sie unter:

-   [Authentifizieren eines SCP-basierten Windows Sockets-Diensts durch einen Client](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Verfassen und Registrieren von SPNs für einen SCP-basierten Windows Sockets Service](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Authentifizieren eines Clients durch einen Windows Sockets-Dienst](how-a-windows-sockets-service-authenticates-a-client.md)

Weitere Informationen finden Sie unter

-   [Veröffentlichen mit Dienstverbindungspunkten](publishing-with-service-connection-points.md)
-   [SSPI-Dokumentation](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets-Dokumentation](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 
