---
description: VDS stellt Objekte zum Ausführen Dienst bezogener Aktivitäten bereit. In diesem Thema werden die einzelnen-Objekte beschrieben.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Start-und Dienst Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359558"
---
# <a name="startup-and-service-objects"></a>Start-und Dienst Objekte

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS stellt Objekte zum Ausführen Dienst bezogener Aktivitäten bereit. In diesem Thema werden die einzelnen-Objekte beschrieben.

## <a name="service-loader-object"></a>Service Loader-Objekt

Das Dienst Lade Programm-Objekt stellt die Methoden bereit, die von Anwendungen zum Laden und Initialisieren von VDS verwendet werden. Um VDS für die Verwendung vorzubereiten, muss eine Anwendung die folgenden Vorgänge ausführen:

-   Erstellen Sie eine Instanz des Service Loader-Objekts, das die [**ivdsserviceloader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) -Schnittstelle zurückgibt.
-   Um den Dienst zu laden, wenden Sie die [**ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) -Methode an.

Ein Codebeispiel finden Sie unter [Laden von VDS](loading-vds.md).

Gestatten Sie immer, dass der Dienst vollständig initialisiert wird, bevor Sie die Methoden aufrufen, die vom Dienst Objekt verfügbar gemacht werden. Verwenden Sie die [**ivdsservice:: isserviceready**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) -Methode, um den Status des Ladevorgangs zu bestimmen. Verwenden Sie die [**ivdsservice:: waitforserviceready**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) -Methode, um Aufrufe von VDS-Objekten zu blockieren, bis die Initialisierung abgeschlossen ist.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.

| type                                              | Element                                         |
|---------------------------------------------------|-------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsserviceloader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Zugehörige Enumerationen                           | Keine.                                           |
| Zugeordnete Strukturen                             | Keine.                                           |



 

## <a name="service-object"></a>Dienst Objekt

Das Dienst Objekt ist ein multifunktionales Objekt, das für alle VDS-Anwendungen von zentraler Bedeutung ist. Mit diesem Objekt kann ein Aufrufer die folgenden Vorgänge ausführen:

-   Bestimmen Sie den Status der Dienst Initialisierung.
-   Ruft alle Hardware-oder Softwareanbieter ab, die bei VDS registriert sind.
-   Bericht über nicht zugeordnete Datenträger.
-   Gibt den Dateisystemtyp und den Laufwerk Buchstaben zurück, die Volumes auf einem Datenträger zugeordnet sind.
-   Entfernen nicht verwendeter benutzermoduspfade und bereitgestellter Ordner aus der Registrierung und Aktualisieren von Datenträgern.
-   Empfangen von VDS-Benachrichtigungen.
-   Starten Sie den Host neu.
-   Rufen Sie Fibre Channel HBA-Ports oder iSCSI-Initiator-Adapter auf dem lokalen Computer ab.
-   Sicheres Vorbereiten von LUNs, die als Datenträger auf dem lokalen Computer verfügbar gemacht werden, zum Entfernen

VDS-Benachrichtigungs Strukturen übergeben Objekt-GUIDs an alle Anwendungen, die mit VDS registriert sind, um Benachrichtigungen zu empfangen. Verwenden Sie die [**ivdsservice:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) -Methode, um eine Objekt-GUID in einen Objekt Zeiger zu konvertieren. Eine ausführlichere Beschreibung des Benachrichtigungs Modells finden Sie unter [VDS-Benachrichtigungen](vds-notification-model.md).

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet. 

