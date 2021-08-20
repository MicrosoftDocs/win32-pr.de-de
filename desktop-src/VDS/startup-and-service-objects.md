---
description: VDS stellt Objekte zum Ausführen dienstbezogener Aktivitäten bereit. In diesem Thema werden die einzelnen Objekte beschrieben.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Start- und Dienstobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a87c7e52a263d03e80f44911f72db5f49259baf33a7b2f90680f30bb3b2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125930"
---
# <a name="startup-and-service-objects"></a>Start- und Dienstobjekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS stellt Objekte zum Ausführen dienstbezogener Aktivitäten bereit. In diesem Thema werden die einzelnen Objekte beschrieben.

## <a name="service-loader-object"></a>Service Loader-Objekt

Das Dienstladeprogrammobjekt stellt die Methoden bereit, die von Anwendungen zum Laden und Initialisieren von VDS verwendet werden. Um VDS für die Verwendung vorzubereiten, muss eine Anwendung die folgenden Vorgänge ausführen:

-   Erstellen Sie eine Instanz des Dienstladeprogrammobjekts, das die [**IVdsServiceLoader-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) zurückgibt.
-   Rufen Sie die [**IVdsServiceLoader::LoadService-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) auf, um den Dienst zu laden.

Ein Codebeispiel finden Sie unter [Laden von VDS.](loading-vds.md)

Lassen Sie immer zu, dass der Dienst vollständig initialisiert wird, bevor die Methoden aufgerufen werden, die vom Dienstobjekt verfügbar gemacht werden. Verwenden Sie die [**IVdsService::IsServiceReady-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) um den Status des Ladevorgangs zu bestimmen. Verwenden Sie die [**IVdsService::WaitForServiceReady-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) um Aufrufe von VDS-Objekten zu blockieren, bis die Initialisierung abgeschlossen ist.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.

| Typ                                              | Element                                         |
|---------------------------------------------------|-------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Zugeordnete Enumerationen                           | Keine.                                           |
| Zugeordnete Strukturen                             | Keine.                                           |



 

## <a name="service-object"></a>Dienstobjekt

Das Dienstobjekt ist ein flaches Objekt, das für alle VDS-Anwendungen von zentraler Bedeutung ist. Mit diesem Objekt kann ein Aufrufer die folgenden Vorgänge ausführen:

-   Bestimmen Sie den Status der Dienstinitialisierung.
-   Rufen Sie alle bei VDS registrierten Hardware- oder Softwareanbieter ab.
-   Bericht zu nicht zugeordneten Datenträgern.
-   Geben Sie den Dateisystemtyp und den Laufwerkbuchstaben zurück, die Volumes auf einem Datenträger zugeordnet sind.
-   Entfernen Sie nicht verwendeten Benutzermoduspfade und bereitgestellte Ordner aus der Registrierung, und aktualisieren Sie Datenträger.
-   Empfangen von VDS-Benachrichtigungen.
-   Starten Sie den Host neu.
-   Rufen Sie Fibre Channel HBA-Ports oder iSCSI-Initiatoradapter auf dem lokalen Computer ab.
-   Bereiten Sie LUNs, die als Datenträger auf dem lokalen Computer verfügbar gemacht werden, sicher für das Entfernen vor.

