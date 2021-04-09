---
title: Gegenseitige Authentifizierung in einem Windows Sockets-Dienst mit SCP
description: Die Themen in diesem Abschnitt enthalten Codebeispiele, die zeigen, wie die gegenseitige Authentifizierung bei einem Dienst durchgeführt wird, der sich mit einem Dienst Verbindungspunkt (Service Connection Point, SCP) veröffentlicht.
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in einem Windows Sockets-Dienst mit einem SCP-AD
- Active Directory, verwenden der gegenseitigen Authentifizierung, Windows Sockets Service mit einem SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527715c4a35dc15cd67f5820e6fa891b56452399
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858138"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Gegenseitige Authentifizierung in einem Windows Sockets-Dienst mit SCP

Die Themen in diesem Abschnitt enthalten Codebeispiele, die zeigen, wie die gegenseitige Authentifizierung bei einem Dienst durchgeführt wird, der sich mit einem Dienst Verbindungspunkt (Service Connection Point, SCP) veröffentlicht. Die Beispiele basieren auf einem Microsoft Windows Sockets-Dienst, der ein SSPI-Paket zum Verarbeiten der Aushandlung der gegenseitigen Authentifizierung zwischen einem Client und dem Dienst verwendet. Verwenden Sie die folgenden Verfahren, um die gegenseitige Authentifizierung innerhalb dieses Szenarios zu implementieren.

**So registrieren Sie SPNs in einem Verzeichnis, wenn ein Dienst installiert ist**

1.  Wenden Sie die [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion an, um Dienst Prinzipal Namen (SPNs) für den Dienst zu verfassen.
2.  Wenden Sie die [**dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) -Funktion an, um die SPNs für das Dienst Konto oder das Computer Konto in zu registrieren, in dessen Kontext der Dienst ausgeführt wird. Dieser Schritt muss von einem Domänen Administrator ausgeführt werden. eine Ausnahme besteht darin, dass ein Dienst, der unter dem Konto "LocalSystem" ausgeführt wird, den SPN im Format " <service class> / <host> " für das Computer Konto des Dienst Hosts registrieren kann.

**So überprüfen Sie die Konfiguration beim Dienst Start**

-   Vergewissern Sie sich, dass die entsprechenden SPNs für das Konto, unter dem der Dienst ausgeführt wird, registriert sind. Weitere Informationen finden Sie unter [Anmelde Konto-Wartungs Tasks](logon-account-maintenance-tasks.md).

**So authentifizieren Sie den Dienst beim Client Start**

1.  Rufen Sie die Verbindungsdaten vom Dienst Verbindungspunkt des dienstanders ab.
2.  Stellen Sie eine Verbindung mit dem Dienst her.
3.  Wenden Sie die [**dsmakespn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) -Funktion an, um einen SPN für den Dienst zu erstellen. Erstellen Sie den SPN aus der Zeichenfolge der bekannten Dienstklasse und die Daten, die vom Dienst Verbindungspunkt abgerufen werden. Diese Daten enthalten den Hostnamen des Servers, auf dem der-Dienst ausgeführt wird. Beachten Sie, dass es sich bei dem Hostnamen um einen DNS-Namen handeln muss.
4.  Verwenden Sie ein SSPI-Sicherheitspaket, um die Authentifizierung durchzuführen:
    1.  Rufen Sie die [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) -Funktion auf, um die Anmelde Informationen des Clients abzurufen.
    2.  Übergeben Sie die Client Anmelde Informationen und den SPN an die [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) -Funktion, um ein sicherheitsblob zu generieren, das für die Authentifizierung an den Dienst gesendet werden soll. Legen Sie das Flag für die gegenseitige Authentifizierung von **ISC \_ req \_ \_** zum Anfordern der gegenseitigen Authentifizierung fest
    3.  Exchange-blobdienste bis zum Abschluss der Authentifizierung mit dem Dienst.
5.  Überprüfen Sie die zurückgegebene Funktions Maske für das ISC req-Flag für die **\_ \_ gegenseitige \_** Authentifizierung.
6.  Wenn die Authentifizierung erfolgreich war, tauschen Sie den Datenverkehr mit dem authentifizierten Dienst aus. Verwenden Sie digitales Signieren, um sicherzustellen, dass Nachrichten zwischen Client und Dienst nicht manipuliert wurden. Wenn die Leistungsanforderungen nicht schwerwiegend sind, verwenden Sie die Verschlüsselung. Weitere Informationen und ein Codebeispiel, das zeigt, wie die Funktionen [**makesignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**verschlüsseltmessage**](../SecAuthN/encryptmessage--general.md)und [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) in einem SSPI-Paket verwendet werden, finden Sie unter [sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**So authentifizieren Sie den Client durch den Dienst, wenn ein Client eine Verbindung herstellt**

1.  Laden eines SSPI-Sicherheitspakets, das die gegenseitige Authentifizierung unterstützt.
2.  Wenn ein Client eine Verbindung herstellt, verwenden Sie das Sicherheitspaket, um die Authentifizierung durchzuführen:
    1.  Rufen Sie die [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) -Funktion auf, um die Dienst Anmelde Informationen abzurufen.
    2.  Übergeben Sie die Dienst Anmelde Informationen und das vom Client empfangene sicherheitsblob an die [**Accept-SecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) -Funktion, um ein sicherheitsblob zu generieren, das an den Client zurückgesendet werden soll.
    3.  Exchange-blobschauf dem Client, bis die Authentifizierung beendet ist.
3.  Überprüfen Sie die zurückgegebene Funktions Maske für das ASC ret-Flag für die **\_ \_ gegenseitige \_** Authentifizierung, um sicherzustellen, dass die gegenseitige Authentifizierung
4.  Wenn die Authentifizierung erfolgreich war, tauschen Sie den Datenverkehr mit dem authentifizierten Client aus. Verwenden Sie digitale Signaturen und Verschlüsselung, es sei denn, die Leistung ist ein Problem

Weitere Informationen und ein Codebeispiel für dieses Szenario für die gegenseitige Authentifizierung finden Sie unter:

-   [Authentifizieren eines SCP-basierten Windows Sockets-Dienstanbieter durch einen Client](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Erstellen und Registrieren von SPNs für einen SCP-basierten Windows Sockets-Dienst](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Authentifizieren eines Clients durch einen Windows-Sockets-Dienst](how-a-windows-sockets-service-authenticates-a-client.md)

Weitere Informationen finden Sie unter

-   [Veröffentlichen mit Dienst Verbindungs Punkten](publishing-with-service-connection-points.md)
-   [SSPI-Dokumentation](/windows/desktop/SecAuthN/sspi)
-   [Dokumentation zu Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 