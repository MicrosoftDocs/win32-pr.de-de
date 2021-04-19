---
description: Die Windows-Verwaltungsinfrastruktur (WMI), die Verwaltungs Instrumentation (Mi) und die Open Management Infrastructure (OMI) verwenden alle Management Object Format (MOF)-Dateien, um die Informationen zu beschreiben, die von den jeweiligen Anbietern zur Verfügung gestellt werden.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: WMI/MI/OMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369906"
---
# <a name="wmimiomi-providers"></a><span data-ttu-id="dfd1f-103">WMI/MI/OMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="dfd1f-103">WMI/MI/OMI Providers</span></span>

<span data-ttu-id="dfd1f-104">Die Windows-Verwaltungsinfrastruktur (WMI), die Verwaltungs Instrumentation (Mi) und die Open Management Infrastructure (OMI) verwenden alle Management Object Format (MOF)-Dateien, um die Informationen zu beschreiben, die von den jeweiligen Anbietern zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-104">Windows Management Infrastructure (WMI), Management Instrumentation (MI) and Open Management Infrastructure (OMI) all use Management Object Format (MOF) files to describe the information made available through their respective providers.</span></span>

<dl> <dt>

<span data-ttu-id="dfd1f-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-106">Der Active Directory-Anbieter, der auch als Verzeichnisdienste (DS)-Anbieter bezeichnet wird, ordnet Active Directory Objekte WMI zu.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-106">The Active Directory provider, also known as the Directory Services (DS) provider, maps Active Directory objects to WMI.</span></span> <span data-ttu-id="dfd1f-107">Durch den Zugriff auf den LDAP-Namespace (Lightweight Directory Access Protocol) in WMI können Sie in der Active Directory auf einen Alias verweisen oder ein Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-107">By accessing the Lightweight Directory Access Protocol (LDAP) namespace in WMI, you can reference or make an object an alias in the Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Anwendungs Inventur](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Application Inventory](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-109">Die WMI-Klassen für die Anwendungs Inventur ermöglichen die Ermittlung der installierten Win32-Anwendungen und Windows Store-Anwendungen auf einem Windows-System.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-109">The WMI classes for Application Inventory enable discovery of the installed Win32 applications and Windows store applications on a Windows system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Anwendungs Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-111">Der Anwendungs Proxy-WMI-Anbieter ermöglicht Entwicklern den Zugriff auf den webanwendungsproxy-Dienst, damit Administratoren Anwendungen für den externen Zugriff veröffentlichen können</span><span class="sxs-lookup"><span data-stu-id="dfd1f-111">Application Proxy WMI Provider enables developers to access the Web Application Proxy service so administrators can publish applications for external access.</span></span> <span data-ttu-id="dfd1f-112">Der webanwendungsproxy ist ein Reverseproxy für Active Directory-Verbunddienste (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-112">Web Application Proxy is a reverse proxy for Active Directory Federation Services (AD FS).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker-Laufwerkverschlüsselung (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker Drive Encryption (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-114">Bietet eine Konfiguration und Verwaltung für einen Speicherbereich auf einem Festplattenlaufwerk, das durch eine Instanz von [**Win32 \_ verschlüsseltablevolume**](/windows/desktop/SecProv/win32-encryptablevolume)dargestellt wird, die mithilfe der Verschlüsselung geschützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-114">Provides configuration and management for an area of storage on a hard disk drive, represented by an instance of [**Win32\_EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), that can be protected by using encryption.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-115"><span id="BITS"></span><span id="bits"></span>[Bohrer](/previous-versions/windows/desktop/bitsprov/bits-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-115"><span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-116">Der Background Intelligent Transfer Service (Bits) Compact Server mit Bits-Remote Verwaltung ermöglicht es authentifizierten Administratoren oder Controller Anwendungen, Bits-Übertragungs Aufträge Remote zu erstellen, zu ändern und zu verwalten, ohne den Internetinformationsdienste (IIS)-Dienst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-116">The Background Intelligent Transfer Service (BITS) Compact Server with BITS Remote Management allows authenticated administrators or controller applications to create, modify and manage BITS transfer jobs remotely without using the Internet Information Services (IIS) service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-118">Bietet Zugriff auf die BizTalk-Verwaltungs Objekte, die durch WMI-Klassen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-118">Supplies access to the BizTalk administration objects represented by WMI classes.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Startkonfigurationsdaten](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Boot Configuration Data](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-120">Der Startkonfigurationsdaten (BCD)-Anbieter stellt einen Speicher bereit, der zum Beschreiben von Start Anwendungen und Start Anwendungseinstellungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-120">The Boot Configuration Data (BCD) provider provides a store that is used to describe boot applications and boot application settings.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Start Ereignis Sammler](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Boot Event Collector](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-122">Der WMI-Anbieter des Start Ereignis Sammlers ermöglicht den Zugriff auf Verbindungs-und Konfigurationsinformationen für das Setup-und Start Ereignis Sammlungs Feature unter Windows Server.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-122">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[Cimwin32, Win32, Energie Verwaltungs Ereignisse](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Power Management Events](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-124">Die cimwin32-Anbieter unterstützen die in CimWin32.dll implementierten Klassen und bestehen aus den Core-CIM-Klassen, der Win32-Implementierung dieser Klassen und den Energie Verwaltungs Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-124">The CIMWin32 providers support the classes implemented in CimWin32.dll, and consist of the core CIM classes, the Win32 implementation of those classes, and power management events.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-126">Der CIMWin32a-Anbieter erweitert die im [cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)verfügbaren Klassen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-126">The CIMWin32a provider extends the classes available in the [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[Dcbqoscim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-128">Der dcbqoscim-Anbieter unterstützt Klassen, die Einstellungsdaten für Netzwerk-QoS, Steuerungs Einstellungsdaten und Datenverkehrs Klassen-Einstellungsdaten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-128">The DcbQosCim provider supports classes that describe Network QOS setting data, control setting data, and traffic class setting data.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Verteiltes Dateisystem (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Distributed File System (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-130">Der DFS-Anbieter stellt mithilfe von WMI Skript fähige-DFS-Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-130">The DFS provider supplies scriptable DFS functions through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Verteiltes Dateisystem Replikation (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-132">Erstellt Tools zum Konfigurieren und Überwachen des [verteiltes Dateisystem (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-132">Creates tools for configuring and monitoring the [Distributed File System (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) service.</span></span> <span data-ttu-id="dfd1f-133">Weitere Informationen finden Sie unter [DFSR-WMI-Klassen](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-133">For more information, see [DFSR WMI Classes](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-135">Der [dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) -Anbieter unterstützt Klassen, die den DFS-Namespace Zugriff implementieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-135">The [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) provider supports classes that implement DFS namespace access.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[Dhcpserverpsprovider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-137">Der [dhcpserverpsprovider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) -Anbieter unterstützt Klassen, die mit einem DHCP-Server (Dynamic Host Configuration Protocol) interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-137">The [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) provider supports classes that interact with a dynamic host configuration protocol (DHCP) server.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Datenträger Kontingent](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Disk Quota](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-139">Mithilfe des Windows-Datenträger Kontingent Anbieters können Administratoren die Datenmenge steuern, die von den einzelnen Benutzern in einem NTFS-Dateisystem gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-139">The Windows Disk Quota provider allows administrators to control the amount of data that each user stores on an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-141">Der DTC-Anbieter ermöglicht die Verwaltung des DTC.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-141">The DTC provider enables management of the DTC.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-142"><span id="DNS"></span><span id="dns"></span>[DNS-](/windows/desktop/DNS/dns-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-142"><span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-143">Ermöglicht es Administratoren und Programmierern, Domain Name System (DNS)-Ressourcen Einträge (RRS) und DNS-Server mithilfe von WMI zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-143">Enables administrators and programmers to configure Domain Name System (DNS) resource records (RRs) and DNS Servers using WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim-Anbieter Klassen](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim Provider Classes](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-145">Der dnsclientcim-Anbieter unterstützt Klassen, die mit einem DNS-Client (Domain Name System) interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-145">The Dnsclientcim provider supports classes that interact with a Domain Name System (DNS) client.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[Dnsclientpsprovider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-147">Der [dnsclientpsprovider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) -Anbieter unterstützt WMI-Klassen, die mit einem DNS-Client interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-147">The [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) provider supports WMI classes that interact with a DNS client.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[Dnsserverpsprovider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-149">Der [dnsserverpsprovider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) -Anbieter unterstützt WMI-Klassen, die mit einem DNS-Server interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-149">The [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) provider supports WMI classes that interact with a DNS server.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-151">Der [Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider) Anbieter bietet Zugriff auf Daten aus dem Ereignisprotokoll Dienst und Benachrichtigungen über Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-151">The [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supplies access to data from the event log service, and notification of events.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Verwaltung der Ereignis Ablauf Verfolgung](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Event Tracing Management](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-153">Der Verwaltungs Anbieter für die Ereignis Ablauf Verfolgung ermöglicht den Zugriff auf die Sitzungs Konfigurationen und Ablauf Verfolgungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-153">The Event Tracing Management provider provides access to Event Tracing for Windows (ETW) autologger session configurations and trace events.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Aktualisierung](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Updating](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-155">Der Cau-Anbieter (Failover Cluster-Aware Update) unterstützt die Koordination mit und die Verwaltung von Cau.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-155">The Failover Cluster-Aware Updating (CAU) provider supports coordination with and management of CAU.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failoverclustering mit Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failover Clustering Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-157">Der Hyper-v-Anbieter für Failoverclustering bietet die Verwaltung und Berichterstellung für Hyper-v in einer Cluster Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-157">The Failover Clustering Hyper-V provider provides management and reporting of Hyper-V in a clustering environment.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Speicher-QoS für Failoverclustering](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failover Clustering Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-159">Der-QoS-Anbieter (Failover Clustering Storage Quality of Service) bietet Verwaltung und Berichterstellung für die Clustering-Speicher-QoS-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-159">The Failover Clustering Storage Quality of Service (QoS) provider provides management and reporting of the clustering storage QoS policies.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failovercluster-v1-Anbieter](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failover Cluster V1 Provider](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-161">Der Failovercluster v1-Anbieter ermöglicht die Verwaltung eines Failoverclusters.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-161">The Failover Cluster V1 provider provides management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failovercluster-v1-Erweiterungen](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failover Cluster V1 Extensions](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-163">Der Failovercluster-Erweiterungs Anbieter bietet zusätzliche Verwaltungsfunktionen für einen-Failovercluster.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-163">The Failover Cluster Extensions provider provides additional management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gatewaysystemmonitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-165">Der Gateway Health Monitor-Anbieter verwaltet Ereignisse und Informationen zur gatewayintegritäts Überwachung.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-165">The Gateway Health Monitor provider manages gateway health monitoring events and information.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Gruppenrichtlinie-API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Group Policy API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-167">Der Gruppenrichtlinie-Anbieter ermöglicht die Richtlinien basierte Verwaltung mithilfe der Verzeichnisdienste von Microsoft Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-167">The Group Policy provider enables policy-based administration using Microsoft Active Directory (AD) directory services.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host-Überwachungsdienst](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host Guardian Service](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-169">Der Host-Überwachungs Dienstanbieter stellt die Verwaltung des Host-Überwachungs Diensts für abgeschirmte VMS bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-169">The Host Guardian Service provider provides management of the Host Guardian Service for shielded VMs.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-171">Mit dem Hyper-V-Anbieter können Sie Informationen zu virtuellen Computern verwalten und abrufen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-171">The Hyper-V provider allows you to manage and retrieve information about virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-173">Der Hyper-v-Anbieter (v2) erweitert den [Hyper-v-](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) Anbieter.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-173">The Hyper-V (V2) provider extends the [Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) provider.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internetinformationsdienste (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="dfd1f-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-175">Macht Programmierschnittstellen verfügbar, die verwendet werden können, um die IIS-Metabase abzufragen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-175">Exposes programming interfaces that can be used to query and configure the IIS metabase.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[IPAM-Server (Internet Protocol Address Management)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Internet Protocol Address Management (IPAM) Server](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-177">Der IPAM-Server Anbieter ermöglicht Entwicklern das Verwalten von IPAM über WMI.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-177">The IPAM Server Provider enables developers to manage IPAM through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-179">Der vorinstallierte IP-Routen Anbieter liefert IPv4-Netzwerk Routing Informationen, einschließlich (aber nicht beschränkt auf) die Informationen, die über den Befehl **Route Print** verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-179">The preinstalled IP Route provider supplies IPV4 network routing information, including (but not limited to) the information available through the **route print** command.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-181">Stellt IPMI-Daten aus dem Baseboard-Verwaltungs Controller (BMC) bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-181">Supplies IPMI data from Baseboard Management Controller (BMC) operations.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI-Ziel Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI Target Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-183">Der iSCSI-Zielserver Anbieter unterstützt eine WMI-Schnittstelle zum Verwalten des Microsoft iSCSI-Zielservers, z. b. das Erstellen von virtuellen Datenträgern und deren Darstellung für den Client.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-183">The iSCSI Target Server provider supports a WMI interface for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job-Objekt](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job Object](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-185">Der Auftrags Objekt Anbieter unterstützt den Zugriff auf Daten über benannte Kernel Auftrags Objekte.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-185">The Job Object provider supports access to data about named kernel job objects.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel-Ablauf Verfolgung](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel Trace](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-187">Mit dem vorinstallierten Kernel-Ablaufverfolgungs-Ereignis Anbieter können Sie Kernel-Ablauf Verfolgungs Ereignisse bei der Prozesserstellung, Prozess Beendigung, Thread Erstellung, Thread Beendigung und Modul Auslastung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-187">The preinstalled Kernel Trace event provider allows you to see kernel trace events on Process creation, Process termination, Thread creation, Thread termination and module load.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span><span class="sxs-lookup"><span data-stu-id="dfd1f-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-189">Stellt Klassen bereit, die benutzerdefinierte SIP-Anwendungen (Session Initiation Protocol) mit dem [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11))erstellen, registrieren, konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-189">Provides classes that create, register, configure, manage custom Session Initiation Protocol (SIP) applications with the [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registrierung der Verwaltungs Tools](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Management Tools Registry](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-191">Der Registrierungs Anbieter für Verwaltungs Tools ermöglicht den Remote Zugriff auf die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-191">The Management Tools Registry provider provides remote access to the registry.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Task-Manager für Verwaltungs Tools](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Management Tools Task Manager](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-193">Der Task-Manager-Anbieter für Verwaltungs Tools ermöglicht den Zugriff und die Verwaltung der Task-Manager-Daten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-193">The Management Tools Task Manager provider provides access and management of the Task Manager data.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM-Anwendung](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM Application](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-195">Der MDM-Anwendungsanbieter (Mobile Device Management, Verwaltung mobiler Geräte) verwaltet Anwendungen auf Geräten, die den MDM-Dienst abonniert haben.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-195">The Mobile Device Management (MDM) application provider manages applications on devices that are subscribed to the MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM-Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-197">Der MDM-Bridge-Anbieter ermöglicht die MDM-Verwaltung einer Netzwerk Brücke.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-197">The MDM Bridge provider enables MDM management of a network bridge.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM-Einstellungen](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM Settings](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-199">Der MDM-Einstellungs Anbieter ermöglicht die Verwaltung von Einstellungen auf Geräten, die bei einem MDM-Dienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-199">The MDM Settings Provider enables management of settings on devices enrolled with a MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ pcsvdevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-201">Der [MSFT \_ pcsvdevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) -Anbieter macht eine Klasse verfügbar, die eine Ansichts Klasse für ein physisches Computersystem definiert.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-201">The [MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) provider exposes a class that defines a view class for a physical computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[Msnettimplatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-203">Der [msnettimplatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) -Anbieter Abschnitt enthält Referenzinformationen zu den in NdisIMPlatCim.dll implementierten msnettimplatform-Anbieter Klassen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-203">The [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) provider section provides reference information for MsNetImPlatform provider classes implemented in NdisIMPlatCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[Netadaptercim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-205">Der [netadaptercim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) -Anbieter unterstützt Klassen, die auf Netzwerkadapter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-205">The [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) provider supports classes that access network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[Netdacim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-207">Dieser Abschnitt enthält Referenzinformationen für [netdacim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) -Anbieter Klassen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-207">This section provides reference information for [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) Provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[Netnccim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-209">Stellt Referenzinformationen für [netnccim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) -Anbieter Klassen bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-209">Provides reference information for [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[Netpeer-Dist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-211">Der [netpeerdist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) -Anbieter unterstützt Klassen, die mit der BranchCache-Infrastruktur interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-211">The [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) provider supports classes that interact with the Branch Cache infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[Netqoscim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-213">Der [netqoscim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) -Anbieter stellt Daten für die Netzwerkdienst Qualität (Quality of Service, QoS) und QoS-Einstellungsdaten bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-213">The [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) provider supplies data for network quality of service (QoS) and QoS setting data.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>["Netzwitchteam"](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-215">In diesem Abschnitt finden Sie Referenzinformationen zu den in "netungwitchteam. mof" deklarierten und in NetSwitchTeamCim.dll implementierten Klassen von "netzwitchteam".</span><span class="sxs-lookup"><span data-stu-id="dfd1f-215">This section provides reference information for NetSwitchTeam provider classes declared in NetSwitchTeam.mof and implemented in NetSwitchTeamCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[Nettcpip](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-217">Der Nettcpip-Anbieter unterstützt Klassen, die mit tcpip-Verbindungen interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-217">The NetTCPIP provider supports classes that interact with TCPIP connections.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[Netttcim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-219">In diesem Abschnitt finden Sie Referenzinformationen zu netttcim-Anbieter Klassen, die in "netttcim. mof" definiert und in NetTtCim.dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-219">This section provides reference information for NetTtCim provider classes defined in NetTtCim.mof and implemented in NetTtCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[Netwnv](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-221">Der netwnv-Anbieter unterstützt Klassen, die mit netzwerkvirtualisierungstechnologien interagieren.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-221">The NetWNV provider supports classes that interact with net virtualization technologies.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Netzwerk Zugriffsschutz](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Network Access Protection](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-223">Der Netzwerk Zugriffsschutz-Anbieter macht eine Plattform für den geschützten Zugriff auf private Netzwerke verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-223">The Network Access Protection provider exposes a platform for protected access to private networks.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Netzwerk Lastenausgleich](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Network Load Balancing](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-225">Der Netzwerk Lastenausgleich-Anbieter (Network Load Balancing, NLB) ermöglicht die Verwaltung eines NLB-Clusters.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-225">The Network Load Balancing (NLB) Provider enables management of a NLB cluster.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Network Controller-Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-227">Der Anbieter ermöglicht die Verwaltung eines Netzwerk Controller Servers.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-227">The provider enables management of a network controller server.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-229">Der-Anbieter für NFS ermöglicht Ihnen das Erstellen von Tools und Skripts zum Konfigurieren und Überwachen des Windows-Netzwerkdatei Systems.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-229">The provider for NFS allows you to create tools and scripts for configuring and monitoring the Windows Network File System.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Video](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-231">Der Ping-Anbieter bietet Zugriff auf die Statusinformationen, die vom Standardpingbefehl bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-231">The Ping provider supplies access to the status information provided by the standard ping command.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-233">Stellt Erweiterungen für die Gruppenrichtlinie bereit und ermöglicht Optimierungen in der Anwendung der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-233">Provides extensions to group policy, and permits refinements in the application of policy.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Energieverbrauchs Einheit](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Power Meter](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-235">Der Power Meter-Anbieter unterstützt die Schnittstelle für Energiemessung und Budgetierung (PMB).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-235">The Power Meter provider supports the Power Metering and Budgeting (PMB) interface.</span></span> <span data-ttu-id="dfd1f-236">Diese Klassen sind die primäre Schnittstelle für die Abfrage von PMI-Informationen (Power Meter Interface) von den zugrunde liegenden Energiezählern des Systems.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-236">These classes are the primary interface for the query of Power Meter Interface (PMI) information from underlying power meters on the system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Energierichtlinie](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Power Policy](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-238">Der Energierichtlinien Anbieter bietet Klassen die Möglichkeit, die gesamte Infrastruktur der Energierichtlinie Remote zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-238">The Power Policy provider provides classes the ability to remotely manage all the power policy infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[Ramgmtpsprovider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-240">Der [ramgmtpsprovider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) -Anbieter stellt Klassen zum Verwalten des Remote Zugriffs bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-240">The [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) provider provides classes to manage Remote Access.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[Raserverpsprovider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-242">Der [raserverpsprovider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) -Anbieter stellt Klassen zum Verwalten des Remote Zugriffs Servers bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-242">The [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) provider provides classes to manage the Remote Access Server.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[Reliabilitymetricsprovider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-244">Der [reliabilitymetricsprovider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) -Anbieter macht die Zuverlässigkeits Metrik für das System und das Windows-Ereignisprotokoll verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-244">The [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) provider exposes system and Windows Event Log reliability metrics.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remotedesktopdienste](/windows/desktop/TermServ/terminal-services-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remote Desktop Services](/windows/desktop/TermServ/terminal-services-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-246">Ermöglicht eine konsistente Serververwaltung in einer Remotedesktopdienste Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-246">Enables consistent server administration in a Remote Desktop Services environment.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-248">Definiert Klassen, die es Ihnen ermöglichen, Skripts und Code zum Ändern der Einstellungen des Berichts Servers und des Berichts-Manager zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-248">Defines classes that allow you to write scripts and code to modify the settings of the report server and the Report Manager.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Richtlinien Ergebnissatz (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Resultant Set of Policy (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-250">Stellt Methoden zum Planen und Debuggen von Richtlinien Einstellungen in einer was-wäre-wenn-Situation bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-250">Supplies methods to plan and debug policy settings in a what-if situation.</span></span> <span data-ttu-id="dfd1f-251">Mit diesen Methoden können Administratoren problemlos die Kombination von Richtlinien Einstellungen ermitteln, die für einen Benutzer oder Computer gelten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-251">These methods allow administrators to determine easily the combination of policy settings that apply to, or will apply to, a user or computer.</span></span> <span data-ttu-id="dfd1f-252">Dies wird als Richtlinien Ergebnissatz (RSoP) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-252">This is known as the Resultant Set of Policy (RSoP).</span></span> <span data-ttu-id="dfd1f-253">Weitere Informationen finden Sie unter Informationen zum [RSoP-WMI-Methoden Anbieter](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) und [RSoP-WMI-Klassen](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-253">For more information, see [About the RSoP WMI Method Provider](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) and [RSoP WMI Classes](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Sicherung](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Security](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-255">Ruft Sicherheitseinstellungen ab, mit denen Besitz-, Überwachungs-und Zugriffsrechte für Dateien, Verzeichnisse und Freigaben gesteuert werden, oder ändert Sie.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-255">Retrieves or changes security settings that control ownership, auditing, and access rights to files, directories, and shares.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[Server Manager. deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-257">Der [Server Manager. deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) macht Bereitstellungs Funktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-257">The [ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) exposes deployment functionality.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sitzung](/previous-versions/windows/desktop/wmipsess/session-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-259">Verwaltet Netzwerksitzungen und Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-259">Manages network sessions and connections.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Schatten Kopie](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Shadow Copy](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-261">Stellt Verwaltungsfunktionen für die Schatten Kopien der Funktion für freigegebene Ordner bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-261">Supplies management functions for the Shadow Copies of the Shared Folders feature.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Abgeschirmte VM-Bereitstellung](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Shielded VM Provisioning](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-263">Der abgeschirmte VM Bereitstellung Provider ermöglicht einem Fabric Controller, die sichere Bereitstellung einer abgeschirmten VM auf einem Hyper-V-Host zu starten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-263">The Shielded VM Provisioning provider enables a fabric controller to start the secure provisioning of a shielded VM on a Hyper-V host.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Geschützter VM Provisioning-Dienst](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Shielded VM Provisioning Service](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-265">Der Anbieter ermöglicht die Bereitstellung eines abgeschirmten virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-265">The provider enables provisioning of a shielded virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB-Verwaltung](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB Management](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-267">Die SMB-Verwaltungs-API stellt Klassen und Methoden zum Verwalten von Freigaben und zum Freigeben des Zugriffs bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-267">The SMB Management API provides classes and methods to manage shares and share access.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP-](/windows/desktop/WmiSdk/snmp-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP](/windows/desktop/WmiSdk/snmp-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-269">Ordnet SNMP-Objekte (Simple Network Management Protocol), die in MIB-Schema Objekten (Management Information Base) definiert sind, Klassen zu.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-269">Maps Simple Network Management Protocol (SNMP) objects that are defined in Management Information Base (MIB) schema objects to classes.</span></span> <span data-ttu-id="dfd1f-270">Weitere Informationen finden Sie unter [Einrichten der WMI-SNMP-Umgebung](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-270">For more information, see [Setting up the WMI SNMP Environment](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Protokollierung des Software Bestands](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Software Inventory Logging](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-272">Der Anbieter für die Software Inventur Protokollierung sammelt Lizenzierungs Daten zu Software, die auf einem Windows-Server installiert ist, und ermöglicht den Remote Zugriff auf die Daten, sodass Sie problemlos von einem Rechenzentrum aggregiert werden können.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-272">The Software Inventory Logging provider collects licensing data about software installed on a Windows Server, and provides remote access to the data so it can be aggregated easily by a datacenter.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Lizenzierung für Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Licensing for Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-274">[Software Lizenzierungs Klassen](/previous-versions/windows/desktop/sppwmi/software-license-provider-) , die für Windows Vista verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-274">[Software Licensing Classes](/previous-versions/windows/desktop/sppwmi/software-license-provider-) used for Windows Vista.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software Lizenz](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software License](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-276">Der Software Lizenzierungs Anbieter ruft Software Lizenzierungs Daten ab.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-276">The Software Licensing provider retrieves software licensing data.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Speicher Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-278">Der Speichervolumeanbieter stellt Volumen Verwaltungsfunktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-278">The Storage Volume provider supplies volume management functions.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Speicher Replikat](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Replica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-280">Der Anbieter ermöglicht die Verwaltung eines Speicher Replikats.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-280">The provider enables management of a storage replica.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registrierung](/previous-versions/windows/desktop/regprov/system-registry-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-282">Mit dem System Registrierungs Anbieter können Verwaltungs Anwendungen Daten in der Systemregistrierung abrufen und ändern und Benachrichtigungen erhalten, wenn Änderungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-282">The System Registry provider enables management applications to retrieve and modify data in the system registry, and receive notifications when changes occur.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Wiederherstellung](/windows/desktop/sr/system-restore-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Restore](/windows/desktop/sr/system-restore-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-284">Stellt Klassen bereit, die die System Wiederherstellungs Funktion konfigurieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-284">Supplies classes that configure and use System Restore functionality.</span></span> <span data-ttu-id="dfd1f-285">Weitere Informationen finden Sie unter [Konfigurieren der Systemwiederherstellung](/windows/desktop/sr/configuring-system-restore) und der [WMI-Klassen für die Systemwiederherstellung](/windows/desktop/sr/system-restore-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-285">For more information, see [Configuring System Restore](/windows/desktop/sr/configuring-system-restore) and the [System Restore WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-287">Ermöglicht den Zugriff auf Daten über ein Sicherheitsgerät, das durch eine Instanz von [**Win32 \_ TPM**](/windows/desktop/SecProv/win32-tpm)repräsentiert wird, das der Stamm der Vertrauensstellung für ein Computersystem mit vertrauenswürdiger Microsoft Windows-Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-287">Provides access to data about a security device, represented by an instance of [**Win32\_TPM**](/windows/desktop/SecProv/win32-tpm), that is the root of trust for a Microsoft Windows trusted platform computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-289">Der [TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) -Anbieter ist ein Instanzanbieter, der Klassen mit Informationen zu den Vertrauens Stellungen zwischen Domänen erstellt.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-289">The [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) provider is an instance provider that creates classes with information about the trust relationships between domains.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Benutzer Zugriffs Protokollierung](/previous-versions/windows/desktop/ual/user-access-logging)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[User Access Logging](/previous-versions/windows/desktop/ual/user-access-logging)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-291">Die Benutzer Zugriffs Protokollierung (User Access Logging, UAL) ist ein gängiges Framework für Windows Server-Rollen, mit dem ihre jeweiligen Nutzungs</span><span class="sxs-lookup"><span data-stu-id="dfd1f-291">User Access Logging (UAL) is a common framework for Windows Server roles to report their respective consumption metrics.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[Userprofileprovider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-293">Der [userprofileprovider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) -Anbieter macht Klassen verfügbar, die Informationen zu einem Benutzerprofil in einem Windows-System sowie den Integritäts Status eines umgeleiteten Benutzer Ordners bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-293">The [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) provider exposes classes that provide information about a user profile on a Windows system, as well as the health status of a redirected user folder.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Benutzer Zustands Verwaltung](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[User State Management](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-295">Der Anbieter für die Benutzer Zustands Verwaltung macht eine Verwaltungs-und Berichterstattungs-API für Unternehmens Szenarios verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-295">The User State Management provider exposes a management and reporting API for enterprise scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[Anschauung](/windows/desktop/WmiSdk/view-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[View](/windows/desktop/WmiSdk/view-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-297">Erstellt neue Instanzen und Methoden auf der Grundlage von Instanzen von anderen Klassen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-297">Creates new instances and methods based on instances of other classes.</span></span> <span data-ttu-id="dfd1f-298">Zwei Versionen des Ansichts Anbieters sind auf 64-Bit-Plattformen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-298">Two versions of the View provider are available on 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[Vpnclientpsprovider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-300">Der [vpnclientpsprovider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) -Anbieter stellt eine Plattform für die Automatisierung der Konnektivität mit einem virtuellen privaten Netzwerkclient zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-300">The [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) provider exposes a platform for automating connectivity to a virtual private network client.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-302">Bietet Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem Windows-Treibermodell (WDM) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-302">Provides access to the classes, instances, methods, and events of hardware drivers that conform to the Windows Driver Model (WDM).</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[Wfascim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-304">Der [wfascim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) -Anbieter macht Features für die Netzwerksicherheit und-Filterung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-304">The [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) provider exposes network security and filtering features.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[Whqlprovider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-306">Der [whqlprovider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) -Anbieter macht Informationen über digitale Signaturen über Treiber verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-306">The [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) provider exposes digital signature information about drivers.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-308">Der [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) -Anbieter macht die aktuellen, lokalen und UTC-basierten Zeitstempel auf einem Computersystem verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-308">The [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) provider exposes the current, local, and UTC-based timestamps on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDac)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-310">Stellt die Verwaltung von WDac bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-310">Provides management of WDAC.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-312">Der Windows Defender-Anbieter macht Windows Defender-Sicherheitsfeatures verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-312">The Windows Defender provider exposes Windows Defender security features.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-314">Der Windows Installer-Anbieter, der auch als MSI-Anbieter bezeichnet wird, ermöglicht Anwendungen den Zugriff auf Informationen, die von Windows Installer kompatiblen Anwendungen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-314">The Windows Installer provider, also known as the MSI provider allows applications to access information collected from Windows Installer compliant applications.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows-Produktaktivierung](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Product Activation](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-316">Der Windows-Produkt Aktivierungs Anbieter (WPA) ist eine antischadsoftwaretechnologie, die das gelegentliche Kopieren von Software reduziert.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-316">The Windows Product Activation (WPA) provider is an anti-piracy technology aimed at reducing the casual copying of software.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows-Server-Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-318">Der Anbieter ermöglicht den Zugriff auf und die Verwaltung der Konfiguration, die von der Server-Manager Anwendung gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-318">The provider enables access to and management of the configuration controlled by the Server Manager application.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server-Speicherverwaltung (msftstraugman)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-320">Der msftstringman-Anbieter bietet die Verwaltung von Speichersystemen auf Windows Server-Produkten.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-320">The MsftStrgMan provider provides management for storage systems on Windows Server products.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows-Speicherverwaltung ("straugmgmt")](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-322">Mit dem "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "".</span><span class="sxs-lookup"><span data-stu-id="dfd1f-322">The StrgMgmt provider can be used to manage a wide range of storage configurations, from tablets to external storage arrays on servers.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows-System Bewertungs Tool](/windows/desktop/WinSAT/winsat-mof-classes)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows System Assessment Tool](/windows/desktop/WinSAT/winsat-mof-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-324">Das Windows-System Bewertungs Tool (WinSAT) stellt eine Reihe von Klassen zur Verfügung, mit denen die Leistungsmerkmale und-Funktionen eines Computers bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-324">The Windows System Assessment Tool (WinSAT) exposes a number of classes that assesses the performance characteristics and capabilities of a computer.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI-Kern](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-326">Der WMI-Kern Anbieter definiert Klassen, die die Kernfunktionen von WMI bilden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-326">The WMI Core provider defines classes that compose the core functionality of WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[MSFT \_ providersubsystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-328">Der [MSFT \_ providersubsystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) -Anbieter unterstützt Anbieter.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-328">The [Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) provider supports providers.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32 \_ -Leistung](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32\_Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-330">Die abstrakte Klasse von [**Win32 \_ perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) ist die Basisklasse für die Leistungs Leistungsdaten-Klassen [**Win32 \_ perfrawdata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) und [**Win32 \_ perfformatteddata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-330">The [**Win32\_Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) abstract class is the base class for the performance counter classes [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) and [**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span></span> <span data-ttu-id="dfd1f-331">Sie definiert die erforderlichen Zeitstempel-und Häufigkeits Eigenschaften, die in den CounterType-Algorithmen für die Leistungsindikator Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-331">It defines the required timestamp and frequency properties used in the CounterType algorithms for the performance counter classes.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ perfformatteddata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-333">Eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-333">An abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32- \_ perfrawdata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-335">Die Leistungs Leistungsdaten-Klasse [**Win32 \_ perfrawdata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) ist die abstrakte Basisklasse für alle konkreten Klassen von reinen Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-335">The performance counter class [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) is the abstract base class for all concrete raw performance counter classes.</span></span> <span data-ttu-id="dfd1f-336">Um im System Monitor angezeigt zu werden, müssen Leistungsindikatoren Klassen zum \\ Namespace "root CIMv2" hinzugefügt und von **Win32 \_ perfrawdata** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-336">To appear in System Monitor, performance counter classes must be added to the "Root\\CIMv2" namespace and derived from **Win32\_PerfRawData**.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[Wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-338">Erstellt die WMI- [Leistungs Leistungs Ereignis Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="dfd1f-338">Creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="dfd1f-339">Daten werden vom WMIPerfInst-Anbieter dynamisch für diese Leistungsklassen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-339">Data is dynamically supplied to these performance classes by the WMIPerfInst provider.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[Wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-341">Stellt Daten zu Rohdaten und formatierten Leistungsdaten dynamisch aus Leistungs Bestellungs [Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes) Definitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-341">Supplies raw and formatted performance counter data dynamically from [Performance Counter Class](/windows/desktop/CIMWin32Prov/performance-counter-classes) definitions.</span></span>

</dd> <dt>

<span data-ttu-id="dfd1f-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Arbeitsordner](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span><span class="sxs-lookup"><span data-stu-id="dfd1f-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Work Folders](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dfd1f-343">Arbeitsordner werden zum Synchronisieren von Dateien mit mehreren PCs und mobilen Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="dfd1f-343">Work Folders is used to synchronize files with multiple PCs and mobile devices.</span></span>

</dd> </dl>

 

 
