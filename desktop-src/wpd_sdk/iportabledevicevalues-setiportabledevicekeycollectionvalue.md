---
description: Die SetIPortableDeviceKeyCollectionValue-Methode fügt einen neuen SetIPortableDeviceKeyCollectionValue-Wert (Typ VT UNKNOWN) hinzu oder überschreibt einen \_ vorhandenen.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 100dd614978260824fa14cefc22e1bf7fdd5d11e474e4f58124685fc8d8f2eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963569"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a>IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue-Methode

Die **SetIPortableDeviceKeyCollectionValue-Methode** fügt einen neuen **SetIPortableDeviceKeyCollectionValue-Wert** (Typ VT UNKNOWN) hinzu oder überschreibt einen \_ vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Objekt,** das das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*pValue* \[ In\]
</dt> <dd>

Zeiger auf eine **IPortableDeviceKeyCollection-Schnittstelle,** die den neuen Wert angibt. Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft **AddRef darauf** auf.

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

[**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




