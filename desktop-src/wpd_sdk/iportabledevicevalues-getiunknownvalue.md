---
description: Die GetIUnknownValue-Methode ruft einen IUnknown-Schnittstellenwert (Typ VT \_ UNKNOWN) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: IPortableDeviceValues::GetIUnknownValue-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: daf1164fefdc414a84508e4b295620af3cb671e9da624dd60cc08541c5c4fd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963649"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>IPortableDeviceValues::GetIUnknownValue-Methode

Die **GetIUnknownValue-Methode** ruft einen **IUnknown-Schnittstellenwert** (Typ VT \_ UNKNOWN) ab, der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Schlüssel,** der das abzurufende Element angibt.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die abgerufene **IUnknown-Schnittstelle** empfängt. Der Aufrufer ist für den Aufruf **von Release** für die abgerufene Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                             |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die vom *Schlüssel* angegebene Eigenschaft ist keine **IUnknown-Schnittstelle.**<br/> |
| <dl> <dt>**HRESULT \_ AUS \_ WIN32 (FEHLER \_ NICHT \_ GEFUNDEN)**</dt> </dl> | Die vom *Schlüssel* angegebene Eigenschaft befindet sich nicht in der Auflistung.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




