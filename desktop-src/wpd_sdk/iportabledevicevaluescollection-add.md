---
description: 'IPortableDeviceValuesCollection::Add-Methode: Die Add-Methode fügt der Auflistung ein Element hinzu.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: IPortableDeviceValuesCollection::Add-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083240"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>IPortableDeviceValuesCollection::Add-Methode

Die **Add-Methode** fügt der Auflistung ein Element hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pValues* \[ In\]
</dt> <dd>

Zeiger auf eine **IPortableDeviceValues-Schnittstelle,** die der Auflistung hinzugefügt werden soll. Die Schnittstelle wird nicht tatsächlich kopiert, aber **AddRef** wird dafür aufgerufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um den Wert zur Auflistung hinzuzufügen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




