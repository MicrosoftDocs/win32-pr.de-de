---
description: Die GetSerializedSize-Methode berechnet die Puffergröße, die zum Speichern einer serialisierten IPortableDeviceValues-Schnittstelle erforderlich ist.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: IWpdSerializer::GetSerializedSize-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae6b8381928c64b7d16e9f5daa4dd9fd85acd9b61c13531365d871563ef6afe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704520"
---
# <a name="iwpdserializergetserializedsize-method"></a>IWpdSerializer::GetSerializedSize-Methode

Die **GetSerializedSize-Methode** berechnet die Puffergröße, die zum Speichern einer serialisierten [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md) erforderlich ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSource* \[ In\]
</dt> <dd>

Zeiger auf eine [**IPortableDeviceValues-Schnittstelle,**](iportabledevicevalues.md) deren Größe Sie anfordern möchten.

</dd> <dt>

*pdwSize* \[ out\]
</dt> <dd>

Zeiger auf ein **DWORD,** das die Puffergröße angibt, die zum Serialisieren *von pSource* in Bytes erforderlich ist.

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

 

 




