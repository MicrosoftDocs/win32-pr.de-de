---
description: 'DFM_WM_INITMENUPOPUP: Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.'
title: DFM_WM_INITMENUPOPUP (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096998"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="c9c21-104">DFM \_ WM \_ INITMENUPOPUP-Meldung</span><span class="sxs-lookup"><span data-stu-id="c9c21-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="c9c21-105">Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="c9c21-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="c9c21-106">Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c9c21-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="c9c21-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9c21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c21-108">*wParam* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9c21-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c21-109">Ein Handle für das Dropdownmenü oder Untermenü.</span><span class="sxs-lookup"><span data-stu-id="c9c21-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="c9c21-110">*lParam* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9c21-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c21-111">Das Wort in niedriger Reihenfolge gibt die nullbasierte relative Position des Menüelements an, das das Dropdownmenü oder Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="c9c21-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="c9c21-112">Das obere Wort gibt an, ob das Dropdownmenü das Fenstermenü ist.</span><span class="sxs-lookup"><span data-stu-id="c9c21-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="c9c21-113">Wenn das Menü das Fenstermenü ist, ist dieser Parameter **TRUE;** Andernfalls ist dies **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="c9c21-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c21-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9c21-114">Return value</span></span>

<span data-ttu-id="c9c21-115">Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9c21-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c21-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9c21-116">Requirements</span></span>



| <span data-ttu-id="c9c21-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9c21-117">Requirement</span></span> | <span data-ttu-id="c9c21-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c9c21-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c21-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9c21-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c21-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9c21-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c9c21-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9c21-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9c21-122">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9c21-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9c21-123">Header</span><span class="sxs-lookup"><span data-stu-id="c9c21-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9c21-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c21-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




