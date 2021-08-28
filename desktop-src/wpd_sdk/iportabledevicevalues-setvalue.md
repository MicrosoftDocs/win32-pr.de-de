---
description: Die SetValue-Methode fügt einen neuen PROPVARIANT-Wert hinzu oder überschreibt einen vorhandenen.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: IPortableDeviceValues::SetValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f6af975b2876a177207df4f57bfe1f76d78a4b7239ce6d9c4cfcab52f0cf9042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055040"
---
# <a name="iportabledevicevaluessetvalue-method"></a>IPortableDeviceValues::SetValue-Methode

Die **SetValue-Methode** fügt einen neuen **PROPVARIANT-Wert** hinzu oder überschreibt einen vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Objekt,** das das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*pValue* \[ In\]
</dt> <dd>

Eine **PROPVARIANT,** die den neuen Wert angibt. Das SDK kopiert den Wert, sodass der Aufrufer die lokale Variable durch Aufrufen **von PropVariantClear** nach dem Aufruf dieser Methode frei geben kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn der VARTYPE für *pValue* VT VECTOR oder VT UI1 ist, wird das Festlegen eines Nullpuffers oder eines Puffers der \_ \_ Größe 0  (null) nicht unterstützt. Beispielsweise sind weder pValue.caub.pElems = **NULL** noch pValue.caub.cElems = 0 zulässig.

Diese Methode kann verwendet werden, um einen Wert eines beliebigen Typs aus der Auflistung abzurufen. Wenn Sie den Werttyp jedoch im Voraus kennen, verwenden Sie eine der spezialisierten **Set...-Methoden** dieser Schnittstelle, um den Aufwand zu vermeiden, direkt mit PROPVARIANT-Werten zu arbeiten.

Wenn ein vorhandener Wert über denselben  Schlüssel verfügt, der vom Schlüsselparameter angegeben wird, überschreibt er den vorhandenen Wert ohne Warnung. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




