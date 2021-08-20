---
title: TTM_GETTOOLINFO-Nachricht (Commctrl.h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement über ein Tool verwaltet.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- TTM_GETTOOLINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f19243603ab5d2ba62d498a5595528e39b33658c7a8e4aa0638888806684ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166373"
---
# <a name="ttm_gettoolinfo-message"></a>TTM \_ GETTOOLINFO-Nachricht

Ruft die Informationen ab, die ein QuickInfo-Steuerelement über ein Tool verwaltet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Beim Senden der Nachricht identifizieren die **Member hwnd** und **uId** ein Tool, und der **cbSize-Member** muss die Größe der Struktur angeben. Wenn Sie diese Meldung verwenden, um den QuickInfo-Text abzurufen, stellen Sie sicher, dass der **lpszText-Member** der **TOOLINFO-Struktur** auf einen gültigen Puffer der adquaten Größe zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn das QuickInfo-Steuerelement das Tool enthält, empfängt die [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Informationen zum Tool.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein QuickInfo-Steuerelement neu positioniert.


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ GETTOOLINFOW** (Unicode) und **TTM \_ GETTOOLINFOA** (ANSI)<br/>           |



 

 





