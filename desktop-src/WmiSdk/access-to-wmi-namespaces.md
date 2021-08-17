---
description: WMI verwendet einen Standard-Windows Sicherheitsbeschreibung, um den Zugriff auf WMI-Namespaces zu steuern.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Zugriff auf WMI-Namespaces
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b750c8dee2b95597636620dc54ad193cb762cd259b2bf7149c52996e85e09b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926026"
---
# <a name="access-to-wmi-namespaces"></a>Zugriff auf WMI-Namespaces

WMI verwendet einen Standard-Windows *Sicherheitsbeschreibung,* um den Zugriff auf WMI-Namespaces zu steuern. Wenn Sie eine Verbindung mit WMI herstellen, entweder über den WMI-Moniker "winmgmts" oder durch einen Aufruf von [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) oder [**SWbemLocator.ConnectServer,**](swbemlocator-connectserver.md)stellen Sie eine Verbindung mit einem bestimmten Namespace her.

Die folgenden Informationen werden in diesem Thema erläutert:

-   [WMI-Namespacesicherheit](#wmi-namespace-security)
-   [WMI-Namespaceüberwachung](#wmi-namespace-auditing)
-   [Typen von Namespaceereignissen](#types-of-namespace-events)
-   [Namespacezugriffs-Einstellungen](#namespace-access-settings)
-   [Standardberechtigungen für WMI-Namespaces](#default-permissions-on-wmi-namespaces)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-namespace-security"></a>WMI-Namespacesicherheit

WMI verwaltet die Namespacesicherheit, indem das [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) des Benutzers, der eine Verbindung mit dem Namespace herstellt, mit dem [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) des Namespace verglichen wird. Weitere Informationen zur Windows Sicherheit finden Sie unter [Zugriff auf sicherungsfähige WMI-Objekte.](access-to-wmi-securable-objects.md)

Beachten Sie, dass sich die [Benutzerkontensteuerung (User Account Control, UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ab Windows Vista auf den Zugriff auf WMI-Daten auswirkt und was mit dem [*WMI-Steuerelement*](gloss-w.md)konfiguriert werden kann. Weitere Informationen finden Sie unter [Standardberechtigungen für WMI-Namespaces](#default-permissions-on-wmi-namespaces) und [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

Der Zugriff auf WMI-Namespaces ist auch betroffen, wenn die Verbindung von einem Remotecomputer aus hergestellt wird. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer,](connecting-to-wmi-on-a-remote-computer.md)Sichern einer [WMI-Remoteverbindung](securing-a-remote-wmi-connection.md)und Herstellen einer [Verbindung über Windows Firewall.](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)

Anbieter müssen sich auf die Identitätswechseleinstellung für die Verbindung verlassen, um zu bestimmen, ob das Clientskript oder die Anwendung Daten empfangen soll. Weitere Informationen zu Skript- und Clientanwendungen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md). Weitere Informationen [](gloss-p.md) zum Anbieteridentitätswechsel finden Sie unter [Entwickeln eines WMI-Anbieters.](developing-a-wmi-provider.md)

## <a name="wmi-namespace-auditing"></a>WMI-Namespaceüberwachung

WMI verwendet die [*Namespace-Systemzugriffssteuerungslisten (System Access Control Lists, SACL),*](/windows/desktop/SecGloss/s-gly) um die Namespaceaktivität zu überwachen. Verwenden Sie zum Aktivieren der Überwachung von WMI-Namespaces die Registerkarte **Sicherheit** im [*WMI-Steuerelement,*](gloss-w.md) um die Überwachungseinstellungen für den Namespace zu ändern.

Die Überwachung ist während der Installation des Betriebssystems nicht aktiviert. Um die Überwachung zu aktivieren, klicken Sie im Fenster **Standardsicherheit** auf die Registerkarte **Überwachung.** Anschließend können Sie einen Überwachungseintrag hinzufügen.

Gruppenrichtlinie für den lokalen Computer muss so festgelegt werden, dass die Überwachung zugelassen wird. Sie können die Überwachung aktivieren, indem Sie das MMC-Snap-In Gpedit.msc ausführen und **den Zugriff auf Überwachungsobjekte** unter **Computerkonfiguration**  >  **Windows Einstellungen**  >  **Security Einstellungen** Local  >  **Policies**  >  **Audit Policy** festlegen.

Ein Überwachungseintrag bearbeitet die SACL des Namespace. Wenn Sie einen Überwachungseintrag hinzufügen, handelt es sich entweder um einen Benutzer, eine Gruppe, einen Computer oder einen integrierten Sicherheitsprinzipal. Nach dem Hinzufügen des Eintrags können Sie die Zugriffsvorgänge festlegen, die zu Sicherheitsprotokollereignissen führen. Beispielsweise können Sie für die Gruppe Authentifizierte Benutzer auf Methoden ausführen klicken. Diese Einstellung führt zu Sicherheitsprotokollereignissen, wenn ein Mitglied der Gruppe Authentifizierte Benutzer eine Methode in diesem Namespace ausführt. Die Ereignis-ID für WMI-Ereignisse lautet 4662.

Ihr Konto muss sich in der Gruppe Administratoren und unter erhöhten Rechten ausführen, um die Überwachungseinstellungen zu ändern. Das integrierte Administratorkonto kann auch die Sicherheit oder Überwachung für einen Namespace ändern. Weitere Informationen zur Ausführung im Modus mit erhöhten Rechten finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

Die WMI-Überwachung generiert Erfolgs- oder Fehlerereignisse für Versuche, auf WMI-Namespaces zuzugreifen. Der Dienst überwacht nicht den Erfolg oder Fehler von Anbietervorgängen. Wenn beispielsweise ein Skript eine Verbindung mit WMI und einem Namespace herstellt, kann es zu einem Fehler kommen, da das Konto, unter dem das Skript ausgeführt wird, keinen Zugriff auf diesen Namespace hat oder einen Vorgang wie das Bearbeiten der DACL versucht, der nicht gewährt wird.

Wenn Sie unter einem Konto in der Gruppe "Administratoren" ausführen, können Sie die Namespaceüberwachungsereignisse auf der **benutzeroberfläche Ereignisanzeige** anzeigen.

## <a name="types-of-namespace-events"></a>Typen von Namespaceereignissen

WMI verfolgt die folgenden Ereignistypen im Sicherheitsereignisprotokoll nach:

-   Überprüfung erfolgreich

    Der Vorgang muss zwei Schritte für einen erfolgreichen Überwachungsvorgang erfolgreich ausführen. Zunächst gewährt WMI zugriff auf die Clientanwendung oder das Skript basierend auf der Client-SID und der Namespace-DACL. Zweitens stimmt der angeforderte Vorgang mit den Zugriffsrechten im Namespace SACL für diesen Benutzer oder diese Gruppe überein.

-   Überwachungsfehler

    WMI verweigert den Zugriff auf den Namespace, aber der angeforderte Vorgang entspricht den Zugriffsrechten im Namespace SACL für diesen Benutzer oder diese Gruppe.

## <a name="namespace-access-settings"></a>Namespacezugriffs-Einstellungen

Sie können die Namespacezugriffsrechte für verschiedene Konten im WMI-Steuerelement anzeigen. Diese Konstanten werden unter [**NamespaceZugriffsrechtekonstanten**](namespace-access-rights-constants.md)beschrieben. Sie können den Zugriff auf einen WMI-Namespace mithilfe des WMI-Steuerelements oder programmgesteuert ändern. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](changing-access-security-on-securable-objects.md)

WMI überwacht Änderungen in allen Zugriffsberechtigungen, die in der folgenden Liste aufgeführt sind, mit Ausnahme der Remote enable-Berechtigung. Die Änderungen werden als Überwachungserfolg oder -fehler protokolliert, der der Berechtigung Sicherheit bearbeiten entspricht.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Methoden ausführen
</dt> <dd>

Ermöglicht dem Benutzer das Ausführen von Methoden, die für WMI-Klassen definiert sind. Entspricht der **WBEM \_ METHOD EXECUTE-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Vollständiger Schreibvorgang
</dt> <dd>

Ermöglicht den vollständigen Lese-, Schreib- und Löschzugriff auf WMI-Klassen und -Klasseninstanzen , sowohl statisch als auch dynamisch. Entspricht der **WBEM \_ FULL WRITE \_ REP-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Teilweiser Schreibvorgang
</dt> <dd>

Ermöglicht Schreibzugriff auf statische WMI-Klasseninstanzen. Entspricht der **WBEM \_ PARTIAL WRITE \_ REP-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Anbieterschreibvorgang
</dt> <dd>

Ermöglicht Schreibzugriff auf dynamische WMI-Klasseninstanzen. Entspricht der **WBEM \_ WRITE PROVIDER-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Konto aktivieren
</dt> <dd>

Ermöglicht Lesezugriff auf WMI-Klasseninstanzen. Entspricht der **WBEM ENABLE-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote aktivieren
</dt> <dd>

Ermöglicht den Zugriff auf den Namespace durch Remotecomputer. Entspricht der **WBEM \_ REMOTE ACCESS-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Lesen der Sicherheit
</dt> <dd>

Ermöglicht schreibgeschützten Zugriff auf DACL-Einstellungen. Entspricht der **READ CONTROL-Zugriffsberechtigungskonstante. \_**

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Sicherheit bearbeiten
</dt> <dd>

Ermöglicht schreibzugriff auf DACL-Einstellungen. Entspricht der SCHREIB-DAC-Zugriffsberechtigungskonstante. **\_**

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Standardberechtigungen für WMI-Namespaces

Die Standardsicherheitsgruppen sind:

-   Authentifizierte Benutzer
-   LOKALER DIENST
-   NETZWERKDIENST
-   Administratoren (auf dem lokalen Computer)

Die Standardzugriffsberechtigungen für authentifizierte Benutzer, LOCAL SERVICE und NETWORK SERVICE sind:

-   Methoden ausführen
-   Vollständiger Schreibzugriff
-   Konto aktivieren

Konten in der Gruppe Administratoren verfügen über alle verfügbaren Rechte, einschließlich der Bearbeitung von Sicherheitsbeschreibungen. Aufgrund der Benutzerkontensteuerung (User Account Control, UAC) muss das WMI-Steuerelement oder das Skript jedoch mit erhöhter Sicherheit ausgeführt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

Manchmal muss ein Skript oder eine Anwendung eine Administratorberechtigung wie **SeSecurityPrivilege** aktivieren, um einen Vorgang auszuführen. Beispielsweise kann ein Skript die [**GetSecurityDescriptor-Methode**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) der [**Win32-Druckerklasse \_**](/windows/desktop/CIMWin32Prov/win32-printer) ohne **SeSecurityPrivilege** ausführen und die Sicherheitsinformationen in der [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des Druckerobjektsicherheitsdeskriptors abrufen. [](/windows/desktop/SecGloss/s-gly) Die SACL-Informationen werden jedoch nur an das Skript zurückgegeben, wenn die **SeSecurityPrivilege-Berechtigung** für das Konto verfügbar und aktiviert ist. Wenn das Konto nicht über die Berechtigung verfügt, kann es nicht aktiviert werden. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge.](executing-privileged-operations.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
