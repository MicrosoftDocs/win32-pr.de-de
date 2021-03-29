---
description: Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.
title: DFM_WM_INITMENUPOPUP Meldung (shlobj. h)
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
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128452"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="ee611-104">DFM- \_ WM- \_ initmenupopup-Meldung</span><span class="sxs-lookup"><span data-stu-id="ee611-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="ee611-105">Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee611-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="ee611-106">Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ee611-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="ee611-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee611-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee611-108">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee611-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee611-109">Ein Handle für das Dropdown Menü oder Untermenü.</span><span class="sxs-lookup"><span data-stu-id="ee611-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="ee611-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee611-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee611-111">Das nieder wertige Wort gibt die null basierte relative Position des Menü Elements an, das das Dropdown Menü oder Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="ee611-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="ee611-112">Das höchst wertige Wort gibt an, ob das Dropdown Menü das Fenstermenü ist.</span><span class="sxs-lookup"><span data-stu-id="ee611-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="ee611-113">Wenn das Menü das Menü "Fenster" ist, ist dieser Parameter " **true**". Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="ee611-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee611-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee611-114">Return value</span></span>

<span data-ttu-id="ee611-115">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ee611-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee611-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ee611-116">Requirements</span></span>



| <span data-ttu-id="ee611-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee611-117">Requirement</span></span> | <span data-ttu-id="ee611-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ee611-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee611-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee611-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee611-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee611-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ee611-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee611-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee611-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee611-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ee611-123">Header</span><span class="sxs-lookup"><span data-stu-id="ee611-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee611-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee611-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




