---
description: Neuerungen in Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Neuerungen in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682e4f125fcc11a1b6679af7df78fddba5a766ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369073"
---
# <a name="whats-new-in-windows-7"></a>Neuerungen in Windows 7

## <a name="new-security-feature-in-windows-7"></a>Neues Sicherheits Feature in Windows 7

Im folgenden finden Sie die neue WMI-Sicherheitsfunktion (Windows-Verwaltungsinstrumentation), die in Windows 7 verfügbar ist.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Steuern der Anbieter Sicherheit
</dt> <dd>

Änderungen zur Erhöhung der Sicherheit des WMI-freigegebenen Anbieter Host Prozesses (wmiprvse.exe). Durch diese Änderungen werden drei neue Gruppenrichtlinien und zwei laufende Modi für den freigegebenen WMI-Host eingeführt, die als sicherer und kompatibler Modus bezeichnet werden. Weitere Informationen finden Sie unter [Registrierungsschlüssel zum Steuern der Anbieter Sicherheit](registry-keys-for-controlling-provider-security-.md).

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Weitere neue oder aktualisierte Features in Windows 7

In der folgenden Liste sind die neuen WMI-Features aufgeführt, die in Windows 7 verfügbar sind.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>CIM-Schema Kompatibilität
</dt> <dd>

Ab Windows 7 ist WMI mit der Schema Version 2.17.1 des Common Information Model (CIM) kompatibel. Weitere Informationen finden Sie unter [CIM-Schema Kompatibilität](cim-schema-compatibility.md).

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Cross-Namespace Association Traversale
</dt> <dd>

WMI implementierte einen Standardmechanismus zum Ermitteln von Profilen mithilfe des CIM-Schemas. Weitere Informationen finden Sie unter [Cross Namespace Association Traversal](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Zuordnungs Anbieter
</dt> <dd>

Informationen zum Schreiben und Registrieren eines Zuordnungs Anbieters. Zuordnungs Anbieter werden verwendet, um Standardprofile wie ein Power Profile verfügbar zu machen. Weitere Informationen finden Sie unter [Schreiben eines Zuordnungs Anbieters für Interop](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Optionaler Funktionsstatus
</dt> <dd>

WMI hat die [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse implementiert. Mit dieser Klasse wird der Status der optionalen Features abgefragt und zurückgegeben, die auf einem Computer vorhanden sind. Beispiele für Abfragen, die Windows PowerShell verwenden, finden Sie Unterabfragen [des Status optionaler Features](querying-the-status-of-optional-features.md).

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Ändern des Standard Verhaltens für die autorestore-Repository-Funktion
</dt> <dd>

WMI verfügt über einen neuen Registrierungsschlüssel zum Aktivieren oder Deaktivieren des autorestore-Repository-Features. Weitere Informationen finden Sie unter [Registrierungsschlüssel für die Repository-Konfiguration](registry-key-for-repository-configuration.md).

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Neue Windows PowerShell-Befehls Klassen
</dt> <dd>

Windows PowerShell-Cmdlets ermöglichen es Benutzern, die End-to-End-Aufgaben abzuschließen, die zum Verwalten von lokalen Computern und Remote Computern notwendig sind. Weitere Informationen finden Sie unter [verwaltete Referenz für WMI-PowerShell-Befehls Klassen](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Neuer Mechanismus zum Herstellen einer Verbindung mit Remote Computern
</dt> <dd>

Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit WMI auf einem Remote Computer. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer mithilfe von PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Änderungen an den Software Lizenzierungs Klassen
</dt> <dd>

Die [Software Lizenzierungs Klassen](/previous-versions/windows/desktop/sppwmi/software-license-provider-) verfügen über neue Methoden und Eigenschaften, um mehr Software Lizenzierungs Daten bereitzustellen. Außerdem wurde die [**softwarelicensingdekenactivationlicense**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) -Klasse hinzugefügt.

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Neue Klassen für Energiemessung und Budgetierung
</dt> <dd>

[Energie Messungs-und Budgetierungs Klassen](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) sind die primäre Schnittstelle für die Abfrage von PMI-Informationen (Power Meter Interface) von den zugrunde liegenden Energiezählern des Systems.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Neue Power Policy-Klassen
</dt> <dd>

Mit [Energierichtlinien Klassen](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) wird die Remote Verwaltung aller Energierichtlinien Infrastrukturen ermöglicht.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Änderungen an der [**Win32 \_ Server Feature**](win32-serverfeature.md) -Klasse
</dt> <dd>

Die **ID** -Eigenschaft des [**Win32- \_ Server Features**](win32-serverfeature.md) wurde aktualisiert.

</dd> </dl>

Weitere Informationen zu neuen Features in früheren Betriebssystemversionen finden Sie unter Neuigkeiten [in Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
