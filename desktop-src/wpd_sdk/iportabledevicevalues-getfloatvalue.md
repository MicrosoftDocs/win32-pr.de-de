---
description: Die GetFloatValue-Methode ruft einen FLOAT-Wert (Typ VT \_ R4) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: IPortableDeviceValues::GetFloatValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 364b5de9bbf8b3c5bb307b7bbc0e11fc018393c301c0931e065331879ec096fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430823"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>IPortableDeviceValues::GetFloatValue-Methode

Die **GetFloatValue-Methode** ruft einen **FLOAT-Wert** (Typ VT \_ R4) ab, der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Schlüssel,** der das abzurufende Element angibt.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Zeiger auf den abgerufenen **FLOAT-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                             | Beschreibung                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>    | Die durch *key* angegebene Eigenschaft ist kein **FLOAT-Typ.**<br/>  |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl> | Die vom *Schlüssel* angegebene Eigenschaft befindet sich nicht in der Auflistung.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetFloatValue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




