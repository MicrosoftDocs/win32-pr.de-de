---
description: 'IPortableDevicePropVariantCollection::GetAt-Methode: Die GetAt-Methode ruft ein Element von einem nullbasierten Index aus der Auflistung ab.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: IPortableDevicePropVariantCollection::GetAt-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106798"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>IPortableDevicePropVariantCollection::GetAt-Methode

Die **GetAt-Methode** ruft ein Element von einem nullbasierten Index aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ In\]
</dt> <dd>

**DWORD,** das den nullbasierten Index des abzurufenden Elements enthält.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Zeiger auf eine **PROPVARIANT-Struktur.** Der Aufrufer ist dafür verantwortlich, diesen Arbeitsspeicher durch Aufrufen von **PropVariantClear frei zu geben.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                          |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>    | Ein erforderliches Zeigerargument war **NULL.**<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der übergebene Index lag nicht im Bereich.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter Abrufen der von einem Gerät [unterstützten funktionalen Kategorien.](retrieving-the-functional-categories-supported-by-a-device.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Abrufen eines Objektbezeichners aus einem persistenten eindeutigen Bezeichner](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Abrufen unterstützter Dienstereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienstformate](retrieving-supported-formats.md)
</dt> <dt>

[Abrufen unterstützter Dienstmethoden](retrieving-supported-methods.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Inhaltstypen](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Funktionskategorien](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Abrufen der funktionalen Objektbezeichner für ein Gerät](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Festlegen von Eigenschaften für mehrere Objekte](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




