---
description: Die geterrorvalue-Methode ruft einen HRESULT-Wert (Type VT Error) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'Iportabledevicevalues:: geterrorvalue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356486"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a>Iportabledevicevalues:: geterrorvalue-Methode

Die **geterrorvalue** -Methode ruft einen **HRESULT** -Wert (Type VT Error) ab, der \_ durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
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

Zeiger auf den abgerufenen **HRESULT** -Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>                   | Die von *Key* angegebene Eigenschaft ist kein **HRESULT** -Typ.<br/> |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: Server-Wert**](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




