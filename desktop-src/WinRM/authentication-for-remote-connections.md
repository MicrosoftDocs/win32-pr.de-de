---
title: Authentifizierung für Remote Verbindungen
description: Windows-Remoteverwaltung gewährleistet die Sicherheit für die Kommunikation zwischen Computern, indem mehrere Standard Authentifizierungsmethoden und Nachrichten Verschlüsselung unterstützt werden.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e9aa125f2ccf5d8c224eee645a6dba1ec2fd96e
ms.sourcegitcommit: 25c6d442ab55cbf0e065398a006b1d409349fffd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2020
ms.locfileid: "104038693"
---
# <a name="authentication-for-remote-connections"></a>Authentifizierung für Remote Verbindungen

Windows-Remoteverwaltung gewährleistet die Sicherheit für die Kommunikation zwischen Computern, indem mehrere Standard Authentifizierungsmethoden und Nachrichten Verschlüsselung unterstützt werden.

## <a name="default-group-access"></a>Standard Gruppen Zugriff

Während des Setups erstellt WinRM die lokale Gruppe **winrmremotewmiusers \_ \_**. WinRM schränkt dann den Remote Zugriff auf alle Benutzer ein, die weder Mitglied der lokalen Verwaltungsgruppe noch der Gruppe " **\_ \_ winrmremotewmiusers** " sind. Sie können **winrmremotewmiusers \_ \_** einen lokalen Benutzer, Domänen Benutzer oder eine Domänen Gruppe hinzufügen, indem Sie **net localgroup winrmremotewmiusers \_ \_ /Add <domain> \\ <username>** an der Eingabeaufforderung eingeben. Optional können Sie den Gruppenrichtlinie verwenden, um der Gruppe einen Benutzer hinzuzufügen.

## <a name="default-authentication-settings"></a>Standard Authentifizierungs Einstellungen

Die Standard Anmelde Informationen, der Benutzername und das Kennwort sind die Anmelde Informationen für das angemeldete Benutzerkonto, das das Skript ausführt.

**So wechseln Sie zu einem anderen Konto auf einem Remote Computer**

1.  Geben [**Sie die Anmelde**](wsman-createsession.md) Informationen in einem [**ConnectionOptions**](connectionoptions.md) -oder [**iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) -Objekt an, und stellen Sie diese für den aufzurufenden Befehl bereit.
2.  Legen Sie das **wsmanflagkredusernamepassword** im " *Flags* "-Parameter im " [**anatesession**](wsman-createsession.md) "-Befehl fest.

Die folgende Liste enthält eine Liste der Vorgänge, die auftreten, wenn ein Skript oder eine Anwendung unter den Standard Anmelde Informationen ausgeführt wird:

-   [*Kerberos*](windows-remote-management-glossary.md) ist die Standard Authentifizierungsmethode, wenn sich der Client in einer Domäne befindet und die Remote Ziel Zeichenfolge kein der folgenden ist: localhost, 127.0.0.1 oder \[ :: 1 \] .
-   [*Aushandeln*](windows-remote-management-glossary.md) ist die Standardmethode, wenn der Client sich nicht in einer Domäne befindet, die Remote Ziel Zeichenfolge jedoch eine der folgenden ist: localhost, 127.0.0.1 oder \[ :: 1 \] .

Wenn Sie explizite Anmelde Informationen mit einem [**ConnectionOptions**](connectionoptions.md) -Objekt angeben, ist aushandeln die Standardmethode. Durch die Aushandlung der Authentifizierung wird bestimmt, ob die fortlaufende Authentifizierungsmethode Kerberos oder NTLM ist, je nachdem, ob sich die Computer in einer Domäne oder Arbeitsgruppe befinden. Wenn Sie mithilfe eines lokalen Kontos eine Verbindung mit einem Remote Zielcomputer herstellen, sollte dem Konto der Computername als Präfix vorangestellt werden. Beispiel: MyComputer \\ MyUserName.

Wenn Sie Aushandlungs-, Digest-oder Standard Authentifizierung angeben und ein [**ConnectionOptions**](connectionoptions.md) -Objekt nicht bereitstellen, wird eine Fehlermeldung angezeigt, die besagt, dass explizite Anmelde Informationen erforderlich sind. Wenn HTTPS nicht der Transport ist, muss der Ziel-Remote Computer in der Liste der vertrauenswürdigen Host Computer konfiguriert werden.

Weitere Informationen zu den Authentifizierungs Typen, die in den Standard Konfigurationseinstellungen aktiviert sind, finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

## <a name="basic-authentication"></a>Standardauthentifizierung

