---
description: Die onreceivemess-Methode wird aufgerufen, wenn das Dialogfeld eine Meldung empfängt.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Cbasepropertypage. onreceivemess Age-Methode (cprop. h)
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
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373629"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>Cbasepropertypage. onreceivemess Age-Methode

Die- `OnReceiveMessage` Methode wird aufgerufen, wenn das Dialogfeld eine Meldung empfängt.

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

*HWND* 
</dt> <dd>

Handle für das Fenster.

</dd> <dt>

*Umschlag* 
</dt> <dd>

Message (Nachricht):

</dd> <dt>

*wParam* 
</dt> <dd>

Der erste Message-Parameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Der zweite Meldungs Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück. Die Dialogfeld Prozedur gibt diesen Wert zurück. Weitere Informationen finden Sie in der Platform SDK-Dokumentation.

## <a name="remarks"></a>Bemerkungen

Die Basisklassen Implementierung ruft **defwindowproc** auf. Überschreiben Sie diese Methode, um Meldungen zu verarbeiten, die sich auf die Dialogfeld Steuerelemente Wenn die über schreibende Methode eine bestimmte Nachricht nicht verarbeitet, sollte Sie die Basisklassen Methode aufruft.

Wenn der Benutzereigenschaften über die Dialogfeld Steuerelemente ändert, legen Sie das [**\_ bdirty-Flag "cbasepropertypage:: m**](cbasepropertypage-m-bdirty.md) " auf " **true**" fest. Anschließend können Sie die **ipropertypagesite:: OnStatusChange** -Methode auf dem [**cbasepropertypage:: m \_ ppagesite**](cbasepropertypage-m-ppagesite.md) -Zeiger aufrufen, um den Frame zu informieren.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird auf einen Klick auf eine Schaltfläche reagiert, indem eine Element Variable aktualisiert wird, die in der abgeleiteten Klasse definiert wird. Dieses Beispiel zeigt auch eine Hilfsfunktion zum Festlegen des Status "Dirty" der Eigenschaften Seite.


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
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




