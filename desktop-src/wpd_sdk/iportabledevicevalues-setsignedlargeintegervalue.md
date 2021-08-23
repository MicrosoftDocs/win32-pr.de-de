---
description: Die SetSignedLargeIntegerValue-Methode fügt einen neuen LONGLONG-Wert (Typ VT \_ I8) hinzu oder überschreibt einen vorhandenen Wert.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: IPortableDeviceValues::SetSignedLargeIntegerValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5ac0ec7e7dce817565ea8b260501879ca8423b090ff357b30f177ff828c8ff9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026768"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a>IPortableDeviceValues::SetSignedLargeIntegerValue-Methode

Die **SetSignedLargeIntegerValue-Methode** fügt einen neuen **LONGLONG-Wert** (Typ VT \_ I8) hinzu oder überschreibt einen vorhandenen Wert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY,** der das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Ein **LONGLONG-Wert,** der den neuen Wert angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der vom *Schlüsselparameter* angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




