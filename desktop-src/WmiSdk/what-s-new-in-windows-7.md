---
description: Neuerungen in Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Neuerungen in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000a3460366855df65096333a8b847a6d2c0c0a48a89c91f6791db3286d634fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502860"
---
# <a name="whats-new-in-windows-7"></a>Neuerungen in Windows 7

## <a name="new-security-feature-in-windows-7"></a>Neues Sicherheitsfeature in Windows 7

Im Folgenden werden die neuen Sicherheitsfeatures für Windows Management Instrumentation (WMI) aufgeführt, die in Windows 7 verfügbar sind.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Steuern der Anbietersicherheit
</dt> <dd>

Änderungen zur Verbesserung der Sicherheit des Hostprozesses für freigegebene WMI-Anbieter (wmiprvse.exe). Diese Änderungen führen drei neue Gruppenrichtlinien und zwei Ausführungsmodi für den freigegebenen WMI-Host ein, die als sichere und kompatible Modi bezeichnet werden. Weitere Informationen finden Sie unter [Registrierungsschlüssel zum Steuern der Anbietersicherheit.](registry-keys-for-controlling-provider-security-.md)

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Andere neue oder aktualisierte Features in Windows 7

In der folgenden Liste sind die neuen WMI-Features aufgeführt, die in Windows 7 verfügbar sind.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>CIM-Schemakompatibilität
</dt> <dd>

Ab Windows 7 ist WMI mit der cim-Schemaversion 2.17.1 (Common Information Model) kompatibel. Weitere Informationen finden Sie unter [CIM-Schemakompatibilität.](cim-schema-compatibility.md)

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Namespaceübergreifender Zuordnungsdurchlauf
</dt> <dd>

WMI hat einen Standardmechanismus zum Ermitteln von Profilen mithilfe des CIM-Schemas implementiert. Weitere Informationen finden Sie unter [Namespaceübergreifender Zuordnungsdurchlauf.](cross-namespace-association-traversal.md)

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Zuordnungsanbieter
</dt> <dd>

Informationen zum Schreiben und Registrieren eines Zuordnungsanbieters. Zuordnungsanbieter werden verwendet, um Standardprofile verfügbar zu machen, z. B. ein Energieprofil. Weitere Informationen finden Sie unter [Schreiben eines Zuordnungsanbieters für Interop.](writing-an-association-provider-for-interop.md)

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Optionaler Featurestatus
</dt> <dd>

WMI hat die [**Win32 \_ OptionalFeature-Klasse**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) implementiert. Diese Klasse fragt den Status der optionalen Features ab, die auf einem Computer vorhanden sind, und gibt diesen zurück. Beispielabfragen mit Windows PowerShell finden Sie unter [Abfragen des Status optionaler Features.](querying-the-status-of-optional-features.md)

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Ändern des Standardverhaltens für das AutoRestore-Repositoryfeature
</dt> <dd>

WMI verfügt über einen neuen Registrierungsschlüssel zum Aktivieren oder Deaktivieren des AutoRestore-Repositoryfeatures. Weitere Informationen finden Sie unter [Registrierungsschlüssel für die Repositorykonfiguration.](registry-key-for-repository-configuration.md)

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Neue Windows PowerShell-Befehlsklassen
</dt> <dd>

Windows PowerShell Cmdlets ermöglichen Es Benutzern, die End-to-End-Aufgaben auszuführen, die zum Verwalten lokaler und Remotecomputer erforderlich sind. Weitere Informationen finden Sie unter [Verwaltete Referenz für WMI PowerShell-Befehlsklassen.](managed-reference-for-wmi-powershell-command-classes.md)

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Neuer Mechanismus zum Herstellen einer Verbindung mit Remotecomputern
</dt> <dd>

Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit WMI auf einem Remotecomputer. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer mithilfe von PowerShell.](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Änderungen an den Softwarelizenzklassen
</dt> <dd>

Die [Softwarelizenzierungsklassen](/previous-versions/windows/desktop/sppwmi/software-license-provider-) verfügen über neue Methoden und Eigenschaften, um mehr Softwarelizenzierungsdaten bereitzustellen. Darüber hinaus wurde die [**SoftwareLicensingTokenActivationLicense-Klasse**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) hinzugefügt.

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Neue Leistungsmessungs- und Budgetierungsklassen
</dt> <dd>

[Leistungsmessungs- und Budgetierungsklassen](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) sind die primäre Schnittstelle für die Abfrage von PMI-Informationen (Power Meter Interface) von zugrunde liegenden Stromzählern im System.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Neue Energierichtlinienklassen
</dt> <dd>

[Energierichtlinienklassen](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) ermöglichen die Remoteverwaltung aller Energierichtlinieninfrastrukturen.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Änderungen an der [**Win32 \_ ServerFeature-Klasse**](win32-serverfeature.md)
</dt> <dd>

Die **ID-Eigenschaft** von [**Win32 \_ ServerFeature**](win32-serverfeature.md) wurde aktualisiert.

</dd> </dl>

Weitere Informationen zu neuen Features in früheren Betriebssystemversionen finden Sie unter [Neuerungen in Windows Vista.](what-s-new-in-windows-vista.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
