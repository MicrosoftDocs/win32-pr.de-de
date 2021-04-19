---
description: Ab Windows Vista enthält WMI viele neue Features, die auf Anforderungen von WMI-Benutzern basieren.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Neuerungen in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350150"
---
# <a name="whats-new-in-windowsvista"></a>Neuerungen in Windows Vista

Ab Windows Vista enthält WMI viele neue Features, die auf Anforderungen von WMI-Benutzern basieren.

-   [Neues Problem Behandlungs Tool](#new-troubleshooting-tool)
-   [Neue Sicherheits Features in Windows Vista](#new-security-features-in-windows-vista)
-   [Weitere neue Features in Windows Vista](#other-new-features-in-windows-vista)
-   [Zugehörige Themen](#related-topics)

## <a name="new-troubleshooting-tool"></a>Neues Problem Behandlungs Tool

Ein neues Problem Behandlungs Tool steht zum Herunterladen zur Verfügung.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI-Diagnosehilfsprogramm
</dt> <dd>

Dieses Hilfsprogramm überprüft den aktuellen Status des WMI-Dienstanbieter und zugehöriger Komponenten, DCOM-Einstellungen und Registrierungs Einstellungen auf dem lokalen Computer. Das Hilfsprogramm meldet Probleme und bietet Vorschläge zur Reparatur. Weitere Informationen und das Herunterladen des-Hilfsprogramms finden Sie unter [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Neue Sicherheits Features in Windows Vista

In der folgenden Liste sind die neuen WMI-Sicherheitsfeatures aufgeführt, die in Windows Vista verfügbar sind.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Ablauf Verfolgungs-und Protokollierungs Ereignisse
</dt> <dd>

Der WMI-Dienst verwendet nicht mehr die meisten [WMI-Protokolldateien](wmi-log-files.md). Stattdessen werden [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW) verwendet, und Ereignisse sind über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool wevtutil verfügbar. Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Festlegen der WMI-Namespace Sicherheit in der MOF-Datei
</dt> <dd>

Der **namespacesecuritysddl** -Qualifizierer kann zum Sichern beliebiger Namespaces verwendet werden. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Sicherheitsüberwachung von WMI-Namespaces
</dt> <dd>

WMI verwendet die-Namespace-System-Zugriffs Steuerungs Listen (SACL), um die Namespace Aktivität zu überwachen und Ereignisse an das Sicherheits Ereignisprotokoll zu melden. Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md) und [Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get und Set Security Deskriptor Methods for Sicherungs fähigen Objects
</dt> <dd>

Der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ dcomapplicationsetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)und [**\_ \_ SystemSecurity**](--systemsecurity.md)wurden neue Skript fähige Methoden zum erhalten und Festlegen von Sicherheits Deskriptoren hinzugefügt. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulieren von Sicherheits Deskriptoren in Skripts
</dt> <dd>

Die [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse verfügt über Methoden, die es Skripts ermöglichen, binäre Sicherheits Deskriptoren für Sicherungs fähige Objekte in [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Objekte oder in [Sicherheits deskriptordefinitions](/windows/desktop/SecAuthZ/security-descriptor-definition-language) -Zeichen folgen zu konvertieren. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Benutzerkontensteuerung
</dt> <dd>

Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die zurückgegebenen WMI-Daten, den Remote Zugriff und die Ausführung von Skripts aus. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md). Weitere Informationen zu UAC finden Sie unter [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Weitere neue Features in Windows Vista

In der folgenden Liste sind die neuen WMI-Features aufgeführt, die in Windows Vista verfügbar sind.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Neue Leistungsdaten Anbieter
</dt> <dd>

Der AutoDiscovery/AUTOPURGE-Prozess (ADAP) überträgt Leistungs Objekt Objekte nicht mehr in WMI-Leistungsklassen im WMI-Repository. Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md). Der [wmiperfclass-Anbieter](wmiperfclass-provider.md) erstellt die WMI-Leistungs Leistungs Ereignis Klassen. Daten werden vom [WMIPerfInst-Anbieter](wmiperfinst-provider.md)dynamisch für diese WMI-Leistungsklassen bereitgestellt.

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer für Auflistungen
</dt> <dd>

Die Methode " [**errbemubject. ItemIndex**](swbemobjectset-itemindex.md) " gibt das Objekt zurück, das einem angegebenen Index zugeordnet ist.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Unterstützung für IPv6 und IPv4
</dt> <dd>

WMI [-IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen. Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md).

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Änderungen an Remote Verbindungen
</dt> <dd>

Das Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer unter Windows Vista erfordert möglicherweise Änderungen an den Einstellungen für die [Windows-Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), die [Benutzerkontensteuerung](/previous-versions/aa905108(v=msdn.10))oder DCOM. Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI ab Vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Änderungen an der [ **Win32- \_ quickfixengineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

Für Systeme, die unter dem Betriebssystem Windows Vista und höher ausgeführt werden, gibt diese Klasse nur die von der komponentenbasierten Wartung (Component based Wartung, CBS) gelieferten Updates zurück. Diese Updates sind nicht in der Registrierung aufgeführt. Von der Windows Installer (MSI) oder der [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) bereitgestellte Updates werden von der [**Win32- \_ quickfixengineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)nicht zurückgegeben.

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Aktivieren und Deaktivieren einer NIC
</dt> <dd>

[**Win32 \_ Network Adapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) verfügt über neue Methoden zum Aktivieren und Deaktivieren des Netzwerkadapters.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Anbieter Änderungen
</dt> <dd>

[**Win32 \_ Das Produkt**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) verfügt über neue Eigenschaften und Methoden, um weitere Daten über das Produkt bereitzustellen.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Neue Anzeige Monitor Klassen
</dt> <dd>

[Monitor Anzeige Klassen](/windows/desktop/WmiCoreProv/wmi-core-provider-) enthalten Daten, die vom [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider) bereitgestellt werden, der Daten über Anzeige Monitore bereitstellt.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Anbieter für Intelligent Platform-Verwaltungs Schnittstellen
</dt> <dd>

Der WMI- [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) stellt Daten von Baseboard-Verwaltungs Controller (BMC)-Vorgängen für das Betriebssystem bereit. Der Anbieter stellt Informationen an die Informations Klassen der Intelligent Platform-Verwaltung bereit, die Sensordaten und Daten des BMC-System Ereignis Protokolls (SEL) bereitstellen.

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Erkennen von Hyperthreading und multikernprozessoren
</dt> <dd>

[**Win32 \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) und [**Win32- \_ Prozessor**](/windows/desktop/CIMWin32Prov/win32-processor) verfügen über neue Eigenschaften, mit denen Sie Skripts schreiben können, um zu bestimmen, ob das Computersystem über mehr Kern-oder Hyperthreading-Prozessoren verfügt.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Ereignismeldungen
</dt> <dd>

Windows Vista verfügt über neue Ereignismeldungen. Weitere Informationen finden Sie unter [WMI-Ereignisse](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Bestands Verbesserungen
</dt> <dd>

Viele Hardware Klassen haben Änderungen vorgenommen, um die Hardware Inventur zu verbessern. Beispielsweise wurde [**Win32 \_ cdromdrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) und [**Win32 \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)eine Eigenschaft für die Seriennummer hinzugefügt.

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Neue Anbieter Hostingmodelle
</dt> <dd>

Neue Anbieter-Hostingmodelle wurden für Windows Vista hinzugefügt. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
