---
description: Die GetCount-Methode ruft die Anzahl der Schlüssel in dieser Auflistung ab.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'Iportabledevicekeycollection:: GetCount-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358735"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a>Iportabledevicekeycollection:: GetCount-Methode

Die **GetCount** -Methode ruft die Anzahl der Schlüssel in dieser Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcelems* \[ in\]
</dt> <dd>

Zeiger auf ein **DWORD** , das die Anzahl der Schlüssel in der Auflistung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Ein erforderliches Zeigerargument war **null**.<br/> |



 

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

 

 




