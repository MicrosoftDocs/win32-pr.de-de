---
title: Multi-Hop-Unterstützung in WinRM
description: Windows Die Remoteverwaltung (WinRM) unterstützt die Delegierung von Benutzeranmeldeinformationen auf mehreren Remotecomputern.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76be3054fc9c0d624c206cf5a26d7788e763dfc81f1b2069f6abff8736be2388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121760"
---
# <a name="multi-hop-support-in-winrm"></a>Multi-Hop-Unterstützung in WinRM

Windows Die Remoteverwaltung (WinRM) unterstützt die Delegierung von Benutzeranmeldeinformationen auf mehreren Remotecomputern. Die Multi-Hop-Unterstützungsfunktion kann jetzt den Credential Security Service Provider (CredSSP) für die Authentifizierung verwenden. CredSSP ermöglicht einer Anwendung, die Anmeldeinformationen des Benutzers vom Clientcomputer an den Zielserver zu delegieren.

Die CredSSP-Authentifizierung ist für Umgebungen vorgesehen, in denen die Kerberos-Delegierung nicht verwendet werden kann. Unterstützung für CredSSP wurde hinzugefügt, damit ein Benutzer eine Verbindung mit einem Remoteserver herstellen kann und auf einen Computer mit zweitem Hop zugreifen kann, z. B. eine Dateifreigabe.