Um die Standard [*Authentifizierung im*](windows-remote-management-glossary.md) [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen explizit einzurichten, legen Sie die Kennzeichen " **wsmanflagusebasic** " und " **wsmanflagfordusernamepassword** " im *Flags* -Parameter fest. Die Standard Authentifizierung ist in den Standard Konfigurationseinstellungen für den WinRM-Client und den WinRM-Server deaktiviert.

## <a name="digest-authentication"></a>Digestauthentifizierung

Um die Digestauthentifizierung im [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen explizit festzulegen, legen Sie das **wsmanflagusedigest** -Flag im *Flags* - [*Parameter fest.*](windows-remote-management-glossary.md) Digest wird nicht unterstützt. Sie kann nicht für die WinRM-Serverkomponente konfiguriert werden.

## <a name="negotiate-authentication"></a>Authentifizierung aushandeln

Legen Sie zum expliziten Einrichten der [*Aushandlungs*](windows-remote-management-glossary.md) Authentifizierung, die auch als integrierte Windows-Authentifizierung bezeichnet wird, im [**WSMAN. foratesession**](wsman-createsession.md)-Befehl das **wsmanflagusenegotiate** -Flag im *Flags* -Parameter fest.

Die [Benutzerkontensteuerung (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) wirkt sich auf den Zugriff auf den WinRM-Dienst aus. Wenn die Aushandlungs Authentifizierung in einer Arbeitsgruppe verwendet wird, kann nur das integrierte Administrator Konto auf den Dienst zugreifen. Legen Sie den folgenden Registrierungs Wert fest, damit alle Konten in der Gruppe "Administratoren" auf den Dienst zugreifen können:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **localaccountdekenfilterpolicy** = 1

## <a name="kerberos-authentication"></a>Kerberos-Authentifizierung

Um die [*Kerberos*](windows-remote-management-glossary.md) -Authentifizierung im [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen explizit einzurichten, legen Sie das **wsmanflagusekerberos** -Flag im *Flags* -Parameter fest. Sowohl der Client als auch der Server Computer müssen einer Domäne hinzugefügt werden. Wenn Sie Kerberos als Authentifizierungsmethode verwenden, können Sie keine IP-Adresse im [**WSMAN. kreatesession**](wsman-createsession.md) -oder [**iwsman:: anatesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)-Befehl verwenden.

## <a name="client-certificate-based-authentication"></a>Client Zertifikat basierte Authentifizierung

Legen Sie zum Einrichten der Client Zertifikat basierten Authentifizierung im [**WSMAN. foratesession**](wsman-createsession.md)-Befehl das **wsmanflaguseclientcertificate** -Flag im *Flags* -Parameter fest.

Sie müssen zunächst die Zertifikat Authentifizierung für den Client und den Dienst mithilfe des WinRM-Befehlszeilen Tools aktivieren. Weitere Informationen finden Sie unter [Aktivieren von Authentifizierungs Optionen](#enabling-or-disabling-authentication-options). Sie müssen auch einen Eintrag in der certmapping-Tabelle auf dem WinRM-Server Computer erstellen. Dadurch wird eine Zuordnung zwischen einem oder mehreren Zertifikaten und einem lokalen Konto erstellt. Nachdem das Zertifikat für die Authentifizierung und Autorisierung verwendet wurde, wird das entsprechende lokale Konto für Vorgänge verwendet, die vom WinRM-Dienst ausgeführt werden.

Die Zuordnung kann für einen bestimmten Ressourcen-URI erstellt werden. Weitere Informationen, einschließlich der Erstellung eines certmapping-Tabellen Eintrags, erhalten Sie, indem Sie an der Eingabeaufforderung **WinRM Help certmapping** eingeben.

> [!Note]  
> Das von WinRM in diesem Kontext verwendbare maximale Größen Zertifikat beträgt 16 KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Aktivieren oder Deaktivieren von Authentifizierungs Optionen

Die Standard Authentifizierungs Option bei der Systeminstallation ist Kerberos. Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

Wenn Ihr Skript oder Ihre Anwendung eine bestimmte Authentifizierungsmethode erfordert, die nicht aktiviert ist, müssen Sie die Konfiguration ändern, um diesen Authentifizierungstyp zu aktivieren. Diese Änderung kann mit dem **WinRM** -Befehlszeilen Tool oder über Gruppenrichtlinie für das **Windows-Remoteverwaltung Gruppenrichtlinie Objekt** vorgenommen werden. Sie können auch bestimmte Authentifizierungsmethoden deaktivieren.

**So aktivieren oder deaktivieren Sie die Authentifizierung mit dem WinRM-Tool**

1.  Um die Konfiguration für den WinRM-Client festzulegen, verwenden Sie den Befehl **WinRM Set** , und geben Sie den Client an. Der folgende Befehl deaktiviert z. b. die Digestauthentifizierung für den Client.

    **WinRM Set WinRM/config/Client/auth @ {Digest = "false"}**

2.  Um die Konfiguration für den WinRM-Server festzulegen, verwenden Sie den Befehl **WinRM Set** , und geben Sie den Dienst an. Der folgende Befehl aktiviert z. b. die Kerberos-Authentifizierung für den Dienst.

    **WinRM Set WinRM/config/Service/auth @ {Kerberos = "true"}**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[**WSMAN. kreatesession**](wsman-createsession.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> </dl>

 

 




