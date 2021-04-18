---
title: TTM_GETTOOLINFO Meldung (kommstrg. h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- Windows-Steuerelemente für TTM_GETTOOLINFO Meldung
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
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103731"
---
# <a name="ttm_gettoolinfo-message"></a>TTM \_ gettoolinfo-Meldung

Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur. Beim Senden der Nachricht identifizieren die **HWND** -und **UID** -Member ein Tool, und das **CBSIZE** -Element muss die Größe der Struktur angeben. Wenn Sie diese Meldung verwenden, um den QuickInfo-Text abzurufen, stellen Sie sicher, dass der **lpszText** -Member der **toolinfo** -Struktur auf einen gültigen Puffer der adquate-Größe verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn das QuickInfo-Steuerelement das Tool enthält, empfängt die [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Strukturinformationen über das Tool.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Gettoolinfow** (Unicode) und **TTM \_ gettoolinfoa** (ANSI)<br/>           |



 

 





