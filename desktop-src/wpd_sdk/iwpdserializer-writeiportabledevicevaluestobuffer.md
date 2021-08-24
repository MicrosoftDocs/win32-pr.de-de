---
description: Die WriteIPortableDeviceValuesToBuffer-Methode serialisiert eine IPortableDeviceValues-Schnittstelle in ein vom Aufrufer zugeordnetes Bytearray.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: IWpdSerializer::WriteIPortableDeviceValuesToBuffer-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: db86953e2e08c0a66f6e497c1fcd2350cc726be8852803cf8f4d64bfff523500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657740"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>IWpdSerializer::WriteIPortableDeviceValuesToBuffer-Methode

Die **WriteIPortableDeviceValuesToBuffer-Methode** serialisiert eine **IPortableDeviceValues-Schnittstelle** in ein vom Aufrufer zugeordnetes Bytearray.

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

*dwOutputBufferLength* \[ In\]
</dt> <dd>

**DWORD,** das die Größe von *pBuffer* in Bytes angibt.

</dd> <dt>

*pResults* \[ In\]
</dt> <dd>

Zeiger auf eine zu serialisierende [**IPortableDeviceValues-Schnittstelle.**](iportabledevicevalues.md)

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Puffer. Rufen **Sie GetSerializedSize** auf, um die Größe des erforderlichen Puffers zu erfahren.

</dd> <dt>

*pdwBytesWritten* \[ out\]
</dt> <dd>

Zeiger auf ein **DWORD,** das die Anzahl der Bytes angibt, die tatsächlich in den vom Aufrufer zugeordneten Puffer geschrieben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                          |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein erforderliches Zeigerargument war **NULL.**<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Der vom Aufrufer bereitgestellte Puffer war nicht groß genug.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kopiert eine **IPortableDeviceValues-Schnittstelle** in einen vorhandenen Puffer. Wenn Sie einen neuen Puffer zuordnen möchten, verwenden [**Sie GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWpdSerializer-Schnittstelle**](iwpdserializer.md)
</dt> </dl>

 

 




