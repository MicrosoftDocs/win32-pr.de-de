---
title: Authentifizierung für Remoteverbindungen
description: Windows Die Remoteverwaltung behält die Sicherheit für die Kommunikation zwischen Computern bei, indem mehrere Standardmethoden für die Authentifizierung und Nachrichtenverschlüsselung unterstützt werden.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0622f3d80e923f7d910740c71ee99f0e9a0bc446cea259b292e2d645e3b5a973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858875"
---
# <a name="authentication-for-remote-connections"></a>Authentifizierung für Remoteverbindungen

Windows Die Remoteverwaltung behält die Sicherheit für die Kommunikation zwischen Computern bei, indem mehrere Standardmethoden für die Authentifizierung und Nachrichtenverschlüsselung unterstützt werden.

## <a name="default-group-access"></a>Standardgruppenzugriff

Während des Setups erstellt WinRM die lokale Gruppe **\_ \_ WinRMRemoteWMIUsers**. WinRM schränkt dann den Remotezugriff auf alle Benutzer ein, die weder Mitglied der lokalen Verwaltungsgruppe noch der **WinRMRemoteWMIUsers-Gruppe \_ \_** sind. Sie können **\_ \_ WinRMRemoteWMIUsers** einen lokalen Benutzer, Domänenbenutzer oder eine Domänengruppe hinzufügen, indem Sie **net localgroup WinRMRemoteWMIUsers \_ \_ <domain> \\ <username> /add** an der Eingabeaufforderung eingeben. Optional können Sie die -Gruppenrichtlinie verwenden, um der Gruppe einen Benutzer hinzuzufügen.

## <a name="default-authentication-settings"></a>Standardauthentifizierungs-Einstellungen

Die Standardanmeldeinformationen, der Benutzername und das Kennwort sind die Anmeldeinformationen für das angemeldete Benutzerkonto, mit dem das Skript ausgeführt wird.

**So wechseln Sie zu einem anderen Konto auf einem Remotecomputer**

1.  Geben Sie die Anmeldeinformationen in einem [**ConnectionOptions- oder**](connectionoptions.md) [**IWSManConnectionOptions-Objekt**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) an, und geben Sie diese für den [**CreateSession-Aufruf**](wsman-createsession.md) an.
2.  Legen Sie **WSManFlagCredUserNamePassword** im *Flags-Parameter* im [**CreateSession-Aufruf**](wsman-createsession.md) fest.

Die folgende Liste enthält eine Liste der Schritte, die auftreten, wenn ein Skript oder eine Anwendung unter den Standardanmeldeinformationen ausgeführt wird:

-   [*Kerberos*](windows-remote-management-glossary.md) ist die Standardauthentifizierungsmethode, wenn sich der Client in einer Domäne befindet und die Remotezielzeichenfolge keine der folgenden Ist: localhost, 127.0.0.1 oder \[ ::1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) ist die Standardmethode, wenn sich der Client nicht in einer Domäne befindet, aber die Remotezielzeichenfolge eine der folgenden ist: localhost, 127.0.0.1 oder \[ ::1 \] .

Wenn Sie explizite Anmeldeinformationen mit einem [**ConnectionOptions-Objekt**](connectionoptions.md) angeben, ist Negotiate die Standardmethode. Die Aushandlungsauthentifizierung bestimmt, ob die laufende Authentifizierungsmethode Kerberos oder NTLM ist, je nachdem, ob sich die Computer in einer Domäne oder Arbeitsgruppe befinden. Wenn Sie eine Verbindung mit einem Remotezielcomputer mithilfe eines lokalen Kontos herstellen, sollte dem Konto der Computername vorangestellt werden. Beispiel: myComputer \\ myUsername.

Wenn Sie Negotiate-, Digest- oder Basic-Authentifizierung angeben und kein [**ConnectionOptions-Objekt**](connectionoptions.md) angeben, erhalten Sie eine Fehlermeldung, die angibt, dass explizite Anmeldeinformationen erforderlich sind. Wenn HTTPS nicht der Transport ist, muss der Remotezielcomputer in der Liste der vertrauenswürdigen Hostcomputer konfiguriert werden.

Weitere Informationen zu den Authentifizierungstypen, die in den Standardkonfigurationseinstellungen aktiviert sind, finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)

## <a name="basic-authentication"></a>Standardauthentifizierung

Um die [](windows-remote-management-glossary.md) Standardauthentifizierung explizit im Aufruf von [**WSMan.CreateSession**](wsman-createsession.md)zu erstellen, legen Sie die **Flags WSManFlagUseBasic** und **WSManFlagCredUserNamePassword** im *flags-Parameter* fest. Die Standardauthentifizierung ist in den Standardkonfigurationseinstellungen sowohl für den WinRM-Client als auch für den WinRM-Server deaktiviert.

## <a name="digest-authentication"></a>Digestauthentifizierung

