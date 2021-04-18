---
description: Die Add-Methode fügt der Auflistung ein Element hinzu.
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Iportabledevicevaluescollection:: Add-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365393"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>Iportabledevicevaluescollection:: Add-Methode

Die **Add** -Methode fügt der Auflistung ein Element hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvalues* \[ in\]
</dt> <dd>

Zeiger auf eine **iportabledecovicevalues** -Schnittstelle, die der Auflistung hinzugefügt werden soll. Die Schnittstelle wird nicht tatsächlich kopiert, aber die **adressf** wird darauf aufgerufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um den Wert der Auflistung hinzuzufügen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportableabvicevaluescollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




