---
description: Die getunsignedintegervalue-Methode ruft einen Ulong-Wert (Type VT UI4) ab, der \_ von einem Schlüssel angegeben wird.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'Iportabledevicevalues:: getunsignedintegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373665"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a>Iportabledevicevalues:: getunsignedintegervalue-Methode

Die **getunsignedintegervalue** -Methode ruft einen **ulong** -Wert (Type VT UI4) ab, der \_ von einem Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
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

Zeiger auf den abgerufenen **ulong** -Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>                   | Die von *Key* angegebene Eigenschaft ist kein **ulong** -Typ.<br/>  |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportableendvicevalues:: Server Value**](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienst Methoden](retrieving-supported-methods.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




