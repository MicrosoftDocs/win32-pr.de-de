---
description: Windows Management Infrastructure (WMI), Management Instrumentation (MI) und Open Management Infrastructure (OMI) verwenden alle MOF-Dateien (Management Object Format), um die Informationen zu beschreiben, die von den jeweiligen Anbietern zur Verfügung gestellt werden.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: WMI/MI/OMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682629f72da94cd2210fb781284a7cb4cf7f85868ff405f22727e619d128ae65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992417"
---
# <a name="wmimiomi-providers"></a>WMI/MI/OMI-Anbieter

Windows Management Infrastructure (WMI), Management Instrumentation (MI) und Open Management Infrastructure (OMI) verwenden alle MOF-Dateien (Management Object Format), um die Informationen zu beschreiben, die von den jeweiligen Anbietern zur Verfügung gestellt werden.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

Der Active Directory-Anbieter, auch als DS-Anbieter (Directory Services) bezeichnet, ordnet WMI Active Directory-Objekte zu. Durch Den Zugriff auf den LDAP-Namespace (Lightweight Directory Access Protocol) in WMI können Sie in Active Directory auf ein Objekt verweisen oder es als Alias festlegen.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Anwendungsbestand](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

Die WMI-Klassen für die Anwendungsinventur ermöglichen die Ermittlung der installierten Win32-Anwendungen und Windows Speichern von Anwendungen auf einem Windows System.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Anwendungsproxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

Anwendungsproxy WMI-Anbieter ermöglicht Entwicklern den Zugriff auf den Web Anwendungsproxy-Dienst, damit Administratoren Anwendungen für den externen Zugriff veröffentlichen können. Web Anwendungsproxy ist ein Reverseproxy für Active Directory-Verbunddienste (AD FS) (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker-Laufwerkverschlüsselung (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Bietet Konfiguration und Verwaltung für einen Speicherbereich auf einem Festplattenlaufwerk, dargestellt durch eine Instanz von [**Win32 \_ EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), die durch Verschlüsselung geschützt werden kann.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[Bits](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

Der Background Intelligent Transfer Service Compact Server (BITS) mit BITS-Remoteverwaltung ermöglicht authentifizierten Administratoren oder Controlleranwendungen, BITS-Übertragungsaufträge remote zu erstellen, zu ändern und zu verwalten, ohne den Internetinformationsdienste-Dienst (IIS) zu verwenden.

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[Biztalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Bietet Zugriff auf die BizTalk-Verwaltungsobjekte, die durch WMI-Klassen dargestellt werden.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Startkonfigurationsdaten](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

Der Startkonfigurationsdaten (BCD) stellt einen Speicher zur Verfügung, der zum Beschreiben von Startanwendungen und Startanwendungseinstellungen verwendet wird.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Startereignissammler](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

Der WMI-Anbieter für den Startereignissammler bietet Zugriff auf Verbindungs- und Konfigurationsinformationen für das Setup- und Startereignissammlungsfeature auf Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Energieverwaltungsereignisse](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

Die CIMWin32-Anbieter unterstützen die in CimWin32.dll implementierten Klassen und bestehen aus den cim-Kernklassen, der Win32-Implementierung dieser Klassen und Energieverwaltungsereignissen.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

Der CIMWin32a-Anbieter erweitert die in [CIMWin32 verfügbaren Klassen.](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

Der DcbQosCim-Anbieter unterstützt Klassen, die Netzwerk-QOS-Einstellungsdaten, Steuerungseinstellungsdaten und Datenverkehrsklasseneinstellungsdaten beschreiben.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[verteiltes Dateisystem (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

Der DFS-Anbieter stellt skriptfähige DFS-Funktionen über WMI zur Verfügung.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[verteiltes Dateisystem Replikation (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Erstellt Tools zum Konfigurieren und Überwachen des verteiltes Dateisystem [(DFS)-Diensts.](/previous-versions/windows/desktop/dfs/distributed-file-system) Weitere Informationen finden Sie unter [DFSR-WMI-Klassen.](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

Der [Dfsncimprov-Anbieter](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) unterstützt Klassen, die den DFS-Namespacezugriff implementieren.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

Der [DhcpServerPSProvider-Anbieter](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) unterstützt Klassen, die mit einem DHCP-Server (Dynamic Host Configuration Protocol) interagieren.

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Datenträgerkontingent](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

Mit Windows Datenträgerkontingentanbieter können Administratoren die Datenmenge steuern, die jeder Benutzer in einem NTFS-Dateisystem speichert.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

Der DTC-Anbieter ermöglicht die Verwaltung des DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[Dns](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Ermöglicht Administratoren und Programmierern das Konfigurieren Domain Name System (DNS)-Ressourceneinträgen (RRs) und DNS-Servern mithilfe von WMI.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim-Anbieterklassen](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

Der Dnsclientcim-Anbieter unterstützt Klassen, die mit einem Domain Name System (DNS)-Client interagieren.

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

Der [DnsClientPSProvider-Anbieter](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) unterstützt WMI-Klassen, die mit einem DNS-Client interagieren.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

Der [DnsServerPSProvider-Anbieter](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) unterstützt WMI-Klassen, die mit einem DNS-Server interagieren.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

Der [Ereignisprotokollanbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider) bietet Zugriff auf Daten aus dem Ereignisprotokolldienst und Benachrichtigungen über Ereignisse.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Ereignisablaufverfolgungsverwaltung](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

Der Anbieter für die Ereignisablaufverfolgungsverwaltung bietet Zugriff auf Die Ereignisablaufverfolgung für Windows (ETW) für die automatische Protokollierung von Sitzungskonfigurationen und Ablaufverfolgungsereignissen.

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Aktualisieren](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

Der Failover Cluster-Aware Updating (CAU)-Anbieter unterstützt die Koordination und Verwaltung von CAU.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Hyper-V-Failoverclustering](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

Der Hyper-V-Anbieter für Failoverclustering ermöglicht die Verwaltung und Berichterstellung von Hyper-V in einer Clusteringumgebung.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failoverclustering Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

Der Failoverclustering-Storage Quality of Service (QoS)-Anbieter ermöglicht die Verwaltung und Berichterstellung der Clusteringspeicher-QoS-Richtlinien.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failovercluster V1-Anbieter](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

Der Failovercluster-V1-Anbieter ermöglicht die Verwaltung eines Failoverclusters.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failovercluster V1-Erweiterungen](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

Der Failoverclustererweiterungsanbieter bietet zusätzliche Verwaltung eines Failoverclusters.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Systemüberwachung](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

Der Gateway-Systemüberwachung verwaltet Ereignisse und Informationen zur Überwachung der Gatewayzustandsüberwachung.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Gruppenrichtlinie-API](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

Der Gruppenrichtlinie ermöglicht die richtlinienbasierte Verwaltung mithilfe von Microsoft Active Directory-Verzeichnisdiensten (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host-Wächterdienst](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

Der Host-Wächterdienst-Anbieter ermöglicht die Verwaltung des Host-Wächterdiensts für abgeschirmte VMs.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

Mit dem Hyper-V-Anbieter können Sie Informationen zu virtuellen Computern verwalten und abrufen.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

Der Hyper-V-Anbieter (V2) erweitert den [Hyper-V-Anbieter.](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internetinformationsdienste (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Macht Programmierschnittstellen verfügbar, die zum Abfragen und Konfigurieren der IIS-Metabasis verwendet werden können.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Internetprotokoll-Adressverwaltungsserver (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

Der IPAM-Serveranbieter ermöglicht Entwicklern die Verwaltung IPAM WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP-Routenanbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

Der vorinstallierte IP-Routenanbieter stellt IPV4-Netzwerkroutinginformationen bereit, einschließlich (aber nicht beschränkt auf) der Informationen, die über den **Routendruckbefehl verfügbar** sind.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Stellt IPMI-Daten aus BMC-Vorgängen (Baseboard Management Controller) zur Verfügung.

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI-Zielserver](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

Der iSCSI-Zielserver-Anbieter unterstützt eine WMI-Schnittstelle für die Verwaltung der Microsoft iSCSI-Zielserver, z. B. das Erstellen virtueller Datenträger und deren Präsentation für den Client.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Auftragsobjekt](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

Der Auftragsobjektanbieter unterstützt den Zugriff auf Daten zu benannten Kernelauftragsobjekten.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel-Ablaufverfolgung](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

Mit dem vorinstallierten Kernel Trace-Ereignisanbieter können Sie Kernel-Ablaufverfolgungsereignisse für Prozesserstellung, Prozessbeendigung, Threaderstellung, Threadbeendigung und Modulauslastung sehen.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Stellt Klassen zum Erstellen, Registrieren, Konfigurieren und Verwalten benutzerdefinierter SESSION-Anwendungen (Session Initiation Protocol) mit [Live Communications Server 2003 zur Verfügung.](/previous-versions/office/aa194012(v=office.11))

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registrierung der Verwaltungstools](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

Der Registrierungsanbieter der Verwaltungstools bietet Remotezugriff auf die Registrierung.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Verwaltungstools Task-Manager](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

Der Verwaltungstools Task-Manager anbieter ermöglicht den Zugriff und die Verwaltung der Task-Manager Daten.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM-Anwendung](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

Der Mobile Geräteverwaltung (MDM)-Anwendungsanbieter verwaltet Anwendungen auf Geräten, die den MDM-Dienst abonniert haben.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM-Brücke](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

Der MDM-Bridge-Anbieter ermöglicht die MDM-Verwaltung einer Netzwerk-Bridge.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM-Einstellungen](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

Der MDM Einstellungen Anbieter ermöglicht die Verwaltung von Einstellungen auf Geräten, die bei einem MDM-Dienst registriert sind.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

Der [MSFT \_ PCSVDevice-Anbieter](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) macht eine Klasse verfügbar, die eine Ansichtsklasse für ein physisches Computersystem definiert.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

Der Abschnitt [MsNetImPlatform-Anbieter](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) enthält Referenzinformationen zu In NdisIMPlatCim.dll implementierten MsNetImPlatform-Anbieterklassen.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

Der [NetAdapterCim-Anbieter](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) unterstützt Klassen, die auf Netzwerkadapter zugreifen.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

Dieser Abschnitt enthält Referenzinformationen zu [NetDaCim-Anbieterklassen.](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Stellt Referenzinformationen für [NetNcCim-Anbieterklassen](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) bereit.

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

Der [NetPeerDist-Anbieter](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) unterstützt Klassen, die mit der BranchCache-Infrastruktur interagieren.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

Der [NetQosCim-Anbieter](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) stellt Daten für QoS-Einstellungsdaten (Quality of Service) und QoS-Einstellungsdaten bereit.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

Dieser Abschnitt enthält Referenzinformationen zu NetSwitchTeam-Anbieterklassen, die in NetSwitchTeam.mof deklariert und in NetSwitchTeamCim.dll implementiert wurden.

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

Der NetTCPIP-Anbieter unterstützt Klassen, die mit TCPIP-Verbindungen interagieren.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

Dieser Abschnitt enthält Referenzinformationen zu NetTtCim-Anbieterklassen, die in NetTtCim.mof definiert und in NetTtCim.dll implementiert sind.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

Der NetWNV-Anbieter unterstützt Klassen, die mit Net Virtualization-Technologien interagieren.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Netzwerkzugriffsschutz](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

Der Netzwerkzugriffsschutz-Anbieter macht eine Plattform für den geschützten Zugriff auf private Netzwerke verfügbar.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Netzwerklastenausgleich](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

Der Netzwerklastenausgleichsanbieter (NETWORK Load Balancing, NLB) ermöglicht die Verwaltung eines NLB-Clusters.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController-Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht die Verwaltung eines Netzwerkcontrollerservers.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[Nfs](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

Mit dem Anbieter für NFS können Sie Tools und Skripts zum Konfigurieren und Überwachen des Windows Network File System erstellen.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

Der Ping-Anbieter bietet Zugriff auf die Statusinformationen, die vom Ping-Standardbefehl bereitgestellt werden.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Politik](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Stellt Erweiterungen für Gruppenrichtlinien bereit und ermöglicht Optimierungen bei der Anwendung der Richtlinie.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Stromzähler](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

Der Anbieter von Stromzählern unterstützt die Schnittstelle "Power Metering and Budgeting" (PMB). Diese Klassen sind die primäre Schnittstelle für die Abfrage von PMI-Informationen (Power Meter Interface) von zugrunde liegenden Stromzählern im System.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Energierichtlinie](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

Der Power Policy-Anbieter bietet Klassen die Möglichkeit, die gesamte Energierichtlinieninfrastruktur remote zu verwalten.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

Der [RAMgmtPSProvider-Anbieter](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) stellt Klassen zum Verwalten des Remotezugriffs bereit.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

Der [RAServerPSProvider-Anbieter](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) stellt Klassen zum Verwalten des Rasservers bereit.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

Der [ReliabilityMetricsProvider-Anbieter](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) macht System- und Windows Zuverlässigkeitsmetriken des Ereignisprotokolls verfügbar.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remotedesktopdienste](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Ermöglicht eine konsistente Serververwaltung in einer Remotedesktopdienste Umgebung.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Definiert Klassen, mit denen Sie Skripts und Code schreiben können, um die Einstellungen des Berichtsservers und der Berichts-Manager zu ändern.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Resultsant Set of Policy (RSoP) (Ergebnissatz der Richtlinie (RSoP))](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Stellt Methoden zum Planen und Debuggen von Richtlinieneinstellungen in einer Was-wäre-wenn-Situation bereit. Mit diesen Methoden können Administratoren ganz einfach die Kombination von Richtlinieneinstellungen bestimmen, die für einen Benutzer oder Computer gelten oder für diesen gelten. Dies wird als Resultant Set of Policy (RSoP) bezeichnet. Weitere Informationen finden Sie unter [Informationen zum RSoP-WMI-Methodenanbieter](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) und den [RSoP-WMI-Klassen.](/previous-versions/windows/desktop/Policy/rsop-wmi-classes)

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Sicherheit](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Ruft Sicherheitseinstellungen ab, die den Besitz, die Überwachung und die Zugriffsrechte für Dateien, Verzeichnisse und Freigaben steuern, oder ändert diese.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) macht Bereitstellungsfunktionen verfügbar.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sitzung](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Verwaltet Netzwerksitzungen und -verbindungen.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Schattenkopie](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Stellt Verwaltungsfunktionen für die Schattenkopien des Features Freigegebene Ordner zur Verfügung.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Bereitstellung abgeschirmter VMs](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

Der Anbieter für die Bereitstellung abgeschirmter VMs ermöglicht einem Fabric-Controller, die sichere Bereitstellung einer abgeschirmten VM auf einem Hyper-V-Host zu starten.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Bereitstellungsdienst für abgeschirmte VMs](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht die Bereitstellung eines abgeschirmten virtuellen Computers.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB-Verwaltung](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

Der SMB-Verwaltungs-API stellt Klassen und Methoden zum Verwalten von Freigaben und zum Freigeben des Zugriffs bereit.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[Snmp](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Karten SNMP-Objekte (Simple Network Management Protocol), die in MIB-Schemaobjekten (Management Information Base) für Klassen definiert sind. Weitere Informationen finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment)

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Protokollierung des Softwarebestands](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

Der Anbieter der Protokollierung des Softwarebestands sammelt Lizenzierungsdaten zu Software, die auf einem Windows Server installiert ist, und bietet Remotezugriff auf die Daten, sodass sie problemlos von einem Rechenzentrum aggregiert werden können.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Softwarelizenzierung für Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Softwarelizenzierungsklassen, die](/previous-versions/windows/desktop/sppwmi/software-license-provider-) für Windows Vista verwendet werden.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Softwarelizenz](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

Der Softwarelizenzierungsanbieter ruft Softwarelizenzierungsdaten ab.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volumen](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

Der Storage Volumeanbieter stellt Volumeverwaltungsfunktionen bereit.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Replikat](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht die Verwaltung eines Speicherreplikats.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Systemregistrierung](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

Der Systemregistrierungsanbieter ermöglicht Verwaltungsanwendungen das Abrufen und Ändern von Daten in der Systemregistrierung sowie das Empfangen von Benachrichtigungen, wenn Änderungen auftreten.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Systemwiederherstellung](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Stellt Klassen bereit, die die Systemwiederherstellungsfunktionen konfigurieren und verwenden. Weitere Informationen finden Sie unter [Konfigurieren der Systemwiederherstellung](/windows/desktop/sr/configuring-system-restore) und der WMI-Klassen für die [Systemwiederherstellung.](/windows/desktop/sr/system-restore-wmi-classes)

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

Ermöglicht den Zugriff auf Daten über ein Sicherheitsgerät, dargestellt durch eine Instanz von [**Win32 \_ TPM,**](/windows/desktop/SecProv/win32-tpm)das der Vertrauensstamm für ein Microsoft Windows vertrauenswürdiges Plattformcomputersystem ist.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

Der [Trustmon-Anbieter](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) ist ein Instanzanbieter, der Klassen mit Informationen zu den Vertrauensstellungen zwischen Domänen erstellt.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Benutzerzugriffsprotokollierung](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

Die Benutzerzugriffsprotokollierung (User Access Logging, UAL) ist ein gängiges Framework für Windows Serverrollen, um ihre jeweiligen Nutzungsmetriken zu melden.

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

Der [UserProfileProvider-Anbieter](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) macht Klassen verfügbar, die Informationen zu einem Benutzerprofil auf einem Windows System sowie den Integritätsstatus eines umgeleiteten Benutzerordners bereitstellen.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Verwaltung des Benutzerzustands](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

Der Benutzerzustandsverwaltungsanbieter macht eine Verwaltungs- und Berichterstellungs-API für Unternehmensszenarien verfügbar.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[ansehen](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Erstellt neue Instanzen und Methoden basierend auf Instanzen anderer Klassen. Zwei Versionen des View-Anbieters sind auf 64-Bit-Plattformen verfügbar.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

Der [VPNClientPSProvider-Anbieter](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) macht eine Plattform zum Automatisieren der Konnektivität mit einem virtuellen privaten Netzwerkclient verfügbar.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[Wdm](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

Bietet Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardwaretreibern, die dem Windows Driver Model (WDM) entsprechen.

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

Der [WFasCim-Anbieter](/previous-versions/windows/desktop/wfascimprov/network-security-classes) macht Netzwerksicherheits- und Filterfunktionen verfügbar.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

Der [WhqlProvider-Anbieter](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) macht Informationen zu digitalen Signaturen zu Treibern verfügbar.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

Der [Win32ClockProvider-Anbieter](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) macht die aktuellen, lokalen und UTC-basierten Zeitstempel auf einem Computersystem verfügbar.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Datenzugriffskomponenten (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Stellt die Verwaltung von WDAC bereit.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

Der Windows Defender-Anbieter macht Windows Defender Sicherheitsfeatures verfügbar.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

Der Windows Installer-Anbieter, der auch als MSI-Anbieter bezeichnet wird, ermöglicht Anwendungen den Zugriff auf Informationen, die von Windows Installer-kompatiblen Anwendungen gesammelt wurden.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Produktaktivierung](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

Der WPA-Anbieter (Windows Product Activation) ist eine Antiskopierungstechnologie, die darauf abzielt, das gelegentliche Kopieren von Software zu reduzieren.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server-Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

Der Anbieter ermöglicht den Zugriff auf und die Verwaltung der Konfiguration, die von der Server-Manager Anwendung gesteuert wird.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

Der MsftStrgMan-Anbieter ermöglicht die Verwaltung von Speichersystemen auf Windows Server-Produkten.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

Der StrgMgmt-Anbieter kann verwendet werden, um eine Vielzahl von Speicherkonfigurationen zu verwalten, von Tablets bis hin zu externen Speicherarrays auf Servern.

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows Systembewertungstool](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

Das Windows System Assessment Tool (WinSAT) macht eine Reihe von Klassen verfügbar, die die Leistungsmerkmale und Funktionen eines Computers bewerten.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

Der WMI Core-Anbieter definiert Klassen, die die Kernfunktionalität von WMI bilden.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

Der [Anbieter Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) unterstützt Anbieter.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32 \_ Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

Die abstrakte [**Win32 \_ Perf-Klasse**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) ist die Basisklasse für die Leistungsindikatorklassen [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) und [**Win32 \_ PerfFormattedData.**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov) Sie definiert die erforderlichen Zeitstempel- und Häufigkeitseigenschaften, die in den CounterType-Algorithmen für die Leistungsindikatorklassen verwendet werden.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Eine abstrakte Basisklasse für die vorinstallierten, berechneten Datenklassen.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

Die Leistungsindikatorklasse [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) ist die abstrakte Basisklasse für alle konkreten unformatierten Leistungsindikatorklassen. Um im Systemmonitor angezeigt zu werden, müssen Leistungsindikatorklassen dem Namespace "Root \\ CIMv2" hinzugefügt und von **Win32 \_ PerfRawData** abgeleitet werden.

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Erstellt die [WMI-Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes). Daten werden diesen Leistungsklassen dynamisch vom WMIPerfInst-Anbieter bereitgestellt.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Stellt unformatierte und formatierte Leistungsindikatordaten dynamisch aus Definitionen der [Leistungsindikatorklasse zur](/windows/desktop/CIMWin32Prov/performance-counter-classes) Verfügung.

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Arbeitsordner](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

Arbeitsordner wird verwendet, um Dateien mit mehreren PCs und mobilen Geräten zu synchronisieren.

</dd> </dl>

 

 
