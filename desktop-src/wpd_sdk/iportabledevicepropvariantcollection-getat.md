---
description: Die GetAt-Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'Iportabledevicepropvariantcollection:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365977"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>Iportabledevicepropvariantcollection:: GetAt-Methode

Die **GetAt** -Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

**DWORD** , das den NULL basierten Index des abzurufenden Elements enthält.

</dd> <dt>

*pValue* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine **PROPVARIANT** -Struktur. Der Aufrufer ist dafür verantwortlich, diesen Speicher durch Aufrufen von **propvariantclear frei** zugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                          |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | Ein erforderliches Zeigerargument war **null**.<br/>      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der von ihm über gegebene Index lag außerhalb des zulässigen Bereichs.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienst Formate](retrieving-supported-formats.md)
</dt> <dt>

[Abrufen unterstützter Dienst Methoden](retrieving-supported-methods.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Inhaltstypen](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Abrufen der funktionalen Objekt Bezeichner für ein Gerät](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Festlegen von Eigenschaften für mehrere Objekte](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




