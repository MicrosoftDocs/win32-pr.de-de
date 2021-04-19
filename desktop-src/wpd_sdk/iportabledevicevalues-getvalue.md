---
description: Die GetValue-Methode ruft einen durch einen Schlüssel angegebenen PROPVARIANT-Wert ab.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Iportabledevicevalues:: GetValue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352885"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>Iportabledevicevalues:: GetValue-Methode

Die **GetValue** -Methode ruft einen durch einen Schlüssel angegebenen **PROPVARIANT** -Wert ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
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

Zeiger auf den abgerufenen **PROPVARIANT** -Wert. Der Aufrufer muss den Speicher freigeben, indem er **propvariantclear** aufruft, wenn er damit abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn VarType für *pValue den Wert* VT \_ Vector oder VT \_ UI1 aufweist, wird das  Abrufen eines Puffers mit der Größe Null oder der Größe 0 (null) nicht unterstützt. Beispielsweise sind weder pValue. Caub. pelems = **null** noch pValue. Caub. celems = 0 zulässig.

Diese Methode kann verwendet werden, um einen Wert eines beliebigen Typs aus der Auflistung abzurufen. Wenn Sie jedoch den Werttyp im Voraus kennen, verwenden Sie eine der spezialisierten Abruf Methoden dieser Schnittstelle, um den mehr Aufwand bei der direkten Arbeit mit PROPVARIANT-Werten zu vermeiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: removeValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**Iportabledebug:: SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




