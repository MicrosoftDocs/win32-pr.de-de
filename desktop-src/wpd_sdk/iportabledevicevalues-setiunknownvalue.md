---
description: Die SetIUnknownValue-Methode fügt einen neuen IUnknown-Wert (Typ VT \_ UNKNOWN) hinzu oder überschreibt einen vorhandenen Wert.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: IPortableDeviceValues::SetIUnknownValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c4a7c8a77cfef505b2a507b6281b931eea7f09c4ea1fbc79e651e7f517593799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697051"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a>IPortableDeviceValues::SetIUnknownValue-Methode

Die **SetIUnknownValue-Methode** fügt einen neuen **IUnknown-Wert** (Typ VT \_ UNKNOWN) hinzu oder überschreibt einen vorhandenen Wert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY,** der das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*pValue* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **IUnknown-Schnittstelle,** die den neuen Wert angibt. Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft **AddRef** darauf auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der vom *Schlüsselparameter* angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




