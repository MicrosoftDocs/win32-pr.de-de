---
description: Die Add-Methode fügt der Auflistung ein Element hinzu.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Iportabledevicepropvariantcollection:: Add-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373846"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Iportabledevicepropvariantcollection:: Add-Methode

Die **Add** -Methode fügt der Auflistung ein Element hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pValue* \[ in\]
</dt> <dd>

Zeiger auf ein neues **PROPVARIANT** -Objekt, das der Auflistung hinzugefügt werden soll. Diese Methode kopiert die **PROPVARIANT** in die Auflistung. Daher sollten Sie Ihre lokale Kopie der Variablen freigeben, indem Sie **propvariantclear** aufrufen, nachdem Sie diese Methode aufgerufen haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn VarType für *pValue den Wert* VT \_ Vector oder VT \_ UI1 aufweist, wird das Festlegen und Abrufen eines Puffers, **der NULL** oder NULL ist, nicht unterstützt. Beispielsweise sind weder pValue. Caub. pelems = **null** noch pValue. Caub. celems = 0 zulässig.

Wenn ein Aufrufer versucht, ein Element eines anderen in der Auflistung enthaltenen VarType hinzuzufügen, und der PROPVARIANT-Wert nicht automatisch von dieser Schnittstelle geändert werden kann, schlägt diese Methode fehl. Um den Sammlungstyp manuell zu ändern, nennen Sie [**iportabledevicepropvariantcollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Verschieben von Inhalt auf dem Gerät](moving-content-on-the-device.md)
</dt> <dt>

[Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




