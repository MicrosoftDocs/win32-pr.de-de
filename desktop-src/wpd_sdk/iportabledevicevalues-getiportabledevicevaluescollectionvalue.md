---
description: Die GetIPortableDeviceValuesCollectionValue-Methode ruft einen IPortableDeviceValuesCollection-Wert (Typ VT UNKNOWN) ab, der durch einen \_ Schlüssel angegeben wird.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cbbea545f0f3c75281c5abb7e68795750521251392529d037bf18682e84dc436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697078"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue-Methode

Die **GetIPortableDeviceValuesCollectionValue-Methode** ruft einen **IPortableDeviceValuesCollection-Wert** (Typ VT UNKNOWN) ab, der durch einen \_ Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Schlüssel,** der das abzurufende Element angibt.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die abgerufene [**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md) empfängt. Der Aufrufer ist für den Aufruf von **Release auf** der abgerufenen Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch key angegebene *Eigenschaft* ist keine **IPortableDeviceValuesCollection-Schnittstelle.**<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/>                                |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter Abrufen der von einem Gerät [unterstützten Renderingfunktionen.](retrieving-the-rendering-capabilities-supported-by-a-device.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




