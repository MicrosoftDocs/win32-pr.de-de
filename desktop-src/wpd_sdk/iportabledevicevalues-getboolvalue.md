---
description: Die GetBoolValue-Methode ruft einen booleschen Wert (Typ VT BOOL) ab, \_ der durch einen Schlüssel angegeben wird.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: IPortableDeviceValues::GetBoolValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26006d151cd3adfc9f1c3f892cca05724c4ba54dc273cbbf58bd96c5779ccefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807020"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a>IPortableDeviceValues::GetBoolValue-Methode

Die **GetBoolValue-Methode** ruft einen **booleschen Wert** (Typ VT BOOL) ab, \_ der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
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

Zeiger auf den abgerufenen **BOOL-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch key angegebene *Eigenschaft* ist kein **BOOL-Typ.**<br/>   |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Festlegen von Eigenschaften für ein einzelnes Objekt.](setting-properties-for-a-single-object.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBoolValue**](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[Abrufen unterstützter Dienstereignisse](retrieving-supported-events.md)
</dt> <dt>

[Festlegen von Eigenschaften für ein einzelnes Objekt](setting-properties-for-a-single-object.md)
</dt> <dt>

[Schreiben von Inhaltsobjekteigenschaften](writing-content-object-properties.md)
</dt> </dl>

 

 




