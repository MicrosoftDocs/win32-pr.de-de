---
description: Die OnDisconnect-Methode wird aufgerufen, wenn auf der Eigenschaften Seite das zugeordnete-Objekt freigegeben werden soll.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Cbasepropertypage. OnDisconnect-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364821"
---
# <a name="cbasepropertypageondisconnect-method"></a>Cbasepropertypage. OnDisconnect-Methode

Die- `OnDisconnect` Methode wird aufgerufen, wenn die Eigenschaften Seite das zugeordnete-Objekt freigeben soll.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassen Implementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbasepropertypage:: abtobjects**](cbasepropertypage-setobjects.md) -Methode ruft die- `OnDisconnect` Methode auf. `OnDisconnect`Überschreiben Sie, um alle Zeiger freizugeben, die in der [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode abgerufen wurden.

## <a name="examples"></a>Beispiele


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




