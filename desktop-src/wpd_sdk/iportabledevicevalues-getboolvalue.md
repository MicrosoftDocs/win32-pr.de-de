---
description: Die GetBoolValue-Methode ruft einen booleschen Wert (Typ VT \_ bool) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'Iportabledevicevalues:: GetBoolValue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358350"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a>Iportabledevicevalues:: GetBoolValue-Methode

Die **GetBoolValue** -Methode ruft einen **booleschen** Wert (Typ VT \_ bool) ab, der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
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

Zeiger auf den abgerufenen **booleschen** Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>                   | Die von *Key* angegebene Eigenschaft ist kein **boolescher** Typ.<br/>   |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Festlegen von Eigenschaften für ein einzelnes Objekt](setting-properties-for-a-single-object.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportabledebug:: SetBoolValue**](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md)
</dt> <dt>

[Festlegen von Eigenschaften für ein einzelnes Objekt](setting-properties-for-a-single-object.md)
</dt> <dt>

[Schreiben von Content-Object-Eigenschaften](writing-content-object-properties.md)
</dt> </dl>

 

 




