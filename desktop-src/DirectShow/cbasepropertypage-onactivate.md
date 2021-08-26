---
description: Die OnActivate-Methode wird aufgerufen, wenn die Eigenschaftenseite aktiviert wird.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: CBasePropertyPage.OnActivate-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f779f5bc6c33f15b5e2b1da83a72d38b91c1785564e9cace99b91469e9fdfc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052570"
---
# <a name="cbasepropertypageonactivate-method"></a>CBasePropertyPage.OnActivate-Methode

Die `OnActivate` -Methode wird aufgerufen, wenn die Eigenschaftenseite aktiviert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassenimplementierungen geben S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die [**CBasePropertyPage::Activate-Methode**](cbasepropertypage-activate.md) ruft die `OnActivate` -Methode auf. Überschreiben Sie in der abgeleiteten Klasse , `OnActivate` um das Dialogfeld zu initialisieren.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Trackbar-Steuerelement initialisiert. In diesem Beispiel wird davon ausgegangen, dass **m \_ pOwningFilter** ein Zeiger auf eine benutzerdefinierte Schnittstelle auf dem Filter ist, der der Eigenschaftenseite zugeordnet ist. (Verwenden Sie die [**CBasePropertyPage::OnConnect-Methode,**](cbasepropertypage-onconnect.md) um solche Zeiger zu initialisieren.)


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




