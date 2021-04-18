---
description: Die ChangeType-Methode konvertiert alle Elemente in der Auflistung in den angegebenen VarType.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Iportabledevicepropvariantcollection:: ChangeType-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371409"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>Iportabledevicepropvariantcollection:: ChangeType-Methode

Die **ChangeType** -Methode konvertiert alle Elemente in der Auflistung in den angegebenen VarType.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VT* \[ in\]
</dt> <dd>

Gibt den **VarType** an, in den alle Elemente in der Auflistung konvertiert werden sollen. Beispiel Typen sind VT \_ UI4 und VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode fehlschlägt, kann die Auflistung in einem Zwischenzustand belassen werden, wobei einige Elemente konvertiert und einige nicht konvertiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




