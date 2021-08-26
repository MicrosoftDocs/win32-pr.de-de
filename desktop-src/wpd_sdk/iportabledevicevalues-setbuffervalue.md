---
description: Die SetBufferValue-Methode fügt einen neuen BYTE-Wert \* (Typ VT \_ VECTOR \| VT UI1) hinzu oder überschreibt \_ einen vorhandenen.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: IPortableDeviceValues::SetBufferValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 25a087c6f2d1e254e225f82ef794915898fbc20c7203fe20315d51f78e9770f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055100"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>IPortableDeviceValues::SetBufferValue-Methode

Die **SetBufferValue-Methode** fügt einen neuen **BYTE-Wert** \* (Typ VT VECTOR \_ \| VT UI1) hinzu oder überschreibt \_ einen vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
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

Ein **BYTE, \*** das die Daten enthält, die in das Element geschrieben werden. Die übermittelten Pufferdaten werden in die Schnittstelle kopiert, sodass der Aufrufer diesen Puffer nach diesem Aufruf frei geben kann.

</dd> <dt>

*cbValue* \[ In\]
</dt> <dd>

Die Größe des Werts, auf den *pValue* zeigt, in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn ein vorhandener Wert über denselben  Schlüssel verfügt, der vom Schlüsselparameter angegeben wird, überschreibt er den vorhandenen Wert ohne Warnung. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

Das Festlegen **eines NULL-Puffers** oder eines Puffers der Größe 0 (null) wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




