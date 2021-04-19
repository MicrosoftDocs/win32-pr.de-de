---
description: Die onapplychanges-Methode wird aufgerufen, wenn der Benutzer Änderungen auf die Eigenschaften Seite anwendet.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Cbasepropertypage. onapplychanges-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369256"
---
# <a name="cbasepropertypageonapplychanges-method"></a>Cbasepropertypage. onapplychanges-Methode

Die- `OnApplyChanges` Methode wird aufgerufen, wenn der Benutzer Änderungen auf der Eigenschaften Seite anwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassen Implementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbasepropertypage:: apply**](cbasepropertypage-apply.md) -Methode ruft auf, `OnApplyChanges` Wenn das [**\_ bdirty-Flag "cbasepropertypage:: m**](cbasepropertypage-m-bdirty.md) " auf " **true**" fest. `OnApplyChanges`Überschreiben Sie, um die Änderungen zu verarbeiten und **m \_ bdirty** auf **false** zurückzusetzen.

## <a name="examples"></a>Beispiele


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
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

 

 




