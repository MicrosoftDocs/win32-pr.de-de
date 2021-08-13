---
description: Die SetIPortableDeviceValuesCollectionValue-Methode fügt einen neuen IPortableDeviceValuesCollection-Wert (Typ VT UNKNOWN) hinzu oder überschreibt einen \_ vorhandenen.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7f015333a8d384743d0e8ea16000252a4e60fd24ab0637b92ee3d85ddb42a1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697088"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a>IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue-Methode

Die **SetIPortableDeviceValuesCollectionValue-Methode** fügt einen neuen **IPortableDeviceValuesCollection-Wert** (Typ VT UNKNOWN) hinzu oder überschreibt einen \_ vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Objekt,** das das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*pValue* \[ In\]
</dt> <dd>

Zeiger auf eine **IPortableDeviceValuesCollection-Schnittstelle,** die den neuen Wert angibt. Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft **AddRef darauf** auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über denselben  Schlüssel verfügt, der vom Schlüsselparameter angegeben wird, überschreibt er den vorhandenen Wert ohne Warnung. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




