---
description: Die getserializedsize-Methode berechnet die Puffergröße, die zum Speichern einer serialisierten iportabledevicevalues-Schnittstelle erforderlich ist.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Iwpdserializer:: getserializedsize-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355273"
---
# <a name="iwpdserializergetserializedsize-method"></a>Iwpdserializer:: getserializedsize-Methode

Die **getserializedsize** -Methode berechnet die Puffergröße, die zum Speichern einer serialisierten [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstelle erforderlich ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psource* \[ in\]
</dt> <dd>

Zeiger auf eine [**iportabletovicevalues**](iportabledevicevalues.md) -Schnittstelle, deren Größe Sie anfordern möchten.

</dd> <dt>

*pdwSize* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **DWORD** , das die für die Serialisierung von *psource* erforderliche Puffergröße in Bytes angibt.

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

 

 




