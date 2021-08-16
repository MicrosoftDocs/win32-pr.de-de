---
description: Die OnApplyChanges-Methode wird aufgerufen, wenn der Benutzer Änderungen auf die Eigenschaftenseite wendet.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: CBasePropertyPage.OnApplyChanges-Methode (Cprop.h)
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
ms.openlocfilehash: f822bed433af6e3fab0250e06a04911ee10187039036211974b046b32df6b7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823106"
---
# <a name="cbasepropertypageonapplychanges-method"></a>CBasePropertyPage.OnApplyChanges-Methode

Die `OnApplyChanges` -Methode wird aufgerufen, wenn der Benutzer Änderungen auf die Eigenschaftenseite wendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassenimplementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die [**CBasePropertyPage::Apply-Methode**](cbasepropertypage-apply.md) ruft auf, wenn `OnApplyChanges` das [**CBasePropertyPage::m \_ bDirty-Flag**](cbasepropertypage-m-bdirty.md) **TRUE ist.** Überschreiben Sie , um die Änderungen zu verarbeiten, und `OnApplyChanges` setzen Sie m **\_ bDirty auf** FALSE **zurück.**

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
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




