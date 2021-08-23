---
description: 'IPortableDeviceValuesCollection::GetCount-Methode: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: IPortableDeviceValuesCollection::GetCount-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: abf157a8a539d98c5b75826e4568df7c3209a0efc2dab49f6487250dd08ae391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707370"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>IPortableDeviceValuesCollection::GetCount-Methode

Die **GetCount-Methode** ruft die Anzahl der Elemente in der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcElems* \[ In\]
</dt> <dd>

Zeiger auf ein **DWORD,** das die Anzahl der **IPortableDeviceValues-Schnittstellen** in der Auflistung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | Ein erforderliches Zeigerargument war **NULL.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




