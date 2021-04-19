---
description: Die copyvaluestopropertystore-Methode kopiert alle Werte aus einer Auflistung in eine IPropertyStore-Schnittstelle.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Iportabledevicevalues:: copyvaluestopropertystore-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373893"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>Iportabledevicevalues:: copyvaluestopropertystore-Methode

Die **copyvaluestopropertystore** -Methode kopiert alle Werte aus einer Auflistung in eine **IPropertyStore** -Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstore* \[ in\]
</dt> <dd>

Zeiger auf ein Speicher Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode konvertiert keine Werte von VT \_ LPWSTR in VT \_ BSTR. Viele externe Anwendungen oder Komponenten, die mit Ihrer Anwendung kommunizieren (z. b. einige Shellanwendungen), verwenden die **IPropertyStore** -Schnittstelle. Diese Methode bietet eine schnelle und einfache Möglichkeit zum Austauschen von Daten mit diesen Programmen.

Diese Methode wird in Windows Vista und höheren Versionen von Windows unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: copyvaluesfrompropertystore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




