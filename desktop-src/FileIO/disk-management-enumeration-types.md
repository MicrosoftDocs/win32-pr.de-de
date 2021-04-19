---
description: Mit der Datenträgerverwaltung verwendete Enumerationstypen.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Enumerationstypen der Datenträgerverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c186a2a722bf9614bb83b19bcaa29be486cf54bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362637"
---
# <a name="disk-management-enumeration-types"></a>Enumerationstypen der Datenträgerverwaltung

Die folgenden Enumerationstypen werden mit der Datenträgerverwaltung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Enumeration                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Medientyp**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Stellt die verschiedenen Formen von Geräte Medien dar.<br/>                                                                                                                                                                                                                                                             |
| [**Partitions \_ Stil**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Stellt das Format einer Partition dar.<br/>                                                                                                                                                                                                                                                                     |
| [**\_ \_ speicherbustyp**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Stellt eine symbolische Methode zum Darstellen von Speicherbus Typen bereit.<br/>                                                                                                                                                                                                                                              |
| [**Integritäts Status der Speicher \_ Komponente \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Gibt den Integritäts Status einer Speicherkomponente an.<br/>                                                                                                                                                                                                                                                       |
| [**\_ \_ Form \_ Faktor des Speichergeräts**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Gibt den Formfaktor eines Geräts an.<br/>                                                                                                                                                                                                                                                                    |
| [**\_ \_ Energie \_ Deckungs \_ Einheiten für Speichergeräte**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Die Einheiten des maximalen Schwellenwerts für die Stromversorgung.<br/>                                                                                                                                                                                                                                                                 |
| [**\_Speicherport \_ - \_ Codesatz**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Ist für das System reserviert. <br/>                                                                                                                                                                                                                                                                                 |
| [**Speicher eigen \_ schafts- \_ ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Listet die möglichen Werte des **PropertyId** -Members der [**Speicher \_ Eigenschaften- \_ Abfrage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) Struktur auf, die als Eingabe an die [**IOCTL- \_ Speicher \_ Abfrage \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) -Eigenschaften Anforderung weitergegeben wurde, um die Eigenschaften eines Speichergeräts oder eines Adapters abzurufen.<br/> |
| [**Speicher \_ \_ Protokolltyp**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Gibt das Protokoll eines Speichergeräts an.<br/>                                                                                                                                                                                                                                                               |
| [**Speicher \_ \_ Abfragetyp**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Wird von der [**\_ \_ Abfrage Struktur der Speicher Eigenschaften**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) verwendet, die an den Steuercode der [**Eigenschaft der IOCTL- \_ Speicher \_ Abfrage \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) übermittelt wird, um anzugeben, welche Informationen über eine Eigenschaft eines Speichergeräts oder eines Adapters zurückgegeben werden<br/>                             |
| [**\_Cache \_ Änderung schreiben**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Gibt an, ob die Schreib Cache Funktionen eines Geräts änderbar sind.<br/>                                                                                                                                                                                                                                    |
| [**Schreib \_ Cache \_ aktivieren**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Gibt an, ob der Schreib Cache aktiviert oder deaktiviert ist.<br/>                                                                                                                                                                                                                                                 |
| [**Schreib \_ \_ Cachetyp**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Gibt den Cachetyp an.<br/>                                                                                                                                                                                                                                                                                 |
| [**Schreiben \_ durch**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Gibt an, ob ein Speichergerät das Schreiben Zwischenspeichern unterstützt.<br/>                                                                                                                                                                                                                                        |



 

 

