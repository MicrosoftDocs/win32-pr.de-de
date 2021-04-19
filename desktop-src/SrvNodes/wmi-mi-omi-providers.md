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
# <a name="wmimiomi-providers"></a>WMI/MI/OMI-Anbieter

Die Windows-Verwaltungsinfrastruktur (WMI), die Verwaltungs Instrumentation (Mi) und die Open Management Infrastructure (OMI) verwenden alle Management Object Format (MOF)-Dateien, um die Informationen zu beschreiben, die von den jeweiligen Anbietern zur Verfügung gestellt werden.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

Der Active Directory-Anbieter, der auch als Verzeichnisdienste (DS)-Anbieter bezeichnet wird, ordnet Active Directory Objekte WMI zu. Durch den Zugriff auf den LDAP-Namespace (Lightweight Directory Access Protocol) in WMI können Sie in der Active Directory auf einen Alias verweisen oder ein Objekt erstellen.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Anwendungs Inventur](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

Die WMI-Klassen für die Anwendungs Inventur ermöglichen die Ermittlung der installierten Win32-Anwendungen und Windows Store-Anwendungen auf einem Windows-System.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Anwendungs Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

Der Anwendungs Proxy-WMI-Anbieter ermöglicht Entwicklern den Zugriff auf den webanwendungsproxy-Dienst, damit Administratoren Anwendungen für den externen Zugriff veröffentlichen können Der webanwendungsproxy ist ein Reverseproxy für Active Directory-Verbunddienste (AD FS) (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker-Laufwerkverschlüsselung (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Bietet eine Konfiguration und Verwaltung für einen Speicherbereich auf einem Festplattenlaufwerk, das durch eine Instanz von [**Win32 \_ verschlüsseltablevolume**](/windows/desktop/SecProv/win32-encryptablevolume)dargestellt wird, die mithilfe der Verschlüsselung geschützt werden kann.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[Bohrer](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

Der Background Intelligent Transfer Service (Bits) Compact Server mit Bits-Remote Verwaltung ermöglicht es authentifizierten Administratoren oder Controller Anwendungen, Bits-Übertragungs Aufträge Remote zu erstellen, zu ändern und zu verwalten, ohne den Internetinformationsdienste (IIS)-Dienst zu verwenden.

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Bietet Zugriff auf die BizTalk-Verwaltungs Objekte, die durch WMI-Klassen dargestellt werden.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Startkonfigurationsdaten](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

Der Startkonfigurationsdaten (BCD)-Anbieter stellt einen Speicher bereit, der zum Beschreiben von Start Anwendungen und Start Anwendungseinstellungen verwendet wird.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Start Ereignis Sammler](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

Der WMI-Anbieter des Start Ereignis Sammlers ermöglicht den Zugriff auf Verbindungs-und Konfigurationsinformationen für das Setup-und Start Ereignis Sammlungs Feature unter Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[Cimwin32, Win32, Energie Verwaltungs Ereignisse](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

Die cimwin32-Anbieter unterstützen die in CimWin32.dll implementierten Klassen und bestehen aus den Core-CIM-Klassen, der Win32-Implementierung dieser Klassen und den Energie Verwaltungs Ereignissen.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

Der CIMWin32a-Anbieter erweitert die im [cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)verfügbaren Klassen.

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[Dcbqoscim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

Der dcbqoscim-Anbieter unterstützt Klassen, die Einstellungsdaten für Netzwerk-QoS, Steuerungs Einstellungsdaten und Datenverkehrs Klassen-Einstellungsdaten beschreiben.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Verteiltes Dateisystem (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

Der DFS-Anbieter stellt mithilfe von WMI Skript fähige-DFS-Funktionen bereit.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Verteiltes Dateisystem Replikation (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Erstellt Tools zum Konfigurieren und Überwachen des [verteiltes Dateisystem (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) -Dienstanbieter. Weitere Informationen finden Sie unter [DFSR-WMI-Klassen](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

Der [dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) -Anbieter unterstützt Klassen, die den DFS-Namespace Zugriff implementieren.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[Dhcpserverpsprovider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

Der [dhcpserverpsprovider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) -Anbieter unterstützt Klassen, die mit einem DHCP-Server (Dynamic Host Configuration Protocol) interagieren.

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Datenträger Kontingent](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

Mithilfe des Windows-Datenträger Kontingent Anbieters können Administratoren die Datenmenge steuern, die von den einzelnen Benutzern in einem NTFS-Dateisystem gespeichert wird.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

Der DTC-Anbieter ermöglicht die Verwaltung des DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[DNS-](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Ermöglicht es Administratoren und Programmierern, Domain Name System (DNS)-Ressourcen Einträge (RRS) und DNS-Server mithilfe von WMI zu konfigurieren.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim-Anbieter Klassen](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

Der dnsclientcim-Anbieter unterstützt Klassen, die mit einem DNS-Client (Domain Name System) interagieren.

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[Dnsclientpsprovider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

Der [dnsclientpsprovider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) -Anbieter unterstützt WMI-Klassen, die mit einem DNS-Client interagieren.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[Dnsserverpsprovider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

Der [dnsserverpsprovider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) -Anbieter unterstützt WMI-Klassen, die mit einem DNS-Server interagieren.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

Der [Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider) Anbieter bietet Zugriff auf Daten aus dem Ereignisprotokoll Dienst und Benachrichtigungen über Ereignisse.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Verwaltung der Ereignis Ablauf Verfolgung](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

Der Verwaltungs Anbieter für die Ereignis Ablauf Verfolgung ermöglicht den Zugriff auf die Sitzungs Konfigurationen und Ablauf Verfolgungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (ETW).

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Aktualisierung](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

Der Cau-Anbieter (Failover Cluster-Aware Update) unterstützt die Koordination mit und die Verwaltung von Cau.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failoverclustering mit Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

Der Hyper-v-Anbieter für Failoverclustering bietet die Verwaltung und Berichterstellung für Hyper-v in einer Cluster Umgebung.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Speicher-QoS für Failoverclustering](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

Der-QoS-Anbieter (Failover Clustering Storage Quality of Service) bietet Verwaltung und Berichterstellung für die Clustering-Speicher-QoS-Richtlinien.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failovercluster-v1-Anbieter](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

Der Failovercluster v1-Anbieter ermöglicht die Verwaltung eines Failoverclusters.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failovercluster-v1-Erweiterungen](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

Der Failovercluster-Erweiterungs Anbieter bietet zusätzliche Verwaltungsfunktionen für einen-Failovercluster.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gatewaysystemmonitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

Der Gateway Health Monitor-Anbieter verwaltet Ereignisse und Informationen zur gatewayintegritäts Überwachung.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Gruppenrichtlinie-API](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

Der Gruppenrichtlinie-Anbieter ermöglicht die Richtlinien basierte Verwaltung mithilfe der Verzeichnisdienste von Microsoft Active Directory (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host-Überwachungsdienst](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

Der Host-Überwachungs Dienstanbieter stellt die Verwaltung des Host-Überwachungs Diensts für abgeschirmte VMS bereit.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

Mit dem Hyper-V-Anbieter können Sie Informationen zu virtuellen Computern verwalten und abrufen.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

Der Hyper-v-Anbieter (v2) erweitert den [Hyper-v-](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) Anbieter.

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internetinformationsdienste (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Macht Programmierschnittstellen verfügbar, die verwendet werden können, um die IIS-Metabase abzufragen und zu konfigurieren.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[IPAM-Server (Internet Protocol Address Management)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

Der IPAM-Server Anbieter ermöglicht Entwicklern das Verwalten von IPAM über WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

Der vorinstallierte IP-Routen Anbieter liefert IPv4-Netzwerk Routing Informationen, einschließlich (aber nicht beschränkt auf) die Informationen, die über den Befehl **Route Print** verfügbar sind.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Stellt IPMI-Daten aus dem Baseboard-Verwaltungs Controller (BMC) bereit.

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI-Ziel Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

Der iSCSI-Zielserver Anbieter unterstützt eine WMI-Schnittstelle zum Verwalten des Microsoft iSCSI-Zielservers, z. b. das Erstellen von virtuellen Datenträgern und deren Darstellung für den Client.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job-Objekt](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

Der Auftrags Objekt Anbieter unterstützt den Zugriff auf Daten über benannte Kernel Auftrags Objekte.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel-Ablauf Verfolgung](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

Mit dem vorinstallierten Kernel-Ablaufverfolgungs-Ereignis Anbieter können Sie Kernel-Ablauf Verfolgungs Ereignisse bei der Prozesserstellung, Prozess Beendigung, Thread Erstellung, Thread Beendigung und Modul Auslastung anzeigen.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Stellt Klassen bereit, die benutzerdefinierte SIP-Anwendungen (Session Initiation Protocol) mit dem [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11))erstellen, registrieren, konfigurieren und verwalten.

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registrierung der Verwaltungs Tools](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

Der Registrierungs Anbieter für Verwaltungs Tools ermöglicht den Remote Zugriff auf die Registrierung.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Task-Manager für Verwaltungs Tools](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

Der Task-Manager-Anbieter für Verwaltungs Tools ermöglicht den Zugriff und die Verwaltung der Task-Manager-Daten.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM-Anwendung](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

Der MDM-Anwendungsanbieter (Mobile Device Management, Verwaltung mobiler Geräte) verwaltet Anwendungen auf Geräten, die den MDM-Dienst abonniert haben.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM-Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

Der MDM-Bridge-Anbieter ermöglicht die MDM-Verwaltung einer Netzwerk Brücke.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM-Einstellungen](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

Der MDM-Einstellungs Anbieter ermöglicht die Verwaltung von Einstellungen auf Geräten, die bei einem MDM-Dienst registriert sind.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ pcsvdevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

Der [MSFT \_ pcsvdevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) -Anbieter macht eine Klasse verfügbar, die eine Ansichts Klasse für ein physisches Computersystem definiert.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[Msnettimplatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

Der [msnettimplatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) -Anbieter Abschnitt enthält Referenzinformationen zu den in NdisIMPlatCim.dll implementierten msnettimplatform-Anbieter Klassen.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[Netadaptercim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

Der [netadaptercim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) -Anbieter unterstützt Klassen, die auf Netzwerkadapter zugreifen.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[Netdacim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

Dieser Abschnitt enthält Referenzinformationen für [netdacim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) -Anbieter Klassen.

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[Netnccim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Stellt Referenzinformationen für [netnccim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) -Anbieter Klassen bereit.

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[Netpeer-Dist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

Der [netpeerdist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) -Anbieter unterstützt Klassen, die mit der BranchCache-Infrastruktur interagieren.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[Netqoscim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

Der [netqoscim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) -Anbieter stellt Daten für die Netzwerkdienst Qualität (Quality of Service, QoS) und QoS-Einstellungsdaten bereit.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>["Netzwitchteam"](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

In diesem Abschnitt finden Sie Referenzinformationen zu den in "netungwitchteam. mof" deklarierten und in NetSwitchTeamCim.dll implementierten Klassen von "netzwitchteam".

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[Nettcpip](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

Der Nettcpip-Anbieter unterstützt Klassen, die mit tcpip-Verbindungen interagieren.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[Netttcim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

In diesem Abschnitt finden Sie Referenzinformationen zu netttcim-Anbieter Klassen, die in "netttcim. mof" definiert und in NetTtCim.dll implementiert werden.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[Netwnv](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

Der netwnv-Anbieter unterstützt Klassen, die mit netzwerkvirtualisierungstechnologien interagieren.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Netzwerk Zugriffsschutz](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

Der Netzwerk Zugriffsschutz-Anbieter macht eine Plattform für den geschützten Zugriff auf private Netzwerke verfügbar.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Netzwerk Lastenausgleich](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

Der Netzwerk Lastenausgleich-Anbieter (Network Load Balancing, NLB) ermöglicht die Verwaltung eines NLB-Clusters.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Network Controller-Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht die Verwaltung eines Netzwerk Controller Servers.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

Der-Anbieter für NFS ermöglicht Ihnen das Erstellen von Tools und Skripts zum Konfigurieren und Überwachen des Windows-Netzwerkdatei Systems.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Video](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

Der Ping-Anbieter bietet Zugriff auf die Statusinformationen, die vom Standardpingbefehl bereitgestellt werden.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Stellt Erweiterungen für die Gruppenrichtlinie bereit und ermöglicht Optimierungen in der Anwendung der Richtlinie.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Energieverbrauchs Einheit](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

Der Power Meter-Anbieter unterstützt die Schnittstelle für Energiemessung und Budgetierung (PMB). Diese Klassen sind die primäre Schnittstelle für die Abfrage von PMI-Informationen (Power Meter Interface) von den zugrunde liegenden Energiezählern des Systems.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Energierichtlinie](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

Der Energierichtlinien Anbieter bietet Klassen die Möglichkeit, die gesamte Infrastruktur der Energierichtlinie Remote zu verwalten.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[Ramgmtpsprovider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

Der [ramgmtpsprovider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) -Anbieter stellt Klassen zum Verwalten des Remote Zugriffs bereit.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[Raserverpsprovider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

Der [raserverpsprovider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) -Anbieter stellt Klassen zum Verwalten des Remote Zugriffs Servers bereit.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[Reliabilitymetricsprovider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

Der [reliabilitymetricsprovider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) -Anbieter macht die Zuverlässigkeits Metrik für das System und das Windows-Ereignisprotokoll verfügbar.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remotedesktopdienste](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Ermöglicht eine konsistente Serververwaltung in einer Remotedesktopdienste Umgebung.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Definiert Klassen, die es Ihnen ermöglichen, Skripts und Code zum Ändern der Einstellungen des Berichts Servers und des Berichts-Manager zu schreiben.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Richtlinien Ergebnissatz (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Stellt Methoden zum Planen und Debuggen von Richtlinien Einstellungen in einer was-wäre-wenn-Situation bereit. Mit diesen Methoden können Administratoren problemlos die Kombination von Richtlinien Einstellungen ermitteln, die für einen Benutzer oder Computer gelten. Dies wird als Richtlinien Ergebnissatz (RSoP) bezeichnet. Weitere Informationen finden Sie unter Informationen zum [RSoP-WMI-Methoden Anbieter](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) und [RSoP-WMI-Klassen](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Sicherung](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Ruft Sicherheitseinstellungen ab, mit denen Besitz-, Überwachungs-und Zugriffsrechte für Dateien, Verzeichnisse und Freigaben gesteuert werden, oder ändert Sie.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[Server Manager. deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

Der [Server Manager. deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) macht Bereitstellungs Funktionen verfügbar.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sitzung](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Verwaltet Netzwerksitzungen und Verbindungen.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Schatten Kopie](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Stellt Verwaltungsfunktionen für die Schatten Kopien der Funktion für freigegebene Ordner bereit.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Abgeschirmte VM-Bereitstellung](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

Der abgeschirmte VM Bereitstellung Provider ermöglicht einem Fabric Controller, die sichere Bereitstellung einer abgeschirmten VM auf einem Hyper-V-Host zu starten.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Geschützter VM Provisioning-Dienst](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht die Bereitstellung eines abgeschirmten virtuellen Computers.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB-Verwaltung](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

Die SMB-Verwaltungs-API stellt Klassen und Methoden zum Verwalten von Freigaben und zum Freigeben des Zugriffs bereit.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[SNMP-](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Ordnet SNMP-Objekte (Simple Network Management Protocol), die in MIB-Schema Objekten (Management Information Base) definiert sind, Klassen zu. Weitere Informationen finden Sie unter [Einrichten der WMI-SNMP-Umgebung](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Protokollierung des Software Bestands](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

Der Anbieter für die Software Inventur Protokollierung sammelt Lizenzierungs Daten zu Software, die auf einem Windows-Server installiert ist, und ermöglicht den Remote Zugriff auf die Daten, sodass Sie problemlos von einem Rechenzentrum aggregiert werden können.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Lizenzierung für Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Software Lizenzierungs Klassen](/previous-versions/windows/desktop/sppwmi/software-license-provider-) , die für Windows Vista verwendet werden.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software Lizenz](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

Der Software Lizenzierungs Anbieter ruft Software Lizenzierungs Daten ab.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Speicher Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

Der Speichervolumeanbieter stellt Volumen Verwaltungsfunktionen bereit.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Speicher Replikat](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht die Verwaltung eines Speicher Replikats.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registrierung](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

Mit dem System Registrierungs Anbieter können Verwaltungs Anwendungen Daten in der Systemregistrierung abrufen und ändern und Benachrichtigungen erhalten, wenn Änderungen auftreten.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Wiederherstellung](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Stellt Klassen bereit, die die System Wiederherstellungs Funktion konfigurieren und verwenden. Weitere Informationen finden Sie unter [Konfigurieren der Systemwiederherstellung](/windows/desktop/sr/configuring-system-restore) und der [WMI-Klassen für die Systemwiederherstellung](/windows/desktop/sr/system-restore-wmi-classes).

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

Ermöglicht den Zugriff auf Daten über ein Sicherheitsgerät, das durch eine Instanz von [**Win32 \_ TPM**](/windows/desktop/SecProv/win32-tpm)repräsentiert wird, das der Stamm der Vertrauensstellung für ein Computersystem mit vertrauenswürdiger Microsoft Windows-Plattform ist.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

Der [TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) -Anbieter ist ein Instanzanbieter, der Klassen mit Informationen zu den Vertrauens Stellungen zwischen Domänen erstellt.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Benutzer Zugriffs Protokollierung](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

Die Benutzer Zugriffs Protokollierung (User Access Logging, UAL) ist ein gängiges Framework für Windows Server-Rollen, mit dem ihre jeweiligen Nutzungs

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[Userprofileprovider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

Der [userprofileprovider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) -Anbieter macht Klassen verfügbar, die Informationen zu einem Benutzerprofil in einem Windows-System sowie den Integritäts Status eines umgeleiteten Benutzer Ordners bereitstellen.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Benutzer Zustands Verwaltung](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

Der Anbieter für die Benutzer Zustands Verwaltung macht eine Verwaltungs-und Berichterstattungs-API für Unternehmens Szenarios verfügbar.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[Anschauung](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Erstellt neue Instanzen und Methoden auf der Grundlage von Instanzen von anderen Klassen. Zwei Versionen des Ansichts Anbieters sind auf 64-Bit-Plattformen verfügbar.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[Vpnclientpsprovider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

Der [vpnclientpsprovider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) -Anbieter stellt eine Plattform für die Automatisierung der Konnektivität mit einem virtuellen privaten Netzwerkclient zur Verfügung.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

Bietet Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem Windows-Treibermodell (WDM) entsprechen.

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[Wfascim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

Der [wfascim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) -Anbieter macht Features für die Netzwerksicherheit und-Filterung verfügbar.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[Whqlprovider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

Der [whqlprovider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) -Anbieter macht Informationen über digitale Signaturen über Treiber verfügbar.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

Der [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) -Anbieter macht die aktuellen, lokalen und UTC-basierten Zeitstempel auf einem Computersystem verfügbar.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDac)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Stellt die Verwaltung von WDac bereit.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

Der Windows Defender-Anbieter macht Windows Defender-Sicherheitsfeatures verfügbar.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

Der Windows Installer-Anbieter, der auch als MSI-Anbieter bezeichnet wird, ermöglicht Anwendungen den Zugriff auf Informationen, die von Windows Installer kompatiblen Anwendungen gesammelt werden.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows-Produktaktivierung](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

Der Windows-Produkt Aktivierungs Anbieter (WPA) ist eine antischadsoftwaretechnologie, die das gelegentliche Kopieren von Software reduziert.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows-Server-Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht den Zugriff auf und die Verwaltung der Konfiguration, die von der Server-Manager Anwendung gesteuert wird.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server-Speicherverwaltung (msftstraugman)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

Der msftstringman-Anbieter bietet die Verwaltung von Speichersystemen auf Windows Server-Produkten.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows-Speicherverwaltung ("straugmgmt")](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

Mit dem "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "".

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows-System Bewertungs Tool](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

Das Windows-System Bewertungs Tool (WinSAT) stellt eine Reihe von Klassen zur Verfügung, mit denen die Leistungsmerkmale und-Funktionen eines Computers bewertet werden.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI-Kern](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

Der WMI-Kern Anbieter definiert Klassen, die die Kernfunktionen von WMI bilden.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[MSFT \_ providersubsystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

Der [MSFT \_ providersubsystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) -Anbieter unterstützt Anbieter.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32 \_ -Leistung](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

Die abstrakte Klasse von [**Win32 \_ perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) ist die Basisklasse für die Leistungs Leistungsdaten-Klassen [**Win32 \_ perfrawdata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) und [**Win32 \_ perfformatteddata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov). Sie definiert die erforderlichen Zeitstempel-und Häufigkeits Eigenschaften, die in den CounterType-Algorithmen für die Leistungsindikator Klassen verwendet werden.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ perfformatteddata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32- \_ perfrawdata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

Die Leistungs Leistungsdaten-Klasse [**Win32 \_ perfrawdata**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) ist die abstrakte Basisklasse für alle konkreten Klassen von reinen Leistungs Zählers. Um im System Monitor angezeigt zu werden, müssen Leistungsindikatoren Klassen zum \\ Namespace "root CIMv2" hinzugefügt und von **Win32 \_ perfrawdata** abgeleitet werden.

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[Wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Erstellt die WMI- [Leistungs Leistungs Ereignis Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes). Daten werden vom WMIPerfInst-Anbieter dynamisch für diese Leistungsklassen bereitgestellt.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[Wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Stellt Daten zu Rohdaten und formatierten Leistungsdaten dynamisch aus Leistungs Bestellungs [Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes) Definitionen bereit.

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Arbeitsordner](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

Arbeitsordner werden zum Synchronisieren von Dateien mit mehreren PCs und mobilen Geräten verwendet.

</dd> </dl>

 

 
