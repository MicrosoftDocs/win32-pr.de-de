---
description: Die getunsignedlargeintegervalue-Methode ruft einen ULONGLONG-Wert (Typ VT UI8) ab, der \_ von einem Schlüssel angegeben wird.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Iportabledevicevalues:: getunsignedlargeingetegervalue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358289"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a>Iportabledevicevalues:: getunsignedlargeingetegervalue-Methode

Die **getunsignedlargeintegervalue** -Methode ruft einen **ULONGLONG** -Wert (Typ VT UI8) ab, der \_ von einem Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.

</dd> <dt>

*pValue* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den abgerufenen **ULONGLONG** -Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                        |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>                   | Die von *Key* angegebene Eigenschaft ist kein **ULONGLONG** -Typ.<br/> |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportableendvicevalues:: Abbild-ID-Wert**](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




