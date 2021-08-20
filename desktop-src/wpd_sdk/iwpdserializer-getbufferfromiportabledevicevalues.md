---
description: Die GetBufferFromIPortableDeviceValues-Methode serialisiert eine übermittelte IPortableDeviceValues-Schnittstelle in ein zugeordnetes Bytearray. Das zurückgegebene Bytearray wird dem Aufrufer zugeordnet und sollte vom Aufrufer mit coTaskMemFree freigegeben werden.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: IWpdSerializer::GetBufferFromIPortableDeviceValues-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 10a483331d15c09de8398d11e940453d8f239e2207fdefb82d86fd4bb1460daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843013"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>IWpdSerializer::GetBufferFromIPortableDeviceValues-Methode

Die **GetBufferFromIPortableDeviceValues-Methode** serialisiert eine **übermittelte IPortableDeviceValues-Schnittstelle** in ein zugeordnetes Bytearray. Das zurückgegebene Bytearray wird dem Aufrufer zugeordnet und sollte vom Aufrufer mit **coTaskMemFree** freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSource* \[ In\]
</dt> <dd>

Zeiger auf eine zu serialisierende [**IPortableDeviceValues-Schnittstelle.**](iportabledevicevalues.md)

</dd> <dt>

*ppBuffer* \[ out\]
</dt> <dd>

Zeiger auf ein **BYTE \* *_, das die serialisierten Daten enthält. Windows Portable Geräte weisen diesen Speicher zu. der Aufrufer muss es freigeben, indem er _* CoTaskMemFree aufruft.**

</dd> <dt>

*pdwBufferSize* \[ out\]
</dt> <dd>

Zeiger auf ein **DWORD,** das die Größe des zugeordneten Puffers in Bytes angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein erforderliches Zeigerargument war **NULL.**<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es war nicht genügend Arbeitsspeicher verfügbar, um den Puffer zu erstellen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWpdSerializer-Schnittstelle**](iwpdserializer.md)
</dt> </dl>

 

 




