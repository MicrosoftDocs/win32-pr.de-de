---
description: Die GetType-Methode ruft den Datentyp der Elemente in der Auflistung ab.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: IPortableDevicePropVariantCollection::GetType-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 0c29e47cd08b5c31012df92ca04e018d38f7adb7f8802ec534682289852f518b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963739"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>IPortableDevicePropVariantCollection::GetType-Methode

Die **GetType-Methode** ruft den Datentyp der Elemente in der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvt* \[ out\]
</dt> <dd>

Ein Platform SDK **VARTYPE-Enumerationswert,** der den Datentyp aller Elemente in der Auflistung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Ein erforderliches Zeigerargument war **NULL.**<br/> |



 

## <a name="remarks"></a>Hinweise

Alle Elemente, die in einer **IPortableDevicePropVariantCollection** gespeichert sind, sind vom gleichen Typ.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




