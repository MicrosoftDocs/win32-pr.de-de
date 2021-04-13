---
title: Unterstützung von Multi-Hop in WinRM
description: Windows-Remoteverwaltung (WinRM) unterstützt die Delegierung von Benutzer Anmelde Informationen auf mehrere Remote Computer.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22c3d66e8605e932fe15b812f92d51350da2d69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482806"
---
# <a name="multi-hop-support-in-winrm"></a>Unterstützung von Multi-Hop in WinRM

Windows-Remoteverwaltung (WinRM) unterstützt die Delegierung von Benutzer Anmelde Informationen auf mehrere Remote Computer. Die Multi-Hop-Unterstützungsfunktion kann nun Anmelde Informationen Security Service Provider (kredssp) für die Authentifizierung verwenden. Mit "kredssp" kann eine Anwendung die Anmelde Informationen des Benutzers vom Client Computer an den Zielserver delegieren.

Die Authentifizierung mit der Authentifizierung ist für Umgebungen vorgesehen, in denen die Kerberos-Delegierung nicht verwendet werden kann. Die Unterstützung für "kredssp" wurde hinzugefügt, damit ein Benutzer eine Verbindung mit einem Remote Server herstellen und auf einen Computer mit einem zweiten Hop (z. b. auf eine Dateifreigabe) zugreifen kann.

