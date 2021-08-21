---
description: Die GetValue-Methode ruft einen PROPVARIANT-Wert ab, der durch einen Schlüssel angegeben wird.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: IPortableDeviceValues::GetValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cce387bfc08c48547603d8b30a3952952f1e2decf70e06986ea4fb477fe4fdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843032"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>IPortableDeviceValues::GetValue-Methode

Die **GetValue-Methode** ruft einen **PROPVARIANT-Wert** ab, der durch einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
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

Zeiger auf den abgerufenen **PROPVARIANT-Wert.** Der Aufrufer muss den Arbeitsspeicher durch Aufrufen von **PropVariantClear frei** geben, wenn er damit fertig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn VARTYPE für *pValue* VT VECTOR oder VT UI1 ist, wird das Abrufen eines Nullpuffers oder eines Puffers der \_ Größe \_ 0 (null) nicht unterstützt.  Beispielsweise sind weder pValue.caub.pElems = **NULL** noch pValue.caub.cElems = 0 zulässig.

Diese Methode kann verwendet werden, um einen Wert eines beliebigen Typs aus der Auflistung abzurufen. Wenn Sie den Werttyp jedoch im Voraus kennen, verwenden Sie eine der speziellen Abrufmethoden dieser Schnittstelle, um den Mehraufwand der direkten Arbeit mit PROPVARIANT-Werten zu vermeiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues::SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




