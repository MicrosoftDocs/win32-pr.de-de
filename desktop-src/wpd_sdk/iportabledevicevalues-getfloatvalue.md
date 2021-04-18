---
description: Die getFloatValue-Methode ruft einen Gleit Komma Wert (Typ VT R4) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Iportabledevicevalues:: getFloatValue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364688"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>Iportabledevicevalues:: getFloatValue-Methode

Die **getFloatValue** -Methode **Ruft einen Gleit** Komma Wert (Typ VT R4) ab, der \_ durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
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

Zeiger auf den abgerufenen **float** -Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                             | Beschreibung                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>    | Die von *Key* angegebene Eigenschaft ist kein **float** -Typ.<br/>  |
| <dl> <dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportabledebug:: setfloatvalue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




