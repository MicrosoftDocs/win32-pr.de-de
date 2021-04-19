---
description: Die GetAt-Methode ruft einen PropertyKey aus der Auflistung nach Index ab.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Iportabledevicekeycollection:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359647"
---
# <a name="iportabledevicekeycollectiongetat-method"></a>Iportabledevicekeycollection:: GetAt-Methode

Die **GetAt** -Methode ruft einen **PropertyKey** aus der Auflistung nach Index ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

**DWORD** , das den Index des abzurufenden Schlüssels enthält.

</dd> <dt>

*pkey* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **PropertyKey** -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der über gegebene Index lag außerhalb des zulässigen Bereichs.<br/>     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | Ein erforderliches Zeigerargument war **null**.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienst Methoden](retrieving-supported-methods.md)
</dt> </dl>

 

 




