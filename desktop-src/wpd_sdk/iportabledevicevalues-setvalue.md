---
description: Die SetValue-Methode fügt einen neuen PROPVARIANT-Wert hinzu oder überschreibt eine vorhandene.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Iportabledevicevalues:: SetValue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370642"
---
# <a name="iportabledevicevaluessetvalue-method"></a>Iportabledevicevalues:: SetValue-Methode

Die **SetValue** -Methode fügt einen neuen **PROPVARIANT** -Wert hinzu oder überschreibt eine vorhandene.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Ein **PROPVARIANT** -Wert, der den neuen Wert angibt. Das SDK kopiert den Wert, sodass der Aufrufer die lokale Variable durch Aufrufen von **propvariantclear** freigeben kann, nachdem diese Methode aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn VarType für *pValue den Wert* VT \_ Vector oder VT \_ UI1 aufweist, wird das Festlegen eines Puffers, **der NULL** oder NULL ist, nicht unterstützt. Beispielsweise sind weder pValue. Caub. pelems = **null** noch pValue. Caub. celems = 0 zulässig.

Diese Methode kann verwendet werden, um einen Wert eines beliebigen Typs aus der Auflistung abzurufen. Wenn Sie jedoch den Werttyp im Voraus kennen, verwenden Sie eine der spezialisierten **Set...** -Methoden dieser Schnittstelle, um den mehr Aufwand bei der direkten Arbeit mit PROPVARIANT-Werten zu vermeiden.

Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**Iportablede vicevalues:: removeValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




