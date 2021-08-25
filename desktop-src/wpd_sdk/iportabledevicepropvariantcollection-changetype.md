---
description: Die ChangeType-Methode konvertiert alle Elemente in der Auflistung in den angegebenen VARTYPE.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: IPortableDevicePropVariantCollection::ChangeType-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839330"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>IPortableDevicePropVariantCollection::ChangeType-Methode

Die **ChangeType-Methode** konvertiert alle Elemente in der Auflistung in den angegebenen VARTYPE.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vt* \[ In\]
</dt> <dd>

Gibt den **VARTYPE an,** in den Sie alle Elemente in der Auflistung konvertieren möchten. Zu den Beispieltypen zählen VT \_ UI4 und VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn bei dieser Methode ein Fehler auftritt, bleibt die Auflistung möglicherweise in einem Zwischenzustand, bei dem einige Member konvertiert und einige nicht konvertiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




