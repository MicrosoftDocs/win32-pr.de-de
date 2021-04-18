---
description: Die GetType-Methode ruft den Datentyp der Elemente in der Auflistung ab.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Iportabledevicepropvariantcollection:: GetType-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365976"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>Iportabledevicepropvariantcollection:: GetType-Methode

Die **GetType** -Methode ruft den Datentyp der Elemente in der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pvt* \[ vorgenommen\]
</dt> <dd>

Ein Platform SDK- **VarType** -Enumerationswert, der den Datentyp aller Elemente in der Auflistung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Ein erforderliches Zeigerargument war **null**.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Elemente, die in einer **iportabledevicepropvariantcollection** gespeichert sind, weisen denselben Typ auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




