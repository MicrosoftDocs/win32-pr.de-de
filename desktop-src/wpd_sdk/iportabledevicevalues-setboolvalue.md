---
description: Die SetBoolValue-Methode fügt einen neuen booleschen Wert (Typ VT BOOL) hinzu oder überschreibt \_ einen vorhandenen.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: IPortableDeviceValues::SetBoolValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: a4829d1c7f54042864dc4f54f26a17fcf4b0f84daab9352961d775d97adb45cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026778"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a>IPortableDeviceValues::SetBoolValue-Methode

Die **SetBoolValue-Methode** fügt einen neuen **booleschen** Wert (Typ VT BOOL) hinzu oder überschreibt \_ einen vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
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

Eine **BOOL,** die den neuen Wert angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über  den gleichen Schlüssel verfügt, der vom Schlüsselparameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




