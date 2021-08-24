---
description: Enumerationstypen, die mit der Datenträgerverwaltung verwendet werden.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Datenträgerverwaltungs-Enumerationstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e850e5161e4e8a6326d8014f67d6aad9373015e4354a01fa353087c6863a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765910"
---
# <a name="disk-management-enumeration-types"></a>Datenträgerverwaltungs-Enumerationstypen

Die folgenden Enumerationstypen werden bei der Datenträgerverwaltung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Enumeration                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_MEDIENTYP**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Stellt die verschiedenen Formen von Gerätemedien dar.<br/>                                                                                                                                                                                                                                                             |
| [**\_PARTITIONSSTIL**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Stellt das Format einer Partition dar.<br/>                                                                                                                                                                                                                                                                     |
| [**\_ \_ SPEICHERBUSTYP**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Stellt ein symbolisches Mittel zum Darstellen von Speicherbustypen bereit.<br/>                                                                                                                                                                                                                                              |
| [**\_INTEGRITÄTSSTATUS DER SPEICHERKOMPONENTE \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Gibt den Integritätsstatus einer Speicherkomponente an.<br/>                                                                                                                                                                                                                                                       |
| [**FORMFAKTOR DES \_ \_ SPEICHERGERÄTS \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Gibt den Formfaktor eines Geräts an.<br/>                                                                                                                                                                                                                                                                    |
| [**\_ \_ \_ SPEICHERGERÄTE-STROMVERSORGUNGSEINHEITEN \_**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Die Einheiten des maximalen Leistungsschwellenwerts.<br/>                                                                                                                                                                                                                                                                 |
| [**\_ \_ \_ SPEICHERPORTCODESATZ**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Ist für das System reserviert. <br/>                                                                                                                                                                                                                                                                                 |
| [**\_ \_ SPEICHEREIGENSCHAFTS-ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Listet die möglichen Werte des **PropertyId-Members** der [**STORAGE PROPERTY \_ \_ QUERY-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) auf, die als Eingabe an die [**IOCTL \_ STORAGE QUERY \_ \_ PROPERTY-Anforderung**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) übergeben werden, um die Eigenschaften eines Speichergeräts oder Adapters abzurufen.<br/> |
| [**\_ \_ SPEICHERPROTOKOLLTYP**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Gibt das Protokoll eines Speichergeräts an.<br/>                                                                                                                                                                                                                                                               |
| [**\_ \_ SPEICHERABFRAGETYP**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Wird von der [**STORAGE \_ PROPERTY \_ QUERY-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) verwendet, die an den [**IOCTL \_ STORAGE QUERY \_ \_ PROPERTY-Steuerelementcode**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) übergeben wird, um anzugeben, welche Informationen zu einer Eigenschaft eines Speichergeräts oder Adapters zurückgegeben werden.<br/>                             |
| [**WRITE \_ CACHE \_ CHANGE**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Gibt an, ob die Schreibcachefunktionen eines Geräts geändert werden können.<br/>                                                                                                                                                                                                                                    |
| [**WRITE \_ CACHE \_ ENABLE**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Gibt an, ob der Schreibcache aktiviert oder deaktiviert ist.<br/>                                                                                                                                                                                                                                                 |
| [**\_ \_ SCHREIBCACHETYP**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Gibt den Cachetyp an.<br/>                                                                                                                                                                                                                                                                                 |
| [**WRITE \_ THROUGH**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Gibt an, ob ein Speichergerät das Zwischenspeichern per Schreibzugriff unterstützt.<br/>                                                                                                                                                                                                                                        |



 

 

