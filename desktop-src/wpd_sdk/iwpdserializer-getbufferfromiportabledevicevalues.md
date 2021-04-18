---
description: Die getbufferfromiportabledevicevalues-Methode serialisiert eine übermittelte iportabledevicevalues-Schnittstelle zu einem zugeordneten Bytearray. Das zurückgegebene Bytearray wird dem Aufrufer zugeordnet und sollte vom Aufrufer mithilfe von "CoTaskMemFree" freigegeben werden.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Iwpdserializer:: getbufferfromiportabledevicevalues-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358221"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>Iwpdserializer:: getbufferfromiportabledevicevalues-Methode

Die **getbufferfromiportabledevicevalues** -Methode serialisiert eine übermittelte **iportabledevicevalues** -Schnittstelle zu einem zugeordneten Bytearray. Das zurückgegebene Bytearray wird dem Aufrufer zugeordnet und sollte vom Aufrufer mithilfe von " **CoTaskMemFree**" freigegeben werden.

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

*psource* \[ in\]
</dt> <dd>

Zeiger auf eine [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstelle, die serialisiert werden soll.

</dd> <dt>

*ppbuffer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **Byte \* *_, das die serialisierten Daten enthält. Tragbare Windows-Geräte ordnet diesen Arbeitsspeicher zu. der Aufrufer muss ihn durch Aufrufen von _* CoTaskMemFree freigeben**.

</dd> <dt>

*pdwBufferSize* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **DWORD** , das die Größe des zugeordneten Puffers in Bytes angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein erforderliches Zeigerargument war **null**.<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es war nicht genügend Arbeitsspeicher verfügbar, um den Puffer zu erstellen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwpdserializer-Schnittstelle**](iwpdserializer.md)
</dt> </dl>

 

 




