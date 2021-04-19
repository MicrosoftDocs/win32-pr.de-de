---
description: Die Methode "Write teiportabledevicevaluestobuffer" serialisiert eine iportabledevicevalues-Schnittstelle zu einem vom Aufrufer zugeordneten Bytearray.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Iwpdserializer:: Write-portabledevicevaluestobuffer-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370494"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>Iwpdserializer:: Write-portabledevicevaluestobuffer-Methode

Die Methode " **Write teiportabledevicevaluestobuffer** " serialisiert eine **iportabledevicevalues** -Schnittstelle zu einem vom Aufrufer zugeordneten Bytearray.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwoutputbufferlength* \[ in\]
</dt> <dd>

**DWORD** , das die Größe von *pbuffer* in Bytes angibt.

</dd> <dt>

*präsults* \[ in\]
</dt> <dd>

Zeiger auf eine [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstelle, die serialisiert werden soll.

</dd> <dt>

*pbuffer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen vom Aufrufer zugewiesenen Puffer. Um die Größe des erforderlichen Puffers zu ermitteln, müssen Sie **getserializedsize** aufrufen.

</dd> <dt>

*pdwbyteswritten* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **DWORD** , das die Anzahl der Bytes angibt, die tatsächlich in den von dem Aufrufer zugewiesenen Puffer geschrieben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                          |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein erforderliches Zeigerargument war **null**.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Der vom Aufrufer bereitgestellte Puffer war nicht groß genug.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kopiert eine **iportabledevicevalues** -Schnittstelle in einen vorhandenen Puffer. Wenn Sie einen neuen Puffer zuordnen möchten, verwenden Sie [**getbufferfromiportableendvicevalues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwpdserializer-Schnittstelle**](iwpdserializer.md)
</dt> </dl>

 

 




