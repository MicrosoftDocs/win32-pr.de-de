---
description: Die Methode "* tiportabledevicevaluesvalue" fügt einen neuen iportabledevicevalues-Wert hinzu (Type VT \_ unknown) oder überschreibt eine vorhandene.
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'Iportabledevicevalues:: tportabledevicevaluesvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372330"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a>Iportabledevicevalues:: endportabledevicevaluesvalue-Methode

Die Methode "* **tiportabledevicevaluesvalue** " fügt einen neuen **iportabledevicevalues** -Wert hinzu (Type VT \_ unknown) oder überschreibt eine vorhandene.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
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

Ein Zeiger auf eine **iportablede vicevalues** -Schnittstelle, die den neuen Wert angibt. Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft die **adressf** auf.

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

[**Iportableendvicevalues:: getiportableendvicevaluesvalue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




