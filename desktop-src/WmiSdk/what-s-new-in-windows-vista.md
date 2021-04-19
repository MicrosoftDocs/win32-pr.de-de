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
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="f318b-103">Neuerungen in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f318b-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="f318b-104">Ab Windows Vista enthält WMI viele neue Features, die auf Anforderungen von WMI-Benutzern basieren.</span><span class="sxs-lookup"><span data-stu-id="f318b-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="f318b-105">Neues Problem Behandlungs Tool</span><span class="sxs-lookup"><span data-stu-id="f318b-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="f318b-106">Neue Sicherheits Features in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f318b-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="f318b-107">Weitere neue Features in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f318b-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="f318b-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f318b-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="f318b-109">Neues Problem Behandlungs Tool</span><span class="sxs-lookup"><span data-stu-id="f318b-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="f318b-110">Ein neues Problem Behandlungs Tool steht zum Herunterladen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f318b-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="f318b-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI-Diagnosehilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="f318b-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="f318b-112">Dieses Hilfsprogramm überprüft den aktuellen Status des WMI-Dienstanbieter und zugehöriger Komponenten, DCOM-Einstellungen und Registrierungs Einstellungen auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="f318b-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="f318b-113">Das Hilfsprogramm meldet Probleme und bietet Vorschläge zur Reparatur.</span><span class="sxs-lookup"><span data-stu-id="f318b-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="f318b-114">Weitere Informationen und das Herunterladen des-Hilfsprogramms finden Sie unter [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span><span class="sxs-lookup"><span data-stu-id="f318b-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="f318b-115">Neue Sicherheits Features in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f318b-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="f318b-116">In der folgenden Liste sind die neuen WMI-Sicherheitsfeatures aufgeführt, die in Windows Vista verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f318b-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="f318b-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Ablauf Verfolgungs-und Protokollierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="f318b-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="f318b-118">Der WMI-Dienst verwendet nicht mehr die meisten [WMI-Protokolldateien](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="f318b-119">Stattdessen werden [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW) verwendet, und Ereignisse sind über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool wevtutil verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f318b-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="f318b-120">Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Festlegen der WMI-Namespace Sicherheit in der MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="f318b-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="f318b-122">Der **namespacesecuritysddl** -Qualifizierer kann zum Sichern beliebiger Namespaces verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f318b-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="f318b-123">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Sicherheitsüberwachung von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="f318b-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="f318b-125">WMI verwendet die-Namespace-System-Zugriffs Steuerungs Listen (SACL), um die Namespace Aktivität zu überwachen und Ereignisse an das Sicherheits Ereignisprotokoll zu melden.</span><span class="sxs-lookup"><span data-stu-id="f318b-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="f318b-126">Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md) und [Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get und Set Security Deskriptor Methods for Sicherungs fähigen Objects</span><span class="sxs-lookup"><span data-stu-id="f318b-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="f318b-128">Der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ dcomapplicationsetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)und [**\_ \_ SystemSecurity**](--systemsecurity.md)wurden neue Skript fähige Methoden zum erhalten und Festlegen von Sicherheits Deskriptoren hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f318b-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="f318b-129">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulieren von Sicherheits Deskriptoren in Skripts</span><span class="sxs-lookup"><span data-stu-id="f318b-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="f318b-131">Die [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse verfügt über Methoden, die es Skripts ermöglichen, binäre Sicherheits Deskriptoren für Sicherungs fähige Objekte in [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Objekte oder in [Sicherheits deskriptordefinitions](/windows/desktop/SecAuthZ/security-descriptor-definition-language) -Zeichen folgen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f318b-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="f318b-132">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="f318b-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="f318b-134">Die Benutzerkontensteuerung (User Account Control, UAC) wirkt sich auf die zurückgegebenen WMI-Daten, den Remote Zugriff und die Ausführung von Skripts aus.</span><span class="sxs-lookup"><span data-stu-id="f318b-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="f318b-135">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="f318b-136">Weitere Informationen zu UAC finden Sie unter [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="f318b-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="f318b-137">Weitere neue Features in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f318b-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="f318b-138">In der folgenden Liste sind die neuen WMI-Features aufgeführt, die in Windows Vista verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f318b-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="f318b-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Neue Leistungsdaten Anbieter</span><span class="sxs-lookup"><span data-stu-id="f318b-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="f318b-140">Der AutoDiscovery/AUTOPURGE-Prozess (ADAP) überträgt Leistungs Objekt Objekte nicht mehr in WMI-Leistungsklassen im WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="f318b-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="f318b-141">Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="f318b-142">Der [wmiperfclass-Anbieter](wmiperfclass-provider.md) erstellt die WMI-Leistungs Leistungs Ereignis Klassen.</span><span class="sxs-lookup"><span data-stu-id="f318b-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="f318b-143">Daten werden vom [WMIPerfInst-Anbieter](wmiperfinst-provider.md)dynamisch für diese WMI-Leistungsklassen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f318b-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer für Auflistungen</span><span class="sxs-lookup"><span data-stu-id="f318b-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="f318b-145">Die Methode " [**errbemubject. ItemIndex**](swbemobjectset-itemindex.md) " gibt das Objekt zurück, das einem angegebenen Index zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f318b-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="f318b-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Unterstützung für IPv6 und IPv4</span><span class="sxs-lookup"><span data-stu-id="f318b-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="f318b-147">WMI [-IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit.</span><span class="sxs-lookup"><span data-stu-id="f318b-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="f318b-148">Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.</span><span class="sxs-lookup"><span data-stu-id="f318b-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="f318b-149">Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Änderungen an Remote Verbindungen</span><span class="sxs-lookup"><span data-stu-id="f318b-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="f318b-151">Das Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer unter Windows Vista erfordert möglicherweise Änderungen an den Einstellungen für die [Windows-Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), die [Benutzerkontensteuerung](/previous-versions/aa905108(v=msdn.10))oder DCOM.</span><span class="sxs-lookup"><span data-stu-id="f318b-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="f318b-152">Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI ab Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Änderungen an der [ **Win32- \_ quickfixengineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="f318b-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="f318b-154">Für Systeme, die unter dem Betriebssystem Windows Vista und höher ausgeführt werden, gibt diese Klasse nur die von der komponentenbasierten Wartung (Component based Wartung, CBS) gelieferten Updates zurück.</span><span class="sxs-lookup"><span data-stu-id="f318b-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="f318b-155">Diese Updates sind nicht in der Registrierung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f318b-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="f318b-156">Von der Windows Installer (MSI) oder der [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) bereitgestellte Updates werden von der [**Win32- \_ quickfixengineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f318b-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Aktivieren und Deaktivieren einer NIC</span><span class="sxs-lookup"><span data-stu-id="f318b-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="f318b-158">[**Win32 \_ Network Adapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) verfügt über neue Methoden zum Aktivieren und Deaktivieren des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="f318b-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f318b-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Anbieter Änderungen</span><span class="sxs-lookup"><span data-stu-id="f318b-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="f318b-160">[**Win32 \_ Das Produkt**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) verfügt über neue Eigenschaften und Methoden, um weitere Daten über das Produkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f318b-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="f318b-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Neue Anzeige Monitor Klassen</span><span class="sxs-lookup"><span data-stu-id="f318b-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="f318b-162">[Monitor Anzeige Klassen](/windows/desktop/WmiCoreProv/wmi-core-provider-) enthalten Daten, die vom [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider) bereitgestellt werden, der Daten über Anzeige Monitore bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f318b-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="f318b-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Anbieter für Intelligent Platform-Verwaltungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f318b-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="f318b-164">Der WMI- [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) stellt Daten von Baseboard-Verwaltungs Controller (BMC)-Vorgängen für das Betriebssystem bereit.</span><span class="sxs-lookup"><span data-stu-id="f318b-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="f318b-165">Der Anbieter stellt Informationen an die Informations Klassen der Intelligent Platform-Verwaltung bereit, die Sensordaten und Daten des BMC-System Ereignis Protokolls (SEL) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f318b-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="f318b-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Erkennen von Hyperthreading und multikernprozessoren</span><span class="sxs-lookup"><span data-stu-id="f318b-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="f318b-167">[**Win32 \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) und [**Win32- \_ Prozessor**](/windows/desktop/CIMWin32Prov/win32-processor) verfügen über neue Eigenschaften, mit denen Sie Skripts schreiben können, um zu bestimmen, ob das Computersystem über mehr Kern-oder Hyperthreading-Prozessoren verfügt.</span><span class="sxs-lookup"><span data-stu-id="f318b-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="f318b-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Ereignismeldungen</span><span class="sxs-lookup"><span data-stu-id="f318b-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="f318b-169">Windows Vista verfügt über neue Ereignismeldungen.</span><span class="sxs-lookup"><span data-stu-id="f318b-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="f318b-170">Weitere Informationen finden Sie unter [WMI-Ereignisse](wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Bestands Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="f318b-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="f318b-172">Viele Hardware Klassen haben Änderungen vorgenommen, um die Hardware Inventur zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="f318b-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="f318b-173">Beispielsweise wurde [**Win32 \_ cdromdrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) und [**Win32 \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)eine Eigenschaft für die Seriennummer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f318b-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="f318b-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Neue Anbieter Hostingmodelle</span><span class="sxs-lookup"><span data-stu-id="f318b-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="f318b-175">Neue Anbieter-Hostingmodelle wurden für Windows Vista hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f318b-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="f318b-176">Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f318b-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f318b-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f318b-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f318b-178">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="f318b-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
