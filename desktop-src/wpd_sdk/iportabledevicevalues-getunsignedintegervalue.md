---
description: Die GetUnsignedIntegerValue-Methode ruft einen ULONG-Wert (Typ VT UI4) ab, \_ der durch einen Schlüssel angegeben wird.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: IPortableDeviceValues::GetUnsignedIntegerValue-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: eeb418d3d0aa42675f3d5766f2a8d08e1ad2377bbaa4a2a07f4ba96524d3dec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026838"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a>IPortableDeviceValues::GetUnsignedIntegerValue-Methode

Die **GetUnsignedIntegerValue-Methode** ruft einen **ULONG-Wert** (Typ VT UI4) ab, \_ der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
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

Zeiger auf den abgerufenen **ULONG-Wert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch key angegebene *Eigenschaft* ist kein **ULONG-Typ.**<br/>  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen von unterstützten Dienstereignissen.](retrieving-supported-events.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[Abrufen unterstützter Dienstereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienstmethoden](retrieving-supported-methods.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




