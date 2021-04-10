---
title: Bluetooth-Strukturen
description: Dieser Abschnitt enthält Definitionen für Strukturen, die zum Verwalten von Bluetooth-Geräten und-Diensten verwendet werden.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, Referenz, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df10989e41814f6f750bdcc719f01b14ccae315
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855523"
---
# <a name="bluetooth-structures"></a>Bluetooth-Strukturen

Dieser Abschnitt enthält Definitionen für Strukturen, die zum Verwalten von Bluetooth-Geräten und-Diensten verwendet werden.

Bluetooth wird auch durch die Verwendung der Windows Sockets-Programmierschnittstelle unterstützt. Weitere Informationen zum Programmieren von Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie [unter Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).



| `Section`                                                                                       | Inhalt                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Bluetooth- \_ Adresse**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Enthält die Adresse eines Bluetooth-Geräts.                                                                                      |
| [**Bluetooth \_ Authentifizieren von \_ Rückruf- \_ Parametern**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Enthält spezifische Konfigurationsinformationen über das Bluetooth-Gerät, das auf eine Authentifizierungsanforderung antwortet.                  |
| [**Bluetooth- \_ Authenticate- \_ Antwort**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Enthält Informationen, die als Reaktion auf ein BTH- \_ Remote \_ Authentifizierungs Anforderungs Ereignis weitergeleitet werden \_ .                                           |
| [**Bluetooth- \_ COD- \_ Paare**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Ermöglicht die Angabe und den Abruf von Informationen zur Bluetooth-Klasse von Geräten (COD).                                         |
| [**Bluetooth- \_ Geräte \_ Informationen**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Stellt Informationen zu einem Bluetooth-Gerät bereit.                                                                                   |
| [**Bluetooth- \_ Geräte \_ Suche- \_ Parameter**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Gibt Suchkriterien für Bluetooth-Geräte suchen an.                                                                         |
| [**Bluetooth \_ Find \_ Radio- \_ Parametern**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Ermöglicht die Enumeration installierter Bluetooth-Radios.                                                                       |
| [**Informationen zum lokalen Bluetooth- \_ \_ Dienst \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Enthält Informationen zum lokalen Dienst für ein Bluetooth-Radio.                                                                        |
| [**numerische Bluetooth- \_ \_ Vergleichs \_ Informationen**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Enthält den numerischen Wert, der für die Authentifizierung über einen numerischen Vergleich verwendet wird.                                                       |
| [**Bluetooth \_ OOB- \_ Daten \_ Informationen**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Enthält Daten, die für die Authentifizierung vor dem Einrichten einer Out-of-Band-Geräte Kopplung verwendet werden.                                          |
| [**Informationen zum Bluetooth- \_ Kennwort \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Enthält den für die Authentifizierung per Hauptschlüssel verwendeten Schlüssel.                                                                        |
| [**Informationen zur Bluetooth- \_ Pin \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Enthält Informationen, die für die Authentifizierung per PIN verwendet werden.                                                                            |
| [**Bluetooth- \_ Radio \_ Info**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Enthält Informationen zu einem Bluetooth-Radio.                                                                                    |
| [**Bluetooth \_ - \_ Geräteauswahl auswählen \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Erleichtert und verwaltet die Sichtbarkeit, Authentifizierung und Auswahl von Bluetooth-Geräten und-Diensten.                         |
| [**Informationen zum BTH- \_ Gerät \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Speichert Informationen zu einem Bluetooth-Gerät.                                                                                     |
| [**BTH \_ HCI- \_ Ereignis \_ Informationen**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Wird in Verbindung mit dem Abrufen \_ von WM devicechange-Nachrichten für Bluetooth verwendet.                                                       |
| [**BTH \_ L2CAP \_ Ereignis \_ Informationen**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Enthält Daten zu den Ereignissen, die einem L2CAP-Kanal zugeordnet sind.                                                        |
| [**BTH- \_ Abfrage \_ Gerät**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Wird bei der Abfrage des Vorhandenseins eines Bluetooth-Geräts verwendet.                                                                       |
| [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Wird verwendet, um einen Bluetooth-Dienst abzufragen.                                                                                               |
| [**BTH \_ Radio \_ in \_ Bereich**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Speichert Daten zu den Bluetooth-Geräten im Kommunikationsbereich.                                                     |
| [**BTH- \_ Set- \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Stellt Dienst Informationen für den angegebenen Bluetooth-Dienst bereit.                                                                |
| [**SDP- \_ Element \_ Daten**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Speichert SDP-Elementdaten.                                                                                                         |
| [**SDP- \_ Zeichen \_ Folgentyp \_ Daten**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Speichert Informationen zu SDP-Zeichen folgen Typen.                                                                                       |
| [**Sdpattributerange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Wird in einer Bluetooth-Abfrage verwendet, um den Satz von Attributen einzuschränken, der in der Abfrage zurückgegeben werden soll.                                             |
| [**Sdpqueryuuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Ermöglicht die Suche nach UUIDs.                                                                                                 |
| [**Sdpqueryuuidunion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Enthält die UUID, auf der eine SDP-Abfrage durchgeführt werden soll. Wird in Verbindung mit der [**sdpqueryuuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) -Struktur verwendet. |
| [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Wird in Verbindung mit Bluetooth-Socketvorgängen verwendet, wie von der AF- \_ BTH-Adressfamilie definiert.                                   |



 

 

 




