---
description: WMI verwendet einen standardmäßigen Windows-Sicherheits Deskriptor, um den Zugriff auf WMI-Namespaces zu steuern.
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
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960621"
---
# <a name="access-to-wmi-namespaces"></a>Zugriff auf WMI-Namespaces

WMI verwendet einen standardmäßigen Windows- *Sicherheits Deskriptor* , um den Zugriff auf WMI-Namespaces zu steuern. Wenn Sie eine Verbindung mit WMI herstellen, indem Sie entweder den WMI-Moniker "winmgmts" oder einen Aufruf an " [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) " oder " [**Swap. ConnectServer**](swbemlocator-connectserver.md)" aufrufen, stellen Sie eine Verbindung mit einem bestimmten Namespace her.

Die folgenden Informationen werden in diesem Thema behandelt:

-   [WMI-Namespace Sicherheit](#wmi-namespace-security)
-   [WMI-Namespace Überwachung](#wmi-namespace-auditing)
-   [Typen von Namespace Ereignissen](#types-of-namespace-events)
-   [Namespace-Zugriffs Einstellungen](#namespace-access-settings)
-   [Standard Berechtigungen für WMI-Namespaces](#default-permissions-on-wmi-namespaces)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-namespace-security"></a>WMI-Namespace Sicherheit

WMI verwaltet die Namespace Sicherheit, indem das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Benutzers, der eine Verbindung mit dem-Namespace herstellt, mit der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des-Namespace verglichen wird. Weitere Informationen zur Windows-Sicherheit finden [Sie unter Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).

Beachten Sie, dass sich die [Benutzerkontensteuerung (User Account Control, UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ab Windows Vista auf den Zugriff auf WMI-Daten auswirkt und was mit dem [*WMI-Steuer*](gloss-w.md)Element konfiguriert werden kann. Weitere Informationen finden Sie unter [Standard Berechtigungen für WMI-Namespaces](#default-permissions-on-wmi-namespaces) und [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

Der Zugriff auf WMI-Namespaces wird ebenfalls beeinträchtigt, wenn die Verbindung von einem Remote Computer aus erfolgt. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md)und Herstellen einer [Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Anbieter müssen sich auf die Identitätswechsel Einstellung für die Verbindung verlassen, um zu bestimmen, ob das Client Skript oder die Anwendung Daten empfangen soll. Weitere Informationen zu Skript-und Client Anwendungen finden Sie unter [Festlegen der Prozesssicherheit für Client](setting-client-application-process-security.md)Anwendungen. Weitere Informationen zum Identitätswechsel des [*Anbieters*](gloss-p.md) finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).

## <a name="wmi-namespace-auditing"></a>WMI-Namespace Überwachung

WMI verwendet zum Überwachen der Namespace Aktivität die-Namespace [*System-Zugriffs Steuerungs Listen (SACL)*](/windows/desktop/SecGloss/s-gly) . Um die Überwachung von WMI-Namespaces zu aktivieren, verwenden Sie die Registerkarte **Sicherheit** des [*WMI-Steuer*](gloss-w.md) Elements, um die Überwachungs Einstellungen für den-Namespace zu ändern.

Die Überwachung wird während der Installation des Betriebssystems nicht aktiviert. Um die Überwachung zu aktivieren, klicken Sie im Fenster Standard **Sicherheit** auf **die Registerkarte** Überwachung. Anschließend können Sie einen Überwachungs Eintrag hinzufügen.

Gruppenrichtlinie für den lokalen Computer muss so festgelegt werden, dass die Überwachung zugelassen wird. Sie können die Überwachung aktivieren, indem Sie das MMC-Snap-in "gpeer dit. msc" und " **Objektzugriff** überwachen" unter **Computer Konfiguration**  >  **Windows-Einstellungen**  >  **Sicherheitseinstellungen**  >  **lokale Richtlinien** Überwachungs  >  **Richtlinie** festlegen.

Ein Überwachungs Eintrag bearbeitet die SACL des Namespace. Wenn Sie einen Überwachungs Eintrag hinzufügen, handelt es sich entweder um einen Benutzer, eine Gruppe, einen Computer oder einen integrierten Sicherheits Prinzipal. Nachdem Sie den Eintrag hinzugefügt haben, können Sie die Zugriffs Vorgänge festlegen, die zu Sicherheitsprotokoll Ereignissen führen. Beispielsweise können Sie für die Gruppe Authentifizierte Benutzer auf Methoden ausführen klicken. Diese Einstellung führt zu Sicherheitsprotokoll Ereignissen, wenn ein Mitglied der Gruppe "authentifizierte Benutzer" eine Methode in diesem Namespace ausführt. Die Ereignis-ID für WMI-Ereignisse lautet 4662.

Ihr Konto muss sich in der Gruppe "Administratoren" befinden und mit erhöhten Rechten ausgeführt werden, um die Überwachungs Einstellungen zu ändern. Das integrierte Administrator Konto kann auch die Sicherheit oder die Überwachung für einen Namespace ändern. Weitere Informationen zur Ausführung im erweiterten Modus finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

Die WMI-Überwachung generiert Erfolgs-oder Fehlerereignisse für Zugriffsversuche auf WMI-Namespaces. Der Dienst überwacht nicht den Erfolg oder das Fehlschlagen von Anbieter Vorgängen. Wenn ein Skript z. b. eine Verbindung mit WMI und einem Namespace herstellt, kann dies fehlschlagen, weil das Konto, unter dem das Skript ausgeführt wird, keinen Zugriff auf den Namespace hat oder einen Vorgang, z. b. das Bearbeiten der DACL, nicht gestattet, das nicht erteilt wurde.

Wenn Sie unter einem Konto der Gruppe "Administratoren" ausgeführt werden, können Sie die Namespace-Überwachungs Ereignisse auf der **Ereignisanzeige** -Benutzeroberfläche anzeigen.

## <a name="types-of-namespace-events"></a>Typen von Namespace Ereignissen

WMI verfolgt die folgenden Ereignis Typen im Sicherheits Ereignisprotokoll:

-   Überprüfung erfolgreich

    Der Vorgang muss zwei Schritte für eine erfolgreiche Überprüfung ausführen. Zuerst ermöglicht WMI den Zugriff auf die Client Anwendung oder das Skript basierend auf der Client-sid und der Namespace-DACL. Zweitens entspricht der angeforderte Vorgang den Zugriffsrechten in der Namespace-SACL für diesen Benutzer bzw. diese Gruppe.

-   Überwachungs Fehler

    WMI verweigert den Zugriff auf den-Namespace, aber der angeforderte Vorgang entspricht den Zugriffsrechten in der Namespace-SACL für diesen Benutzer bzw. diese Gruppe.

## <a name="namespace-access-settings"></a>Namespace-Zugriffs Einstellungen

Sie können die Namespace-Zugriffsrechte für verschiedene Konten auf dem WMI-Steuerelement anzeigen. Diese Konstanten werden unter [**Namespace-Zugriffsrechte Konstanten**](namespace-access-rights-constants.md)beschrieben. Sie können den Zugriff auf einen WMI-Namespace mithilfe des WMI-Steuer Elements oder Programm gesteuert ändern. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

WMI überwacht Änderungen in allen Zugriffsberechtigungen, die in der folgenden Liste aufgeführt sind, mit Ausnahme der Berechtigung "Remote Aktivierung". Die Änderungen werden als Überwachungs Erfolg oder Fehler protokolliert, der der Berechtigung zum Bearbeiten der Sicherheit entspricht.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Methoden ausführen
</dt> <dd>

Ermöglicht dem Benutzer das Ausführen von Methoden, die in WMI-Klassen definiert sind. Entspricht der **WBEM- \_ Methode \_ Execute** Access-Berechtigungs Konstante.

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Vollständiger Schreibzugriff
</dt> <dd>

Ermöglicht den vollständigen Lese-, Schreib-und Lösch Zugriff auf WMI-Klassen und-Klassen Instanzen (statisch und dynamisch). Entspricht der Berechtigungs Konstante für den **\_ vollständigen \_ Schreib \_ Zugriff von WBEM** .

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partieller Schreibvorgang
</dt> <dd>

Ermöglicht den Schreibzugriff auf statische WMI-Klassen Instanzen. Entspricht der Zugriffs Berechtigungs Konstante für **\_ partielle \_ Schreib \_ Vorgänge von WBEM** .

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Anbieter Schreibvorgang
</dt> <dd>

Ermöglicht den Schreibzugriff auf dynamische WMI-Klassen Instanzen. Entspricht der Zugriffs Berechtigungs Konstante für den **WBEM- \_ Schreib \_ Anbieter** .

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Konto aktivieren
</dt> <dd>

Ermöglicht den Lesezugriff auf WMI-Klassen Instanzen. Entspricht der Berechtigung zum Aktivieren der Zugriffsberechtigung für **WBEM \_** .

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Aktivierung
</dt> <dd>

Ermöglicht den Zugriff auf den-Namespace durch Remote Computer. Entspricht der Zugriffs Berechtigungs Konstante für den WBEM-RAS-Zugriff **\_ \_** .

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sicherheit lesen
</dt> <dd>

Ermöglicht den schreibgeschützten Zugriff auf DACL-Einstellungen. Entspricht der Konstante für den **Lese \_** Zugriff auf die Zugriffsberechtigung.

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Sicherheit bearbeiten
</dt> <dd>

Ermöglicht Schreibzugriff auf DACL-Einstellungen. Entspricht der Konstante zum **Schreiben der \_ DAC** -Zugriffsberechtigung.

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Standard Berechtigungen für WMI-Namespaces

Die Standard Sicherheitsgruppen lauten:

-   Authentifizierte Benutzer
-   LOKALER DIENST
-   NETZWERKDIENST
-   Administratoren (auf dem lokalen Computer)

Die Standard Zugriffsberechtigungen für die authentifizierten Benutzer, den lokalen Dienst und den Netzwerkdienst lauten:

-   Methoden ausführen
-   Vollständiger Schreibzugriff
-   Konto aktivieren

Konten in der Gruppe "Administratoren" sind alle Rechte verfügbar, einschließlich der Bearbeitung von Sicherheits Deskriptoren. Aufgrund der Benutzerkontensteuerung (User Account Control, UAC) muss das WMI-Steuerelement oder das Skript jedoch mit erhöhter Sicherheit ausgeführt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

Manchmal muss ein Skript oder eine Anwendung eine Administrator Berechtigung, wie z. b. **SeSecurityPrivilege**, aktivieren, um einen Vorgang auszuführen. Ein Skript kann z. b. die [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) -Methode der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse ohne **SeSecurityPrivilege** ausführen und die Sicherheitsinformationen in der freigegebenen [*Zugriffs Steuerungs Liste (DACL)*](/windows/desktop/SecGloss/d-gly) der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)des Drucker Objekts abrufen. Die SACL-Informationen werden jedoch nur dann an das Skript zurückgegeben, wenn die **SeSecurityPrivilege** -Berechtigung verfügbar ist und für das Konto aktiviert ist. Wenn für das Konto nicht die Berechtigung verfügbar ist, kann es nicht aktiviert werden. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
