---
description: Die SetUnsignedIntegerValue-Methode fügt einen neuen ULONG-Wert (VT \_ UI4-Typ) hinzu oder überschreibt einen vorhandenen.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: IPortableDeviceValues::SetUnsignedIntegerValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9c58569554cf9170788524bdcb233bf42b3318f1e954050bb713711c93337543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928460"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a>IPortableDeviceValues::SetUnsignedIntegerValue-Methode

Die **SetUnsignedIntegerValue-Methode** fügt einen neuen **ULONG-Wert** (VT \_ UI4-Typ) hinzu oder überschreibt einen vorhandenen Wert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
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

Eine **ULONG,** die den neuen Wert angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der vom *Schlüsselparameter* angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [**Angeben von Clientinformationen.**](specifying-client-information.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[**Angeben von Clientinformationen**](specifying-client-information.md)
</dt> </dl>

 

 




