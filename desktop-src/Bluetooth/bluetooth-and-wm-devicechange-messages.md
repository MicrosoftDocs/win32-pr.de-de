---
title: Bluetooth und WM_DEVICECHANGE Nachrichten
description: Bluetooth enthält bestimmte WM DEVICECHANGE-Nachrichten, die es Entwicklern ermöglichen, Nachrichten zu erhalten, wenn Bluetooth \_ Geräte Statusänderungen durchlaufen.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b22c08c4243ce33f7d3146e96a3fcdd5c937b4781fd783918c148939ca0e22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588410"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Bluetooth und WM \_ DEVICECHANGE-Nachrichten

Bluetooth enthält bestimmte [**WM \_ DEVICECHANGE-Nachrichten,**](/windows/desktop/DevIO/wm-devicechange) die es Entwicklern ermöglichen, Nachrichten zu erhalten, wenn Bluetooth Geräte Statusänderungen durchlaufen. In diesem Thema wird beschrieben, wie sie Bluetooth **WM \_ DEVICECHANGE-Nachrichten** empfangen und Bluetooth Nachrichten auflistet.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Empfangen Bluetooth WM \_ DEVICECHANGE-Nachrichten

Zum Empfangen [**von WM \_ DEVICECHANGE-Nachrichten**](/windows/desktop/DevIO/wm-devicechange) muss zunächst ein Handle für das lokale Radio geöffnet werden. Hierzu können Sie eine der folgenden Methoden verwenden:

-   Verwenden Sie die [Funktion SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) mit den folgenden Parametern: (GUID \_ BTHPORT DEVICE INTERFACE, ..., DIGCF PRESENT DIGCF DEVICEINTERFACE), und verwenden Sie dann die \_ Funktionen \_ \_ \| \_ [SetupDiEnumDeviceInterfaces,](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces) [SetupDiGetDeviceInterfaceDetail,](https://msdn.microsoft.com/library/ms792901.aspx) [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)und [SetupDiDestroyDeviceInfoList.](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
-   Verwenden Sie [**die Funktionen BluetoothFindFirstErklär,**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio) [**BluetoothFindNext Audio und**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio) [**BluetoothFindErklärClose.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)

Wenn das Bluetooth geöffnet wird, rufen Sie die [**RegisterDeviceNotification-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) auf, und registrieren Sie sich für Benachrichtigungen auf dem Handle, indem **Sie DBT \_ DEVTYP \_ HANDLE** als Gerätetyp verwenden. Bei der Registrierung werden die folgenden GUIDs gesendet, und das [**DEV \_ BROADCAST \_ HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch-Datenmitglied \_** ist der zugeordnete Puffer.

## <a name="bluetooth-specific-messages"></a>Bluetooth-spezifische Nachrichten

In der folgenden Tabelle sind Bluetooth [**WM \_ DEVICECHANGE-Meldungen**](/windows/desktop/DevIO/wm-devicechange) aufgeführt.

| GUID                                   | BUFFER                                                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_GUID-BLUETOOTH \_ HCI-EREIGNIS \_            | [**BTH \_ \_ HCI-EREIGNISINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Diese Meldung wird gesendet, wenn ein remote Bluetooth Gerät auf ACL-Ebene eine Verbindung herstellt oder trennt.                                                                                                                                                                                                                                                                    |
| \_ \_ GUID-BLUETOOTH-L2CAP-EREIGNIS \_          | [**BTH \_ \_ L2CAP-EREIGNISINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Diese Meldung wird gesendet, wenn ein L2CAP-Kanal zwischen dem lokalen Funkgerät und einem Remotegerät Bluetooth oder beendet wurde. Bei L2CAP-Kanälen, bei denen es sich um Multiplexer handelt, z. B. RFCOMM, wird diese Meldung nur gesendet, wenn der zugrunde liegende Kanal eingerichtet wird, nicht, wenn jeder Multiplexkanal, z. B. ein RFCOMM-Kanal, eingerichtet oder beendet wird. |
| \_ \_ GUID-BLUETOOTH-PIN-ANFORDERUNG \_          | Nicht zutreffend                                         | Diese Meldung sollte von der Anwendung ignoriert werden. Wenn die Anwendung PIN-Anforderungen empfangen muss, sollte die [**BluetoothRegisterForAuthentication-Funktion**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) verwendet werden.                                                                                                                                                   |
| GUID \_ BLUETOOTH \_ RADIO \_ IN \_ RANGE      | [**BTH \_ RADIO \_ IN \_ RANGE**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Diese Meldung wird gesendet, wenn eines der folgenden Attribute eines Remote-Bluetooth-Geräts geändert wurde: das Gerät wurde gefunden, die Klasse des Geräts, der Name, der verbundene Zustand oder der gespeicherte Zustand des Geräts. Diese Meldung wird auch gesendet, wenn diese Attribute festgelegt oder bzw. entiert werden.                                                                                  |
| GUID \_ BLUETOOTH \_ RADIO \_ OUT \_ OF \_ RANGE | [**\_BLUETOOTH-ADRESSE**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Diese Meldung wird gesendet, wenn nach Abschluss der letzten Anfrage kein zuvor gefundenes Gerät gefunden wurde. Diese Nachricht wird nicht an gespeicherte Geräte gesendet. Die **BTH \_ ADDRESS-Struktur** ist die Adresse des Geräts, das nicht gefunden wurde.                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**BluetoothFindFirst Audio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**BluetoothFindNext Audio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**BluetoothFind LowClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**\_BLUETOOTH-ADRESSE**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**BTH \_ \_ HCI-EREIGNISINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**BTH \_ \_ L2CAP-EREIGNISINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**BTH \_ RADIO \_ IN \_ RANGE**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**DEV \_ BROADCAST \_ HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 