Um die Digestauthentifizierung [*explizit*](windows-remote-management-glossary.md) im Aufruf von [**WSMan.CreateSession**](wsman-createsession.md)zu erstellen, legen Sie das **Flag WSManFlagUseDigest** im *flags-Parameter* fest. Digest wird nicht unterstützt. Sie kann nicht für die WinRM-Serverkomponente konfiguriert werden.

## <a name="negotiate-authentication"></a>Aushandeln der Authentifizierung

Legen Sie [](windows-remote-management-glossary.md) das **Flag WSManFlagUseNegotiate** im *flags-Parameter* fest, um im Aufruf von [**WSMan.CreateSession**](wsman-createsession.md)explizit die Negotiate-Authentifizierung (auch als integrierte Windows-Authentifizierung bezeichnet) zu erstellen.

[Die Benutzerkontensteuerung (User Account Control, UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) wirkt sich auf den Zugriff auf den WinRM-Dienst aus. Wenn die Negotiate-Authentifizierung in einer Arbeitsgruppe verwendet wird, kann nur das integrierte Administratorkonto auf den Dienst zugreifen. Um allen Konten in der Gruppe Administratoren den Zugriff auf den Dienst zu ermöglichen, legen Sie den folgenden Registrierungswert fest:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Kerberos-Authentifizierung

Um die [*Kerberos-Authentifizierung*](windows-remote-management-glossary.md) explizit im Aufruf von [**WSMan.CreateSession**](wsman-createsession.md)zu erstellen, legen Sie das **WSManFlagUseKerberos-Flag** im *flags-Parameter* fest. Sowohl der Client- als auch der Servercomputer müssen einer Domäne beigetreten sein. Wenn Sie Kerberos als Authentifizierungsmethode verwenden, können Sie keine IP-Adresse im Aufruf von [**WSMan.CreateSession**](wsman-createsession.md) oder [**IWSMan::CreateSession verwenden.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)

## <a name="client-certificate-based-authentication"></a>Clientzertifikatbasierte Authentifizierung

Legen Sie das **Flag WSManFlagUseClientCertificate** im *flags-Parameter* fest, um die clientzertifikatbasierte Authentifizierung im Aufruf von [**WSMan.CreateSession**](wsman-createsession.md)zu erstellen.

Sie müssen zunächst die Zertifikatauthentifizierung sowohl auf dem Client als auch im Dienst mithilfe des Winrm-Befehlszeilentools aktivieren. Weitere Informationen finden Sie unter [Aktivieren von Authentifizierungsoptionen.](#enabling-or-disabling-authentication-options) Sie müssen auch einen Eintrag in der Tabelle CertMapping auf dem WinRM-Servercomputer erstellen. Dadurch wird eine Zuordnung zwischen mindestens einem Zertifikat und einem lokalen Konto erstellt. Nachdem das Zertifikat für die Authentifizierung und Autorisierung verwendet wurde, wird das entsprechende lokale Konto für Vorgänge verwendet, die vom WinRM-Dienst ausgeführt werden.

Die Zuordnung kann für einen bestimmten Ressourcen-URI erstellt werden. Um mehr zu erfahren, einschließlich der Erstellung eines CertMapping-Tabelleneintrags, geben Sie **winrm help certmapping** an der Eingabeaufforderung ein.

> [!Note]  
> Das Zertifikat mit maximaler Größe, das von WinRM in diesem Kontext verwendet werden kann, beträgt 16 KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Aktivieren oder Deaktivieren von Authentifizierungsoptionen

Die Standardauthentifizierungsoption bei der Systeminstallation ist Kerberos. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)

Wenn Ihr Skript oder Ihre Anwendung eine bestimmte Authentifizierungsmethode erfordert, die nicht aktiviert ist, müssen Sie die Konfiguration ändern, um diese Art der Authentifizierung zu aktivieren. Diese Änderung kann mithilfe des **Winrm-Befehlszeilentools** oder über Gruppenrichtlinie für das **Windows-Remoteverwaltungsobjekt Gruppenrichtlinie werden.** Sie können auch bestimmte Authentifizierungsmethoden deaktivieren.

**So aktivieren oder deaktivieren Sie die Authentifizierung mit dem Winrm-Tool**

1.  Verwenden Sie zum Festlegen der Konfiguration für den WinRM-Client den **Befehl Winrm Set,** und geben Sie den Client an. Beispielsweise deaktiviert der folgende Befehl die Digestauthentifizierung für den Client.

    **winrm set winrm/config/client/auth @{Digest="false"}**

2.  Verwenden Sie zum Festlegen der Konfiguration für den WinRM-Server den **Befehl Winrm Set,** und geben Sie den Dienst an. Beispielsweise aktiviert der folgende Befehl die Kerberos-Authentifizierung für den Dienst.

    **winrm set winrm/config/service/auth @{Kerberos="true"}**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> </dl>

 

 




