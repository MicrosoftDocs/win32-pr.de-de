---
description: Die SetGuidValue-Methode fügt einen neuen GUID-Wert (Typ VT CLSID) hinzu oder überschreibt \_ einen vorhandenen.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: IPortableDeviceValues::SetGuidValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de2554422ca9df16a1a1df98a5f4888e4914909885c6661818b0692b33b66763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963589"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a>IPortableDeviceValues::SetGuidValue-Methode

Die **SetGuidValue-Methode** fügt einen neuen **GUID-Wert** (Typ VT CLSID) hinzu oder überschreibt \_ einen vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Objekt,** das das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Eine **REFGUID,** die den neuen Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über denselben  Schlüssel verfügt, der vom Schlüsselparameter angegeben wird, überschreibt er den vorhandenen Wert ohne Warnung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Hinzufügen einer Ressource zu einem Objekt](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




