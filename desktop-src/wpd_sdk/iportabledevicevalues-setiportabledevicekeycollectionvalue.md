---
description: Die Methode "* tiportabledevicekeycollectionvalue" fügt einen neuen Wert für "stiportabledevicekeycollectionvalue" (Typ "VT \_ unknown") hinzu oder überschreibt eine vorhandene.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'Iportabledevicevalues:: tportabledevicekeycollectionvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366973"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a>Iportabledevicevalues:: endportabledevicekeycollectionvalue-Methode

Die Methode "* **tiportabledevicekeycollectionvalue** " fügt einen neuen Wert für " **stiportabledevicekeycollectionvalue** " (Typ "VT \_ unknown") hinzu oder überschreibt eine vorhandene.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
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

Zeiger auf eine **iportabledevicekeycollection** -Schnittstelle, die den neuen Wert angibt. Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft die **adressf** auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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

[**Iportablede vicevalues:: getiportabledevicekeycollectionvalue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




