---
description: Benachrichtigt eine Anwendung, dass eine zuvor geplante Connect-oder Disconnect-Anforderung an das MTP/Bluetooth-Gerät abgeschlossen wurde.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Iconnectionrequestcallback:: OnComplete-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866523"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Iconnectionrequestcallback:: OnComplete-Methode

Mit der **OnComplete** -Methode wird eine Anwendung benachrichtigt, dass eine zuvor geplante Connect-oder Disconnect-Anforderung an das MTP/Bluetooth-Gerät abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hrStatus* \[ in\]
</dt> <dd>

Der Status der Anforderung zum Verbinden oder Trennen eines bestimmten Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Anwendung implementiert die [**iconnectionrequestcallback**](iconnectionrequestcallback.md) -Schnittstelle zum Empfangen von Benachrichtigungen zu abgeschlossenen Anforderungen und zum Abbrechen ausstehender Anforderungen.

Windows Portable Devices (WPD) ruft diese Methode auf, um eine Anwendung zu benachrichtigen, dass eine zuvor geplante Anforderung abgeschlossen wurde. Jede Anforderung kann durch den von der Anwendung bereitgestellten Rückruf nachverfolgt und abgebrochen werden. Wenn die Anwendung also mehrere Anforderungen gleichzeitig mit demselben [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Objekt senden muss, sollte jeder Anforderung ein eindeutiges [**iconnectionrequestcallback**](iconnectionrequestcallback.md) -Objekt als Eingabeparameter an die [**iportabledeviceconnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) -und [**iportabledeviceconnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) -Methoden übergeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portablede viceconnectapi. idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>Portabledeviceguids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconnectionrequestcallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




