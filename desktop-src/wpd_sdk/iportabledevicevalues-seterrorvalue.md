---
description: Die SetErrorValue-Methode fügt einen neuen HRESULT-Wert (Typ VT ERROR) hinzu oder \_ überschreibt einen vorhandenen.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: IPortableDeviceValues::SetErrorValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 41bb9a6d8f2878b9bcfac6584c39fd55153ecae8a539c7f8886a5d0eb90d1bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026788"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a>IPortableDeviceValues::SetErrorValue-Methode

Die **SetErrorValue-Methode** fügt einen neuen **HRESULT-Wert** (Typ VT ERROR) hinzu oder \_ überschreibt einen vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
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

Ein **HRESULT,** das den neuen Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über  den gleichen Schlüssel verfügt, der vom Schlüsselparameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetErrorValue**](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




