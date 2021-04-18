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
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="029e5-104">TTM \_ gettoolinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="029e5-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="029e5-105">Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.</span><span class="sxs-lookup"><span data-stu-id="029e5-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="029e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="029e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="029e5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="029e5-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="029e5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="029e5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="029e5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="029e5-110">Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="029e5-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="029e5-111">Beim Senden der Nachricht identifizieren die **HWND** -und **UID** -Member ein Tool, und das **CBSIZE** -Element muss die Größe der Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="029e5-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="029e5-112">Wenn Sie diese Meldung verwenden, um den QuickInfo-Text abzurufen, stellen Sie sicher, dass der **lpszText** -Member der **toolinfo** -Struktur auf einen gültigen Puffer der adquate-Größe verweist.</span><span class="sxs-lookup"><span data-stu-id="029e5-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029e5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="029e5-113">Return value</span></span>

<span data-ttu-id="029e5-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="029e5-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="029e5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="029e5-115">Remarks</span></span>

<span data-ttu-id="029e5-116">Wenn das QuickInfo-Steuerelement das Tool enthält, empfängt die [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Strukturinformationen über das Tool.</span><span class="sxs-lookup"><span data-stu-id="029e5-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="029e5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="029e5-117">Examples</span></span>

<span data-ttu-id="029e5-118">Im folgenden Beispiel wird ein QuickInfo-Steuerelement neu positioniert.</span><span class="sxs-lookup"><span data-stu-id="029e5-118">The following example repositions a tooltip control.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="029e5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="029e5-119">Requirements</span></span>



| <span data-ttu-id="029e5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="029e5-120">Requirement</span></span> | <span data-ttu-id="029e5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="029e5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="029e5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="029e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="029e5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="029e5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="029e5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="029e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="029e5-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="029e5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="029e5-126">Header</span><span class="sxs-lookup"><span data-stu-id="029e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="029e5-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="029e5-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="029e5-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="029e5-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="029e5-129">**TTM \_ Gettoolinfow** (Unicode) und **TTM \_ gettoolinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="029e5-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