Weitere Informationen zu CredSSP finden Sie unter [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> WinRM-Clients und -Server unterstützen die CredSSP-Authentifizierung nur mit expliziten Anmeldeinformationen.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Setup und Details zur Konfiguration der Multi-Hop-Unterstützung

Es gibt mehrere Mechanismen zum Konfigurieren von WinRM-Einstellungen. Im folgenden Verfahren werden das **Hilfsprogramm winrm** und Gruppenrichtlinie Editor (**GPEdit.msc**) verwendet. CredSSP kann auch mithilfe von Windows PowerShell für WinRM aktiviert werden. Ausführliche Konfigurationsinformationen und Verwendungsbeispiele finden Sie in den Cmdlets [Enable-WSManCredSSP,](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)und [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Windows PowerShell.

Die CredSSP-Delegierung muss in den Clienteinstellungen und in den Diensteinstellungen auf dem Remotecomputer aktiviert werden. Darüber hinaus muss für die Verwendung von CredSSP ein HTTP- oder [*HTTPS-Listener*](windows-remote-management-glossary.md) auf dem Server eingerichtet werden.

**So konfigurieren Sie die Multi-Hop-Unterstützung mit credSSP-Authentifizierung für WinRM**

1.  CredSSP muss in den Clientkonfigurationseinstellungen aktiviert sein. Dieses Flag kann manuell oder über eine Gruppenrichtlinie-Einstellung aktiviert werden. Die Standardeinstellung lautet **Falsch**. Die **CredSSP-Authentifizierungsrichtlinie zulassen** befindet sich unter dem folgenden Pfad: Administrative Vorlage für die Computerkonfiguration \\ Windows Komponenten Windows \\ \\ WinRM-Client (Remoteverwaltung). \\

    Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm, um CredSSP auf dem WinRM-Client zu aktivieren:

    **winrm set winrm/config/client/auth @{CredSSP="true"}**

2.  CredSSP muss in den Konfigurationseinstellungen des WinRM-Diensts aktiviert sein. Dieses Flag kann manuell oder über eine Gruppenrichtlinie-Einstellung aktiviert werden. Die Standardeinstellung lautet **Falsch**. Die **Richtlinie CredSSP-Authentifizierung zulassen** befindet sich unter dem folgenden Pfad: Administrative Vorlage für die Computerkonfiguration Windows Komponenten Windows \\ \\ \\ WinRM-Diensts (Remote management, \\ Remoteverwaltung).

    Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm, um CredSSP für den WinRM-Dienst zu aktivieren:

    **winrm set winrm/config/service/auth @{CredSSP="true"}**

3.  Die Richtlinieneinstellung Allow Delegating Fresh Credentials (**AllowFreshCredentials**) muss auf dem WinRM-Client aktiviert sein, und der Richtlinie muss ein Dienstprinzipalname (Service Principal Name, SPN) mit dem WSMAN-Präfix hinzugefügt werden. Der SPN stellt den Zielcomputer dar, an den die Benutzeranmeldeinformationen delegiert werden können. Der SPN kann auf einen oder mehrere Computer festgelegt werden. Die folgende Tabelle enthält Beispiele für gültige Formate für SPNs.

    

    | SPN                                       | Beschreibung                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/myComputer.myDomain.com<br/>  | WinRM-Server, der auf myComputer.myDomain.com ausgeführt wird.<br/>                         |
    | \*WSMAN/.myDomain.com<br/>          | Alle WinRM-Server, die in myDomain.com ausgeführt werden.<br/>                               |
    | \*WSMAN/.fabrikam.myDomain.com<br/> | Alle WinRM-Server, die in auf allen Computern in .fabrikam.myDomain.com ausgeführt werden.<br/> |

    

     

    Weitere Informationen zum Festlegen von Gruppenrichtlinien finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)

    Weitere Informationen zur **AllowFreshCredentials-Richtlinie** finden Sie in der Richtlinienbeschreibung, die vom Gruppenrichtlinie-Editor bereitgestellt wird, und [kb 951608](https://support.microsoft.com/kb/951608). Die **Richtlinie AllowFreshCredentials** befindet sich unter dem folgenden Pfad: Computerkonfiguration \\ Administrative Vorlagen \\ \\ Delegierung von Systemanmeldeinformationen.

4.  Ein HTTPS- oder [*HTTP-Listener*](windows-remote-management-glossary.md) muss auf dem Server konfiguriert werden. Der Zertifikatfingerabdruck, der zum Konfigurieren des *HTTPS-Listeners* verwendet wird, wird auch verwendet, um die Einstellung CertificateThumbprint unter den WinRM-Diensteinstellungen zu konfigurieren.

    Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm zum Konfigurieren eines [*HTTPS-Listeners:*](windows-remote-management-glossary.md)

    **winrm quickconfig -transport:https**

Wenn die Kerberos-Authentifizierung zwischen Client und Server nicht möglich ist, muss der Benutzer eine der folgenden Einstellungen für die Unterstützung mehrerer Hops konfigurieren:

-   Zur Verbesserung der Sicherheit sollte der Benutzer der WinRM-Diensteinstellung das **CertificateThumbprint-Attribut** hinzufügen. Wenn der WinRM-Dienst mit einem **CertificateThumbprint-Attribut** konfiguriert ist, versucht der Dienst, das entsprechende Zertifikat im Lokalen Computerspeicher zu finden, und verwendet dieses Zertifikat für die CredSSP-Authentifizierung. Wenn der WinRM-Dienst ein Zertifikat aus dem Lokalen Computerspeicher verwendet, um den Server zu authentifizieren, muss dem Netzwerkdienstkonto Zugriff auf den privaten Schlüssel des Zertifikats gewährt werden.

    > [!Note]  
    > Wenn die Diensteinstellung nicht konfiguriert ist, verwendet der WinRM-Server ein selbstsigniertes Zertifikat, das im Arbeitsspeicher erstellt wird, um an den Client gesendete Nachrichten zu verschlüsseln. Dieses Zertifikat wird jedoch nicht für die Authentifizierung verwendet.

     

-   Wenn weder Kerberos-Authentifizierung noch Zertifikatfingerabdrücke verfügbar sind, kann der Benutzer die NTLM-Authentifizierung aktivieren. Wenn die NTLM-Authentifizierung verwendet wird, muss die Richtlinie Allow Fresh Credentials with NTLM-only Server Authentication (**AllowFreshCredentialsWhenNTLMOnly**) aktiviert sein, und der Richtlinie muss ein SPN mit dem WSMAN-Präfix hinzugefügt werden. Diese Einstellung ist weniger sicher als die Kerberos-Authentifizierung und der Zertifikatfingerabdruck, da Anmeldeinformationen an einen nicht authentifizierten Server gesendet werden.

    Weitere Informationen zur **Richtlinie AllowFreshCredentialsWhenNTLMOnly** finden Sie in der Richtlinienbeschreibung des Gruppenrichtlinie-Editors und [in kb 951608](https://support.microsoft.com/kb/951608). Die **Richtlinie AllowFreshCredentialsWhenNTLMOnly** befindet sich unter dem folgenden Pfad: Computerkonfiguration \\ Administrative Vorlagen \\ \\ Delegierung von Systemanmeldeinformationen.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Verwenden der CredSSP-Authentifizierung mit expliziten Anmeldeinformationen

Ein Benutzer kann explizite Anmeldeinformationen sowohl über HTTP als auch über HTTPS angeben. Der folgende Befehl veranschaulicht die Verwendung des Hilfsprogramms winrm zum Ausführen eines Remotevorgangs mit credSSP-Authentifizierung mit expliziten Anmeldeinformationen über HTTPS:

**winrm OPERATION -remote: https://myMachine -authentication:CredSSP -username:myUsername -password:myPassword**

 

