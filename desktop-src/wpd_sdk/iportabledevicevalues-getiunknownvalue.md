---
description: Die getiunknownvalue-Methode ruft einen IUnknown-Schnittstellen Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'Iportabledevicevalues:: getiunknownvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365423"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>Iportabledevicevalues:: getiunknownvalue-Methode

Die **getiunknownvalue** -Methode ruft einen **IUnknown** -Schnittstellen Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.

</dd> <dt>

*ppValue* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die abgerufene **IUnknown** -Schnittstelle empfängt. Der Aufrufer ist für das Aufrufen von **Release** an der abgerufenen Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                             |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>                   | Die von *Key* angegebene Eigenschaft ist keine **IUnknown** -Schnittstelle.<br/> |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: Server Wert**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




