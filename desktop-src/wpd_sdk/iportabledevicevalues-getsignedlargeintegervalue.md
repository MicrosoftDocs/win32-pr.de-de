---
description: Die GetSignedLargeIntegerValue-Methode ruft einen LONGLONG-Wert (Typ VT \_ I8) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: IPortableDeviceValues::GetSignedLargeIntegerValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 516d7c08b68e4480b3240ea9335793589114070859cf28d5cf91e645b616a2db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055110"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a>IPortableDeviceValues::GetSignedLargeIntegerValue-Methode

Die **GetSignedLargeIntegerValue-Methode** ruft einen **LONGLONG-Wert** (Typ VT \_ I8) ab, der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
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

Zeiger auf den abgerufenen **ULONG-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die vom *Schlüssel* angegebene Eigenschaft ist kein **LONGLONG-Typ.**<br/> |
| <dl> <dt>**HRESULT \_ AUS \_ WIN32 (FEHLER \_ NICHT \_ GEFUNDEN)**</dt> </dl> | Die vom *Schlüssel* angegebene Eigenschaft befindet sich nicht in der Auflistung.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




