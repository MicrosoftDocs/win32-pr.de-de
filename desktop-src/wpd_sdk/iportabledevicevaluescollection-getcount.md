---
description: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'Iportabledevicevaluescollection:: GetCount-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353810"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>Iportabledevicevaluescollection:: GetCount-Methode

Die **GetCount** -Methode ruft die Anzahl der Elemente in der Auflistung ab.

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

Zeiger auf ein **DWORD** , das die Anzahl der **iportabledevicevalues** -Schnittstellen in der Auflistung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Ein erforderliches Zeigerargument war **null**.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportableabvicevaluescollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




