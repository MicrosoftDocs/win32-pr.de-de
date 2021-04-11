---
title: Bluetooth-und WM_DEVICECHANGE-Nachrichten
description: Bluetooth umfasst bestimmte WM \_ devicechange-Nachrichten, mit denen Entwickler Nachrichten abrufen können, wenn Bluetooth-Gerätestatus Änderungen durchlaufen.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948828"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Bluetooth-und WM- \_ devicechange-Meldungen

Bluetooth umfasst bestimmte [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Nachrichten, mit denen Entwickler Nachrichten abrufen können, wenn Bluetooth-Gerätestatus Änderungen durchlaufen. In diesem Thema wird beschrieben, wie Sie Bluetooth-spezifische **WM- \_ devicechange** -Nachrichten empfangen und Bluetooth-spezifische Meldungen auflisten.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Empfangen von Bluetooth-spezifischen WM- \_ devicechange-Nachrichten

Zum Empfangen von " [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) "-Nachrichten muss zunächst ein Handle für das lokale Radio geöffnet werden. Hierzu können Sie eine der folgenden Methoden verwenden:

-   Verwenden Sie die [setupdigetclassdevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) -Funktion mit den folgenden Parametern: (GUID \_ bthport- \_ Geräte \_ Schnittstelle,..., digcf stellt " \_ \| digcf \_ deviceinterface" dar) und dann die Funktionen " [setupdienumdeviceintergesichter](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)", " [setupdigetdeviceinterfacedetail](https://msdn.microsoft.com/library/ms792901.aspx)", "|" und " [setupdidestroydeviceinfolist](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) " zu verwenden. [](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
-   Verwenden Sie die Funktionen [**bluetoothfindfirstradio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**bluetoothfindnextradio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)und [**bluetoothfindradioclose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .

Wenn das Bluetooth-Funk Handle geöffnet ist, können Sie die [**registerdevicenotifi-**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) Funktion aufrufen und sich für Benachrichtigungen über das Handle mithilfe des **DBT \_ devype- \_ Handles** als DeviceType registrieren. Wenn Sie registriert sind, werden die folgenden GUIDs gesendet, und das [**dev \_ Broadcast \_ handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch- \_ Datenmember** ist der zugeordnete Puffer.

## <a name="bluetooth-specific-messages"></a>Bluetooth-spezifische Meldungen

In der folgenden Tabelle sind Bluetooth-spezifische [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Meldungen aufgeführt.

| GUID                                   | BUFFER                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ Bluetooth \_ HCI- \_ Ereignis            | [**BTH \_ HCI- \_ Ereignis \_ Informationen**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Diese Meldung wird gesendet, wenn ein Bluetooth-Remote Gerät eine Verbindung mit der ACL-Ebene herstellt oder trennt.                                                                                                                                                                                                                                                                    |
| GUID \_ Bluetooth \_ L2CAP \_ Ereignis          | [**BTH \_ L2CAP \_ Ereignis \_ Informationen**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Diese Meldung wird gesendet, wenn ein L2CAP-Kanal zwischen dem lokalen Radio und einem Bluetooth-Remote Gerät eingerichtet oder beendet wurde. Bei L2CAP-Kanälen, bei denen es sich um Multiplexer handelt, wie z. b. RFCOMM, wird diese Nachricht nur gesendet, wenn der zugrunde liegende Kanal eingerichtet wird, nicht, wenn jeder Multiplex-Kanal (z. b. ein RFCOMM-Kanal) eingerichtet oder beendet |
| GUID \_ Bluetooth- \_ Pin- \_ Anforderung          | Nicht zutreffend                                         | Diese Meldung sollte von der Anwendung ignoriert werden. Wenn die Anwendung Pin-Anforderungen empfangen muss, sollte die [**bluetoothregisterforauthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) -Funktion verwendet werden.                                                                                                                                                   |
| GUID- \_ Bluetooth- \_ Radio \_ im \_ Bereich      | [**BTH \_ Radio \_ in \_ Bereich**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Diese Meldung wird gesendet, wenn eines der folgenden Attribute eines Bluetooth-Remote Geräts geändert wurde: das Gerät wurde ermittelt, die Klasse des Geräts, der Name, der verbundene Zustand oder der Zustand des Geräts wurde gespeichert. Diese Meldung wird auch gesendet, wenn diese Attribute festgelegt oder gelöscht werden.                                                                                  |
| GUID \_ Bluetooth- \_ Radio \_ außerhalb des gültigen \_ \_ Bereichs | [**Bluetooth- \_ Adresse**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Diese Meldung wird gesendet, wenn ein zuvor ermitteltes Gerät nach dem Abschluss der letzten Abfrage nicht gefunden wurde. Diese Meldung wird nicht für gespeicherte Geräte gesendet. Die **BTH- \_ Adress** Struktur ist die Adresse des Geräts, das nicht gefunden wurde.                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bluetoothfindfirstradio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**Bluetoothfindnextradio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**Bluetoothfindradioclose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**Registerdevicenotifizierung**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[Setupdidestroyeinfolist](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[Setupdienumbinviceintergesichter](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[Setupdigetclassbinvs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**Bluetooth- \_ Adresse**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**BTH \_ HCI- \_ Ereignis \_ Informationen**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**BTH \_ L2CAP \_ Ereignis \_ Informationen**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**BTH \_ Radio \_ in \_ Bereich**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**DEV- \_ Broadcast \_ handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM- \_ devicechange**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 