VDS-Benachrichtigungsstrukturen übergeben Objekt-GUIDs an alle Anwendungen, die beim VDS registriert sind, um Benachrichtigungen zu empfangen. Verwenden Sie die [**IVdsService::GetObject-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) um eine Objekt-GUID in einen Objektzeiger zu konvertieren. Eine ausführlichere Beschreibung des Benachrichtigungsmodells finden Sie unter [VDS-Benachrichtigungen.](vds-notification-model.md)

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| Typ                                                                   | Element                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Schnittstellen, die immer implementiert, aber nicht für Anwendungen verfügbar gemacht werden | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Zugeordnete Enumerationen                                                | [**VDS \_ \_ \_ ABFRAGEANBIETERFLAG,**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag) [**VDS-OBJEKTTYP, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_object_type) [**\_ VDS-DIENSTFLAG, \_**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) [**VDS-LAUFWERKBUCHSTABENFLAG, \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag) [**\_ VDS-DATEISYSTEMFLAG, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag) [**\_ \_ VDS-DATEISYSTEM-PROP-FLAG \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Zugeordnete Strukturen                                                  | [**VDS \_ \_DIENSTPROP,**](/windows/desktop/api/Vds/ns-vds-vds_service_prop) [**VDS \_ FILE SYSTEM \_ \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop) [**VDS FILE SYSTEM TYPE \_ \_ \_ \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop) [**VDS DRIVE LETTER \_ \_ \_ NOTIFICATION,**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) [**VDS FILE SYSTEM \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**VDS MOUNT POINT \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** Diese Schnittstellen werden erst Windows Server 2003 R2 unterstützt.

## <a name="initiator-adapter-object"></a>Initiatoradapterobjekt

Ein Initiatoradapterobjekt modelliert einen iSCSI-Initiatoradapter auf dem Hostcomputer des VDS-Diensts. Der VDS-Dienst kann initiator-Adapter nur auf dem lokalen Computer anzeigen. Die Rolle eines Initiatoradapterobjekts dient zum Verwalten von Anmeldesitzungen vom lokalen Computer zu iSCSI-Zielen.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| Typ                                              | Element                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Zugeordnete Enumerationen                           | [**VDS \_ \_ \_ ISCSI-ANMELDETYP.**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type) [**VDS \_ ISCSI \_ LOGIN \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**VDS \_ ISCSI \_ AUTH \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Zugeordnete Strukturen                             | [**VDS \_ \_ISCSI-INITIATORADAPTER- \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows Server 2003:** Diese Schnittstelle wird erst Windows Server 2003 R2 unterstützt.

## <a name="initiator-portal-object"></a>Initiator-Portalobjekt

Ein Initiatorportalobjekt modelliert ein iSCSI-Initiatorportal auf einem iSCSI-Initiator. Ein Initiatorportal ist die Kombination aus IP-Adresse und Port, über die ein Hostcomputer eine Verbindung mit einem Portal in einem iSCSI-Subsystem herstellt. Die Rolle eines Initiatorportalobjekts besteht darin, als einer der Endpunkte eines MPIO-Pfads zu fungieren und IPSEC-Sicherheitseinstellungen zu konfigurieren.

In der folgenden Tabelle sind die zugehörigen Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| Typ                                              | Element                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Zugeordnete Enumerationen                           | [**VDS \_ \_ISCSI-IPSEC-FLAG \_**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Zugeordnete Strukturen                             | [**VDS \_ \_ISCSI-INITIATORPORTAL \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**VDS \_ ISCSI \_ IPSEC \_ KEY**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**VDS \_ IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** Diese Schnittstelle wird erst Windows Server 2003 R2 unterstützt.

## <a name="hba-port-object"></a>HBA-Portobjekt

Das HBA-Portobjekt modelliert einen Fibre Channel HBA-Port (Host Bus Adapter).

Verwenden Sie die [**IVdsServiceHba::QueryHbaPorts-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) um die HBA-Ports zu bestimmen, die VDS auf dem lokalen Computer bekannt sind.

In der folgenden Tabelle sind die zugehörigen Schnittstellen, Enumerationen und Strukturen aufgeführt.

| Typ                                              | Element                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Zugeordnete Enumerationen                           | [**VDS \_ \_HBAPORT-TYP,**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type) [**VDS \_ HBAPORT-STATUS, \_**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status) [**VDS \_ HBAPORT-GESCHWINDIGKEITSFLAG \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Zugeordnete Strukturen                             | [**VDS \_ HBAPORT \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** Diese Schnittstelle wird erst Windows Server 2003 R2 unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Laden von VDS](loading-vds.md)
</dt> <dt>

[**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[VDS-Benachrichtigungen](vds-notification-model.md)
</dt> </dl>

 

 