Weitere Informationen zu "kredssp" finden Sie in [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> WinRM-Clients und-Server unterstützen die kredssp-Authentifizierung nur mit expliziten Anmelde Informationen.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Setup und Details zur Unterstützung der Multihop-Unterstützung

Es gibt mehrere Mechanismen zum Konfigurieren von WinRM-Einstellungen. Im folgenden Verfahren werden das **WinRM** -Hilfsprogramm und der Gruppenrichtlinie-Editor (**gpeer dit. msc**) verwendet. "Kredssp" kann auch mithilfe von Windows PowerShell für WinRM aktiviert werden. Ausführliche Informationen zu den Konfigurationsinformationen und Verwendungs Beispielen finden Sie in den Windows PowerShell-Cmdlets " [enable-wsmankredssp](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true)", " [Get-wsmankredssp](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)" und " [Deaktivierte wsmankredssp](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) ".

Die erstellungskredssp-Delegierung muss in den Client Einstellungen und in den Dienst Einstellungen auf dem Remote Computer aktiviert sein. Darüber hinaus erfordert die Verwendung von "up-SP" das Einrichten eines HTTP-oder HTTPS- [*Listener*](windows-remote-management-glossary.md) auf dem Server.

**So konfigurieren Sie die Unterstützung von Multi-Hop mithilfe der-Authentifizierung für WinRM**

1.  "Kredssp" muss in den Client Konfigurationseinstellungen aktiviert werden. Dieses Flag kann manuell oder über eine Gruppenrichtlinie Einstellung aktiviert werden. Die Standardeinstellung lautet **Falsch**. Die Richtlinie zum **Zulassen der Autorisierung** für die Authentifizierung befindet sich unter folgendem Pfad: Computer Konfiguration \\ Administrative Vorlage \\ Windows-Komponenten \\ Windows-Remoteverwaltung (WinRM) \\ WinRM-Client.

    Der folgende Befehl veranschaulicht, wie Sie das WinRM-Hilfsprogramm zum Aktivieren von "kredssp" auf dem WinRM-Client verwenden:

    **WinRM Set WinRM/config/Client/auth @ {condssp = "true"}**

2.  "Kredssp" muss in den WinRM-Dienst Konfigurationseinstellungen aktiviert werden. Dieses Flag kann manuell oder über eine Gruppenrichtlinie Einstellung aktiviert werden. Die Standardeinstellung lautet **Falsch**. Die Richtlinie zum **Zulassen der Autorisierung** für die Authentifizierung befindet sich unter folgendem Pfad: Computer Konfiguration \\ Administrative Vorlage \\ Windows-Komponenten \\ Windows-Remoteverwaltung (WinRM) \\ WinRM-Dienst.

    Der folgende Befehl veranschaulicht, wie Sie das WinRM-Hilfsprogramm zum Aktivieren von "kredssp" für den WinRM-Dienst verwenden:

    **WinRM Set WinRM/config/Service/auth @ {condssp = "true"}**

3.  Die Richtlinien Einstellung Delegierung neuer Anmelde Informationen zulassen (**allowfreshanmeldeinformationen**) muss auf dem WinRM-Client aktiviert sein, und ein Dienst Prinzipal Name (Service Principal Name, SPN) mit dem WSMAN-Präfix muss der Richtlinie hinzugefügt werden. Der SPN stellt den Zielcomputer dar, an den die Anmelde Informationen des Benutzers delegiert werden können. Der SPN kann auf einen oder mehrere Computer festgelegt werden. In der folgenden Tabelle finden Sie Beispiele für gültige Formate für SPNs.

    

    | SPN                                       | BESCHREIBUNG                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/MyComputer. mydomain. com<br/>  | WinRM-Server, der auf myComputer.mydomain.com ausgeführt wird.<br/>                         |
    | WSMAN/ \* . mydomain.com<br/>          | Alle WinRM-Server, die in mydomain.com ausgeführt werden.<br/>                               |
    | WSMAN/ \* . fabrikam.mydomain.com<br/> | Alle WinRM-Server, die in ausgeführt werden, auf allen Computern in. fabrikam.mydomain.com.<br/> |

    

     

    Weitere Informationen zum Festlegen von Gruppenrichtlinien finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

    Weitere Informationen zur Richtlinie **allowfreshanmeldeinformationen** finden Sie in der Richtlinien Beschreibung, die vom Gruppenrichtlinie-Editor bereitgestellt wird, und [KB 951608](https://support.microsoft.com/kb/951608). Die Richtlinie " **allowfresh-Anmelde** Informationen" befindet sich unter folgendem Pfad: Computer Konfiguration \\ Administrative Vorlagen \\ \\ Delegierung von System Anmelde Informationen.

4.  Ein HTTPS-oder http- [*Listener*](windows-remote-management-glossary.md) muss auf dem Server konfiguriert werden. Der Zertifikat Fingerabdruck, der zum Konfigurieren des HTTPS- *Listener* verwendet wird, wird auch zum Konfigurieren der Einstellung "certifikatethenbprint" unter den WinRM-Dienst Einstellungen verwendet.

    Der folgende Befehl veranschaulicht, wie Sie mit dem WinRM-Hilfsprogramm einen HTTPS- [*Listener*](windows-remote-management-glossary.md)konfigurieren:

    **WinRM quickconfig-Transport: https**

Wenn die Kerberos-Authentifizierung zwischen Client und Server nicht möglich ist, muss der Benutzer eine der folgenden Einstellungen für die Unterstützung von Multi-Hop konfigurieren:

-   Um die Sicherheit zu verbessern, sollte der Benutzer der WinRM-Dienst Einstellung das **certifiupethumschlag** -Attribut hinzufügen. Wenn der WinRM-Dienst mit einem **certifikatethbibprint** -Attribut konfiguriert ist, versucht der Dienst, das entsprechende Zertifikat im Speicher des lokalen Computers zu finden, und verwendet dieses Zertifikat für die Authentifizierung mit dem lokalen Computer. Wenn der WinRM-Dienst ein Zertifikat aus dem lokalen Computerspeicher zum Authentifizieren des Servers verwendet, muss dem Netzwerkdienst Konto der Zugriff auf den privaten Schlüssel des Zertifikats gestattet sein.

    > [!Note]  
    > Wenn die Dienst Einstellung nicht konfiguriert ist, verwendet der WinRM-Server ein selbst signiertes Zertifikat, das im Arbeitsspeicher erstellt wird, um die an den Client gesendeten Nachrichten zu verschlüsseln. Dieses Zertifikat wird jedoch nicht für die Authentifizierung verwendet.

     

-   Wenn weder die Kerberos-Authentifizierung noch die Zertifikat Fingerabdrücke verfügbar sind, kann der Benutzer die NTLM-Authentifizierung aktivieren. Wenn die NTLM-Authentifizierung verwendet wird, muss die Richtlinie neue Anmelde Informationen mit nur NTLM-Server Authentifizierung zulassen (**allowfreshkredentials. ntlmonly**) aktiviert sein, und der Richtlinie muss ein SPN mit dem WSMAN-Präfix hinzugefügt werden. Diese Einstellung ist weniger sicher als die Kerberos-Authentifizierung und Zertifikat Fingerabdrücke, weil Anmelde Informationen an einen nicht authentifizierten Server gesendet werden.

    Weitere Informationen zur Richtlinie **allowfreshkredentialseinsntlmonly** finden Sie in der Richtlinien Beschreibung, die vom Gruppenrichtlinie-Editor bereitgestellt wird, und [KB 951608](https://support.microsoft.com/kb/951608). Die Richtlinie " **allowfreshkredentials. ntlmonly** " befindet sich unter folgendem Pfad: Computer Konfiguration \\ Administrative Vorlagen \\ \\ Delegierung von System Anmelde Informationen.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Verwenden der fordssp-Authentifizierung mit expliziten Anmelde Informationen

Ein Benutzer kann sowohl über HTTP als auch über HTTPS explizite Anmelde Informationen angeben. Mit dem folgenden Befehl wird veranschaulicht, wie das WinRM-Hilfsprogramm verwendet wird, um einen Remote Vorgang mithilfe der-Authentifizierung mit der Authentifizierung mit expliziten Anmelde Informationen über HTTPS auszuführen

**WinRM-Vorgang-Remote: https://myMachine -Authentication: "kredssp-username: MyUserName-Password: mypassword"**

 

