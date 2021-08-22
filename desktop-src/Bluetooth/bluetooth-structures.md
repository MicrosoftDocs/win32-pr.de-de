---
title: Bluetooth Strukturen
description: Dieser Abschnitt enthält Definitionen für Strukturen, die zum Verwalten Bluetooth Geräten und Diensten verwendet werden.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, Referenz, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a2208902360b4f1161f9586e41f59f062972efbbba7eeb0cfb8ffbbc3c6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588280"
---
# <a name="bluetooth-structures"></a>Bluetooth Strukturen

Dieser Abschnitt enthält Definitionen für Strukturen, die zum Verwalten Bluetooth Geräten und Diensten verwendet werden.

Bluetooth wird auch mithilfe der Windows Sockets-Programmierschnittstelle unterstützt. Weitere Informationen zum Programmieren Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie unter [Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).



| `Section`                                                                                       | Content                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_BLUETOOTH-ADRESSE**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Enthält die Adresse eines Bluetooth Geräts.                                                                                      |
| [**BLUETOOTH \_ AUTHENTICATE \_ CALLBACK \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Enthält spezifische Konfigurationsinformationen zum Bluetooth Gerät, das auf eine Authentifizierungsanforderung antwortet.                  |
| [**\_ \_ BLUETOOTH-AUTHENTIFIZIERUNGSANTWORT**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Enthält Informationen, die als Antwort auf ein BTH \_ REMOTE \_ AUTHENTICATE \_ REQUEST-Ereignis übergeben werden.                                           |
| [**BLUETOOTH \_ COD \_ PAIRS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Stellt für die Spezifikation und den Abruf von Codinformationen (Class Of Device) Bluetooth bereit.                                         |
| [**\_ \_ BLUETOOTH-GERÄTEINFORMATIONEN**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Stellt Informationen zu einem Bluetooth Gerät bereit.                                                                                   |
| [**BLUETOOTH \_ DEVICE \_ SEARCH \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Gibt Suchkriterien für Bluetooth Gerätesuchen an.                                                                         |
| [**BLUETOOTH \_ FIND \_ RADIO \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Erleichtert die Enumeration installierter Bluetooth Radios.                                                                       |
| [**\_INFORMATIONEN ZUM LOKALEN \_ BLUETOOTH-DIENST \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Enthält lokale Dienstinformationen für ein Bluetooth Radio.                                                                        |
| [**\_NUMERISCHE \_ BLUETOOTH-VERGLEICHSINFORMATIONEN \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Enthält den numerischen Wert, der für die Authentifizierung über einen numerischen Vergleich verwendet wird.                                                       |
| [**\_ \_ OOB-DATENINFORMATIONEN \_ FÜR BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Enthält Daten, die vor dem Einrichten einer Out-of-Band-Gerätekopplung zur Authentifizierung verwendet werden.                                          |
| [**BLUETOOTH \_ PASSKEY \_ INFO**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Enthält den Hauptschlüssel, der für die Authentifizierung über den Hauptschlüssel verwendet wird.                                                                        |
| [**\_ \_ BLUETOOTH-PIN-INFORMATIONEN**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Enthält Informationen, die für die Authentifizierung über PIN verwendet werden.                                                                            |
| [**BLUETOOTH \_ RADIO \_ INFO**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Enthält Informationen zu einem Bluetooth Radio.                                                                                    |
| [**BLUETOOTH \_ SELECT \_ DEVICE \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Erleichtert und verwaltet die Sichtbarkeit, Authentifizierung und Auswahl von Bluetooth Geräten und Diensten.                         |
| [**\_BTH-GERÄTEINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Speichert Informationen zu einem Bluetooth Gerät.                                                                                     |
| [**BTH \_ \_ HCI-EREIGNISINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Wird in Verbindung mit dem Abrufen von WM \_ DEVICECHANGE-Nachrichten für Bluetooth verwendet.                                                       |
| [**BTH \_ \_ L2CAP-EREIGNISINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Enthält Daten zu den Ereignissen, die einem L2CAP-Kanal zugeordnet sind.                                                        |
| [**\_BTH-ABFRAGEGERÄT \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Wird beim Abfragen des Vorhandenseins eines Bluetooth Geräts verwendet.                                                                       |
| [**\_BTH-ABFRAGEDIENST \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Wird zum Abfragen eines Bluetooth Diensts verwendet.                                                                                               |
| [**BTH \_ RADIO \_ IN \_ RANGE**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Speichert Daten zu den Bluetooth Geräten, die sich innerhalb des Kommunikationsbereichs befinden.                                                     |
| [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Stellt Dienstinformationen für den angegebenen Bluetooth-Dienst bereit.                                                                |
| [**\_SDP-ELEMENTDATEN \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Speichert SDP-Elementdaten.                                                                                                         |
| [**\_ \_ SDP-ZEICHENFOLGENTYPDATEN \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Speichert Informationen zu SDP-Zeichenfolgentypen.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Wird in einer Bluetooth Abfrage verwendet, um den Satz von Attributen einzuschränken, die in der Abfrage zurückgegeben werden sollen.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Erleichtert die Suche nach UUIDs.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Enthält die UUID, für die eine SDP-Abfrage ausgeführt werden soll. Wird in Verbindung mit der [**SdpQueryUuid-Struktur**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) verwendet. |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Wird in Verbindung mit Bluetooth Socketvorgängen verwendet, wie von der AF \_ BTH-Adressfamilie definiert.                                   |



 

 

 




