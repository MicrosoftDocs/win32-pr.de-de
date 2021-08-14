---
description: Die CopyValuesToPropertyStore-Methode kopiert alle Werte aus einer Auflistung in eine IPropertyStore-Schnittstelle.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: IPortableDeviceValues::CopyValuesToPropertyStore-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2d134cb61831426451b1c6068bde5ca787b027fbe5b153587b45d9693ef739c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697247"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>IPortableDeviceValues::CopyValuesToPropertyStore-Methode

Die **CopyValuesToPropertyStore-Methode** kopiert alle Werte aus einer Auflistung in eine **IPropertyStore-Schnittstelle.**

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStore* \[ In\]
</dt> <dd>

Zeiger auf ein Speicherobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode konvertiert keine Werte von VT \_ LPWSTR in VT \_ BSTR. Viele externe Anwendungen oder Komponenten, die mit Ihrer Anwendung kommunizieren, z. B. einige Shellanwendungen, verwenden die **IPropertyStore-Schnittstelle.** Diese Methode bietet eine schnelle und einfache Möglichkeit zum Austauschen von Daten mit diesen Programmen.

Diese Methode wird in Windows Vista und neueren Versionen von Windows unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




