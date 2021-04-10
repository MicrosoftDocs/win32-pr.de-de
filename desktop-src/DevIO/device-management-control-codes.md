---
description: Die folgenden Steuerungs Codes werden für Wechsler-Geräte verwendet.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Steuerungs Codes für die Geräteverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041486"
---
# <a name="device-management-control-codes"></a>Steuerungs Codes für die Geräteverwaltung

Die folgenden Steuerungs Codes werden für Wechsler-Geräte verwendet.



| Wert                                                                                          | Bedeutung                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOCTL- \_ Wechsler \_ Austausch \_ Mittel**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Verschiebt ein Medien Medium von einem Quell Element in ein Ziel und das Medienobjekt, das sich ursprünglich am ersten Ziel an ein zweites Ziel befand. |
| [**IOCTL- \_ Wechsler \_ get- \_ Element \_ Status**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Ruft den Status aller Elemente oder eine angegebene Anzahl von Elementen eines bestimmten Typs ab.                                                         |
| [**IOCTL- \_ Wechsler \_ get- \_ Parameter**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Ruft die Parameter des angegebenen Geräts ab.                                                                                                    |
| [**IOCTL- \_ Wechsler \_ get \_ Product \_ Data**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Ruft die Produktdaten für das angegebene Gerät ab.                                                                                                 |
| [**IOCTL- \_ Wechsler \_ get- \_ Status**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Ruft den aktuellen Status des angegebenen Geräts ab.                                                                                                |
| [**IOCTL- \_ Wechsler \_ Initialisieren des \_ Element \_ Status**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Initialisiert den Status aller Elemente oder der angegebenen Elemente eines bestimmten Typs.                                                               |
| [**IOCTL- \_ Wechsler, \_ \_ Mittel**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Verschiebt ein Medien Medium in ein Ziel.                                                                                                             |
| [**IOCTL- \_ Wechsler- \_ abfragenvolumes \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Ruft die volumetaginformationen für die angegebenen Elemente ab.                                                                                     |
| [**IOCTL- \_ Wechsler \_ Reinitialisieren des \_ Transports**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Physisch wiederholen Sie ein Transport Element.                                                                                                         |
| [**Zugriff auf IOCTL- \_ Wechsler \_ festlegen \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Legt den Zustand des Einfügevorgangs, der Tür oder der Tastatur auf dem Gerät fest.                                                                                   |
| [**Position des IOCTL- \_ Wechsler \_ Satzes \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Legt den Roboter Transportmechanismus des Wechsler auf die angegebene Element Adresse fest.                                                                     |



 

Die folgenden Steuerungs Codes werden bei der Geräteverwaltung verwendet.



| Steuerungs Code                                                                                      | Vorgang                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Überprüfung der IOCTL- \_ Speicher \_ Überprüfung \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Hiermit wird überprüft, ob ein Wechselmedien Gerät geändert wurde.                                                               |
| [**IOCTL- \_ Speicher- \_ eject- \_ Medien**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Das Medium wird von einem SCSI-Gerät ausgelesen.                                                                             |
| [**IOCTL- \_ Speicher- \_ Auslagerungs \_ Steuerelement**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Aktiviert oder deaktiviert den Mechanismus, der Medien auswirft.                                                         |
| [**IOCTL- \_ Speicher \_ get- \_ Geräte \_ Nummer**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Ruft den Gerätetyp, die Gerätenummer und, für ein Partitionier bares Gerät, die Partitionsnummer eines Geräts ab. |
| [**IOCTL- \_ Speicher \_ get \_ Hotplug \_ Info**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Ruft die Hotplug-Konfiguration des angegebenen Geräts ab.                                                 |
| [**IOCTL- \_ Speicher \_ Medien- \_ \_ Serien \_ Nummer**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Ruft die Seriennummer eines USB-Geräts ab.                                                                 |
| [**IOCTL- \_ Speicher \_ get- \_ Medien \_ Typen**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Ruft die Geometry-Informationen des Geräts ab.                                                            |
| [**IOCTL- \_ Speicher \_ get \_ Media \_ types \_ Ex**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Ruft Informationen zu den Medientypen ab, die von einem Gerät unterstützt werden.                                        |
| [**IOCTL- \_ Speicher \_ Lade \_ Medien**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Lädt Medien in ein Gerät.                                                                                   |
| [**IOCTL \_ - \_ Speicher \_ Daten \_ Satz \_ Attribute verwalten**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**\_ \_ MCN-Steuerelement für ioctl-Speicher \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Aktiviert oder deaktiviert die Benachrichtigung über Medien Änderungen.                                                               |
| [**Entfernen von IOCTL- \_ Speicher \_ Medien \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Aktiviert oder deaktiviert den Auswerfen-Mechanismus des Mediums.                                                               |
| [**IOCTL- \_ Speicher \_ Lese \_ Kapazität**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Ruft die Geometry-Informationen für das Gerät ab.                                                           |
| [**IOCTL \_ - \_ speicherset \_ Hotplug \_ Info**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Legt die Hotplug-Konfiguration des angegebenen Geräts fest.                                                      |



 

 

 



