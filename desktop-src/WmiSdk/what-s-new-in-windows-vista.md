---
description: Ab Windows Vista enthält WMI viele neue Features, die auf Anforderungen von WMI-Benutzern basieren.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Neues in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47a2e63307004430099923d3d0a151ed9122b7fb96ff127c59145f1a911a1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553267"
---
# <a name="whats-new-in-windowsvista"></a>Neues in Windows Vista

Ab Windows Vista enthält WMI viele neue Features, die auf Anforderungen von WMI-Benutzern basieren.

-   [Neues Problembehandlungstool](#new-troubleshooting-tool)
-   [Neue Sicherheitsfunktionen in Windows Vista](#new-security-features-in-windows-vista)
-   [Weitere neue Features in Windows Vista](#other-new-features-in-windows-vista)
-   [Zugehörige Themen](#related-topics)

## <a name="new-troubleshooting-tool"></a>Neues Problembehandlungstool

Ein neues Problembehandlungstool steht zum Download zur Verfügung.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI-Diagnosehilfsprogramm
</dt> <dd>

Dieses Hilfsprogramm untersucht den aktuellen Status des WMI-Diensts und der zugehörigen Komponenten, DCOM-Einstellungen und Registrierungseinstellungen auf dem lokalen Computer. Das Hilfsprogramm meldet Probleme und bietet Vorschläge für die Reparatur. Weitere Informationen und zum Herunterladen des Hilfsprogramms finden Sie [unter WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Neue Sicherheitsfunktionen in Windows Vista

In der folgenden Liste sind die neuen WMI-Sicherheitsfeatures aufgeführt, die in Windows Vista verfügbar sind.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Ablaufverfolgung und Protokollierung von Ereignissen
</dt> <dd>

Der WMI-Dienst verwendet die meisten [WMI-Protokolldateien nicht mehr.](wmi-log-files.md) Stattdessen wird die [Ereignisablaufverfolgung](/windows/desktop/ETW/event-tracing-portal) (Event Tracing,  ETW) verwendet, und Ereignisse sind über Ereignisanzeige Benutzeroberfläche oder das Befehlszeilentool Wevtutil verfügbar. Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Festlegen der WMI-Namespacesicherheit in der MOF-Datei
</dt> <dd>

Der **NamespaceSecuritySDDL-Qualifizierer** kann zum Sichern beliebiger Namespaces verwendet werden. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit, wenn der Namespace erstellt wird.](setting-namespace-security-when-the-namespace-is-created.md)

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Sicherheitsüberwachung von WMI-Namespaces
</dt> <dd>

WMI verwendet die Namespacesystem-Zugriffssteuerungslisten (SACL), um Namespaceaktivitäten zu überwachen und Ereignisse an das Sicherheitsereignisprotokoll zu melden. Weitere Informationen finden Sie unter [Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md) und [Festlegen von Namespacesicherheitsdeskriptoren.](setting-namespace-security-descriptors.md)

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects (Sicherheitsdeskriptormethoden für sicherungsfähige Objekte erhalten und festlegen)
</dt> <dd>

[**Win32 \_ Printer, Win32**](/windows/desktop/CIMWin32Prov/win32-printer) [**\_ Service,**](/windows/desktop/CIMWin32Prov/win32-service) [**StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov) [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)und SystemSecurity wurden neue skriptfähige Methoden zum Erhalten und Festlegen von Sicherheitsdeskriptoren [**\_ \_ hinzugefügt.**](--systemsecurity.md) Weitere Informationen finden Sie unter [Changing Access Security on Securable Objects (Ändern der Zugriffssicherheit für sicherungsfähige Objekte).](changing-access-security-on-securable-objects.md)

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Bearbeiten von Sicherheitsbeschreibungen in Skripts
</dt> <dd>

Die [**Win32 \_ SecurityDescriptorHelper-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) verfügt über Methoden, mit denen Skripts binäre Sicherheitsbeschreibungen für sicherungsfähige Objekte in [**Win32 \_ SecurityDescriptor-Objekte**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) oder Zeichenfolgen der [Sicherheitsbeschreibungsdefinitionssprache](/windows/desktop/SecAuthZ/security-descriptor-definition-language) konvertieren können. Weitere Informationen finden Sie unter [Changing Access Security on Securable Objects (Ändern der Zugriffssicherheit für sicherungsfähige Objekte).](changing-access-security-on-securable-objects.md)

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Benutzerkontensteuerung
</dt> <dd>

Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich darauf aus, welche WMI-Daten zurückgegeben werden und wie Skripts ausgeführt werden müssen. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md) Weitere Informationen zur Benutzerkontensteuerung finden Sie unter Erste Schritte [mit Benutzerkontensteuerung auf Windows Vista.](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Weitere neue Features in Windows Vista

In der folgenden Liste sind neue WMI-Features aufgeführt, die in Windows Vista verfügbar sind.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Neue Leistungsindikatordatenanbieter
</dt> <dd>

Der Prozess AutoDiscovery/AutoPurge (ADAP) überträgt keine Leistungsindikatorobjekte mehr an WMI-Leistungsklassen im WMI-Repository. Weitere Informationen finden Sie unter [Leistungsbibliotheken und WMI.](performance-libraries-and-wmi.md) Der [WMIPerfClass-Anbieter](wmiperfclass-provider.md) erstellt die WMI-Leistungsindikatorklassen. Daten werden dynamisch vom [WMIPerfInst-Anbieter an diese WMI-Leistungsklassen bereitgestellt.](wmiperfinst-provider.md)

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer für Sammlungen
</dt> <dd>

Die [**SWbemObject.ItemIndex-Methode gibt**](swbemobjectset-itemindex.md) das einem angegebenen Index zugeordnete Objekt in eine Auflistung zurück.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Unterstützung für IPv6 und IPv4
</dt> <dd>

[WMI-IP-Routenanbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerkklassen geben Daten für IPv4-Adressen an. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen. Weitere Informationen finden Sie unter [IPv6- und IPv4-Unterstützung in WMI.](ipv6-and-ipv4-support-in-wmi.md)

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Änderungen an Remoteverbindungen
</dt> <dd>

Für das Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remotecomputer mit Windows Vista sind möglicherweise Änderungen an den Einstellungen für [Windows Firewall,](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)Benutzerkontensteuerung [oder](/previous-versions/aa905108(v=msdn.10))DCOM erforderlich. Weitere Informationen finden Sie unter [Herstellen einer Remoteverbindung mit WMI ab Vista.](connecting-to-wmi-remotely-starting-with-vista.md)

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Änderungen an [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

Für Systeme, die unter Windows Vista und höher ausgeführt werden, gibt diese Klasse nur die Updates zurück, die von der komponentenbasierten Wartung (Component Based Servicing, CBS) bereitgestellt werden. Diese Updates sind nicht in der Registrierung aufgeführt. Updates, die vom Windows Installer (MSI) oder dem [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) bereitgestellt werden, werden von [**Win32 \_ QuickFixEngineering nicht zurückgegeben.**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Aktivieren und Deaktivieren einer NIC
</dt> <dd>

[**Win32 \_ NetworkAdapter verfügt**](/windows/desktop/CIMWin32Prov/win32-networkadapter) über neue Methoden zum Aktivieren und Deaktivieren des Netzwerkadapters.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Änderungen des Installeranbieters
</dt> <dd>

[**Win32 \_ Das**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) Produkt verfügt über neue Eigenschaften und Methoden, um weitere Daten zum Produkt zur Verfügung zu stellen.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Neue Anzeigemonitorklassen
</dt> <dd>

[Monitor-Anzeigeklassen](/windows/desktop/WmiCoreProv/wmi-core-provider-) enthalten Daten, die vom [WDM-Anbieter bereitgestellt werden](/windows/desktop/WmiCoreProv/wdm-provider) und Daten zu Anzeigemonitoren enthalten.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface-Anbieter
</dt> <dd>

Der [WMI-IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) stellt Daten aus BMC-Vorgängen (Baseboard Management Controller) für das Betriebssystem zur Verfügung. Der Anbieter stellt Informationen für die Intelligent Platform Management Information Classes (Intelligent Platform Management Information Classes) zur Verfügung, die Sensordaten und BMC-Sel-Nachrichtendaten (System Event Log) bereitstellen.

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Erkennen von Hyperthreading- und Multicore-Prozessoren
</dt> <dd>

[**Win32 \_ ComputerSystem und**](/windows/desktop/CIMWin32Prov/win32-computersystem) [**Win32-Prozessor \_**](/windows/desktop/CIMWin32Prov/win32-processor) verfügen über neue Eigenschaften, mit denen Sie Skripts schreiben können, um zu bestimmen, ob das Computersystem über Mehrkern- oder Hyperthreadingprozessoren verfügt.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Ereignismeldungen
</dt> <dd>

Windows Vista verfügt über neue Ereignismeldungen. Weitere Informationen finden Sie unter [WMI-Ereignisse.](wmi-events.md)

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Bestandsverbesserungen
</dt> <dd>

Viele Hardwareklassen wurden geändert, um die Hardwareinventur zu verbessern. Beispielsweise wurde [**Win32 \_ CKILLDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) und [**Win32 DiskDrive eine \_ Seriennummerneigenschaft hinzugefügt.**](/windows/desktop/CIMWin32Prov/win32-diskdrive)

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Neue Anbieterhostingmodelle
</dt> <dd>

Neue Anbieterhostingmodelle wurden für Windows Vista hinzugefügt. Weitere Informationen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
