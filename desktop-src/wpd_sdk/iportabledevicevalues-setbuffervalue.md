---
description: Die setbuffervalue-Methode fügt einen neuen \* Bytewert (Type VT \_ Vector \| VT \_ UI1) hinzu oder überschreibt eine vorhandene.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'Iportabledevicevalues:: setbuffervalue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359670"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>Iportabledevicevalues:: setbuffervalue-Methode

Die **setbuffervalue** -Methode fügt einen neuen  \* Bytewert (Type VT \_ Vector \| VT \_ UI1) hinzu oder überschreibt eine vorhandene.

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

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Ein **Byte \*** , das die Daten enthält, die in das Element geschrieben werden sollen. Die gesendeten Puffer Daten werden in die-Schnittstelle kopiert, sodass der Aufrufer diesen Puffer nach dem Aufruf freigeben kann.

</dd> <dt>

*cbValue* \[ in\]
</dt> <dd>

Die Größe des Werts, auf den *pValue* zeigt (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben. Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

Das Festlegen eines Puffers, der **null oder NULL** ist, wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: getbuffervalue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




