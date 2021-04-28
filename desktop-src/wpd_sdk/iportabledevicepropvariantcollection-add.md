---
description: 'IPortableDevicePropVariantCollection::Add-Methode: Die Add-Methode fügt der Auflistung ein Element hinzu.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: IPortableDevicePropVariantCollection::Add-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112458"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>IPortableDevicePropVariantCollection::Add-Methode

Die **Add-Methode** fügt der Auflistung ein Element hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pValue* \[ In\]
</dt> <dd>

Zeiger auf ein neues **PROPVARIANT-Objekt,** das der Auflistung hinzugefügt werden soll. Diese Methode kopiert **die PROPVARIANT** in die Auflistung, daher sollten Sie Ihre lokale Kopie der Variablen durch Aufrufen **von PropVariantClear** nach dem Aufruf dieser Methode veröffentlichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn der VARTYPE für *pValue* VT VECTOR oder VT UI1 ist, wird das Festlegen und Abrufen eines Puffers mit \_ \_ **NULL-** oder Nullgröße nicht unterstützt. Beispielsweise sind weder pValue.caub.pElems = **NULL** noch pValue.caub.cElems = 0 zulässig.

Wenn ein Aufrufer versucht, ein Element eines anderen VARTYPE-Elements hinzuzufügen, das in der Auflistung enthalten ist, und der PROPVARIANT-Wert von dieser Schnittstelle nicht automatisch geändert werden kann, wird diese Methode fehlschlagen. Um den Auflistungstyp manuell zu ändern, rufen [**Sie IPortableDevicePropVariantCollection::ChangeType auf.**](iportabledevicepropvariantcollection-changetype.md)

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter Abrufen eines Objektbezeichners [aus einem persistenten eindeutigen Bezeichner.](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Verschieben von Inhalten auf dem Gerät](moving-content-on-the-device.md)
</dt> <dt>

[Abrufen eines Objektbezeichners aus einem persistenten eindeutigen Bezeichner](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