| type                                                                   | Element                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                      | [**Ivdsservice**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**ivdsservicehba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**ivdsserviceiscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**ivdsserviceuninstalldisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Schnittstellen, die immer implementiert, aber nicht für Anwendungen verfügbar gemacht werden | [**Ivdsadmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Zugehörige Enumerationen                                                | [**VDS \_ \_ \_ Flag für Abfrage Anbieter**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**VDS- \_ \_ Objekttyp**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**VDS- \_ \_ Dienstflag**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), [**VDS- \_ \_ laufwerkbuchstabungsflag \_**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), [**VDS- \_ \_ dateisystemflag \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), [**VDS- \_ \_ dateisystemprop \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag)                                                      |
| Zugeordnete Strukturen                                                  | [**VDS \_ Dienst \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**VDS \_ - \_ Datei \_ System Stütze**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), [**VDS- \_ Datei \_ \_ Systemtyp- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), [**VDS- \_ Laufwerk \_ Buchstaben \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), [**VDS- \_ Datei \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), VDS-Bereitstellungs [**\_ \_ Punkt \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** diese Schnittstellen werden bis Windows Server 2003 R2 nicht unterstützt.

## <a name="initiator-adapter-object"></a>Initiator-Adapter Objekt

Ein Initiator-Adapter Objekt modelliert einen iSCSI-Initiator-Adapter auf dem Host Computer des VDS-Diensts. Der VDS-Dienst kann nur Initiator-Adapter auf dem lokalen Computer anzeigen. Die Rolle eines initiatoradapterobjekts besteht in der Verwaltung von Anmelde Sitzungen vom lokalen Computer zu iSCSI-Zielen.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet. 

| type                                              | Element                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsiscsiinitiatoradapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Zugehörige Enumerationen                           | [**VDS \_ der iSCSI- \_ \_ Anmeldetyp**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ iSCSI \_ - \_ Anmeldungs**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag)Kennzeichen, [**VDS- \_ iSCSI- \_ \_ Authentifizierungstyp**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Zugeordnete Strukturen                             | [**VDS \_ der iSCSI- \_ Initiator- \_ Adapter \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows Server 2003:** diese Schnittstelle wird bis Windows Server 2003 R2 nicht unterstützt.

## <a name="initiator-portal-object"></a>Initiator-Portal Objekt

Ein Objekt des Initiator-Portals modelliert ein iSCSI-Initiator-Portal auf einem iSCSI-Initiator. Ein Initiator-Portal ist die Kombination aus IP-Adresse und Port, über die ein Host Computer eine Verbindung mit einem Portal in einem iSCSI-Subsystem herstellt. Die Rolle eines Initiator-Portal Objekts besteht darin, als einer der Endpunkte eines MPIO-Pfads zu fungieren und die IPSec-Sicherheitseinstellungen zu konfigurieren.

In der folgenden Tabelle sind die verknüpften Schnittstellen, Enumerationen und Strukturen aufgeführt. 

| type                                              | Element                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsiscsiinitiatorportal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Zugehörige Enumerationen                           | [**VDS \_ iSCSI- \_ IPSec- \_ Flag**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Zugeordnete Strukturen                             | [**VDS \_ unter \_ \_ \_ Stützung des iSCSI-Initiator-Portals**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**VDS- \_ iSCSI- \_ IPSec- \_ Schlüssel**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**VDS- \_ IPAddress**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** diese Schnittstelle wird bis Windows Server 2003 R2 nicht unterstützt.

## <a name="hba-port-object"></a>HBA-Port Objekt

Das HBA-Port Objekt modelliert einen Fibre Channel HBA-Port (Hostbus Adapter).

Verwenden Sie die [**ivdsservicehba:: queryhbapbrüche**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) -Methode, um die HBA-Ports zu bestimmen, die VDS auf dem lokalen Computer bekannt sind.

In der folgenden Tabelle sind die verknüpften Schnittstellen, Enumerationen und Strukturen aufgeführt.

| type                                              | Element                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdshbaport**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Zugehörige Enumerationen                           | [**VDS \_ HBAPORT \_**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**VDS \_ HBAPORT \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**VDS \_ HBAPORT \_ Speed \_ Flag**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Zugeordnete Strukturen                             | [**VDS \_ HBAPORT- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** diese Schnittstelle wird bis Windows Server 2003 R2 nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[**Ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[VDS werden geladen](loading-vds.md)
</dt> <dt>

[**Ivdsservice:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[VDS-Benachrichtigungen](vds-notification-model.md)
</dt> </dl>

 

 
