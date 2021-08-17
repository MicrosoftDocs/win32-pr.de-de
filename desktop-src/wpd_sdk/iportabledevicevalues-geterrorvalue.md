---
description: Die GetErrorValue-Methode ruft einen HRESULT-Wert (Typ VT ERROR) ab, \_ der durch einen Schlüssel angegeben wird.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: IPortableDeviceValues::GetErrorValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 594ed35191433ec817f1e37bd4c037652f6b564d3a5c6191d56ad1c5e855ab34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697149"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a>IPortableDeviceValues::GetErrorValue-Methode

Die **GetErrorValue-Methode** ruft einen **HRESULT-Wert** (Typ VT ERROR) ab, \_ der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Schlüssel,** der das abzurufende Element angibt.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Zeiger auf den abgerufenen **HRESULT-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch key angegebene *Eigenschaft* ist kein **HRESULT-Typ.**<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetErrorValue**](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




