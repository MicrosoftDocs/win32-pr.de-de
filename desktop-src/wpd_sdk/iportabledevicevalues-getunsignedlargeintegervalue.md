---
description: Die GetUnsignedLargeIntegerValue-Methode ruft einen ULONGLONG-Wert (Typ VT \_ UI8) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: IPortableDeviceValues::GetUnsignedLargeIntegerValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: df10faa20094623940e9694a5612c4f49b45f3c979d7e05df3239512cb021ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194029"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a>IPortableDeviceValues::GetUnsignedLargeIntegerValue-Methode

Die **GetUnsignedLargeIntegerValue-Methode** ruft einen **ULONGLONG-Wert** (Typ VT \_ UI8) ab, der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
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

Zeiger auf den abgerufenen **ULONGLONG-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                        |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch *key* angegebene Eigenschaft ist kein **ULONGLONG-Typ.**<br/> |
| <dl> <dt>**HRESULT \_ AUS \_ WIN32 (FEHLER \_ NICHT \_ GEFUNDEN)**</dt> </dl> | Die vom *Schlüssel* angegebene Eigenschaft befindet sich nicht in der Auflistung.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




