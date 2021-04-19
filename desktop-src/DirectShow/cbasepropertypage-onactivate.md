---
description: Die onaktivierungs-Methode wird aufgerufen, wenn die Eigenschaften Seite aktiviert wird.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Cbasepropertypage. onaktivierungs-Methode (cprop. h)
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
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369115"
---
# <a name="cbasepropertypageonactivate-method"></a>Cbasepropertypage. onaktivierungs-Methode

Die- `OnActivate` Methode wird aufgerufen, wenn die Eigenschaften Seite aktiviert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassen Implementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbasepropertypage:: Aktivierungs**](cbasepropertypage-activate.md) -Methode ruft die- `OnActivate` Methode auf. Überschreiben Sie in der abgeleiteten Klasse, `OnActivate` um das Dialogfeld zu initialisieren.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein TrackBar-Steuerelement initialisiert. In diesem Beispiel wird davon ausgegangen, dass **m \_ powningfilter** ein Zeiger auf eine benutzerdefinierte Schnittstelle für den Filter ist, der der Eigenschaften Seite zugeordnet ist. (Verwenden Sie die [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode, um solche Zeiger zu initialisieren.)


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
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




