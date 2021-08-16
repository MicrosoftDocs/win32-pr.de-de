---
description: Benachrichtigt eine Anwendung, dass eine zuvor geplante Anforderung Verbinden verbindung mit dem MTP-/Bluetooth abgeschlossen wurde.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: IConnectionRequestCallback::OnComplete-Methode (Devpkey.h)
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
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843188"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback::OnComplete-Methode

Die **OnComplete-Methode** benachrichtigt eine Anwendung, dass eine zuvor geplante Verbinden- oder Disconnect-Anforderung an das MTP/Bluetooth abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hrStatus* \[ In\]
</dt> <dd>

Der Status der Anforderung zum Verbinden oder Trennen eines bestimmten Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Anwendung implementiert die [**IConnectionRequestCallback-Schnittstelle,**](iconnectionrequestcallback.md) um Benachrichtigungen über abgeschlossene Anforderungen zu empfangen und ausstehende Anforderungen abzubricht.

Windows Portable Devices (WPD) ruft diese Methode auf, um eine Anwendung zu benachrichtigen, dass eine zuvor geplante Anforderung abgeschlossen wurde. Jede Anforderung kann durch den von der Anwendung bereitgestellten Rückruf nachverfolgt und abgebrochen werden. Wenn die Anwendung also mehrere Anforderungen gleichzeitig mit dem gleichen [**IPortableDeviceConnector-Objekt**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) senden muss, sollte jeder Anforderung ein eindeutiges [**IConnectionRequestCallback-Objekt**](iconnectionrequestcallback.md) als Eingabeparameter an die [**Methoden IPortableDeviceConnector::Verbinden**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) und [**IPortableDeviceConnector::D isconnector**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) übergeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




