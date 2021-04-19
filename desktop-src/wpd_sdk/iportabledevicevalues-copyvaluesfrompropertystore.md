---
description: Die copyvaluesfrompropertystore-Methode kopiert den Inhalt eines IPropertyStore in die Auflistung.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Iportabledevicevalues:: copyvaluesfrompropertystore-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355997"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>Iportabledevicevalues:: copyvaluesfrompropertystore-Methode

Die **copyvaluesfrompropertystore** -Methode kopiert den Inhalt eines **IPropertyStore** in die Auflistung.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstore* \[ in\]
</dt> <dd>

Zeiger auf einen **IPropertyStore** , der in die Auflistung kopiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode konvertiert automatisch alle **VT \_ BSTR** -Werte in **VT \_ LPWSTR** -Werte.

Viele externe Anwendungen oder Komponenten, die mit Ihrer Anwendung kommunizieren (z. b. einige Shellanwendungen), verwenden die **IPropertyStore** -Schnittstelle. Diese Methode bietet eine schnelle und einfache Möglichkeit zum Austauschen von Daten mit diesen Programmen.

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

[**Iportablede vicevalues:: copyvaluestopropertystore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




