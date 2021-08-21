---
description: Die OnReceiveMessage-Methode wird aufgerufen, wenn das Dialogfeld eine Nachricht empfängt.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: CBasePropertyPage.OnReceiveMessage-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833f0f7ab9192d88440afff75a36fee744ac2fe053c6fe99d1940686c452799a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158132"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>CBasePropertyPage.OnReceiveMessage-Methode

Die `OnReceiveMessage` -Methode wird aufgerufen, wenn das Dialogfeld eine Nachricht empfängt.

## <a name="syntax"></a>Syntax


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle zum Fenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Message (Nachricht):

</dd> <dt>

*wParam* 
</dt> <dd>

Erster Meldungsparameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Zweiter Meldungsparameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück. Die Dialogprozedur gibt diesen Wert zurück. Weitere Informationen finden Sie in der Dokumentation zum Platform SDK.

## <a name="remarks"></a>Hinweise

Die Basisklassenimplementierung ruft **DefWindowProc auf.** Überschreiben Sie diese Methode, um Meldungen zu behandeln, die sich auf die Dialogsteuerelemente beziehen. Wenn die überschreibende Methode eine bestimmte Nachricht nicht behandelt, sollte sie die Basisklassenmethode aufrufen.

Wenn der Benutzer Eigenschaften über die Dialogsteuerelemente ändert, legen Sie das [**Flag CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) auf **TRUE fest.** Rufen Sie dann die **IPropertyPageSite::OnStatusChange-Methode** für den [**CBasePropertyPage::m \_ pPageSite-Zeiger**](cbasepropertypage-m-ppagesite.md) auf, um den Frame zu informieren.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird auf einen Schaltflächenklick reagiert, indem eine Membervariable aktualisiert wird, von der angenommen wird, dass sie in der abgeleiteten Klasse definiert ist. Dieses Beispiel zeigt auch eine Hilfsfunktion zum Festlegen des geänderten Status der Eigenschaftenseite.


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




