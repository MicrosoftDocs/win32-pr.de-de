---
description: Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.
title: ABM_GETAUTOHIDEBAR Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128480"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="e71fd-104">ABM \_ getautohidebar-Meldung</span><span class="sxs-lookup"><span data-stu-id="e71fd-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="e71fd-105">Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e71fd-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="e71fd-106">Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="e71fd-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="e71fd-107">Verwenden Sie zum Abfragen eines automatischen Ausblenden der appbar eines bestimmten Monitors [**ABM \_ getautohidebarex**](abm-getautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="e71fd-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="e71fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e71fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71fd-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="e71fd-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="e71fd-110">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die den Bildschirmrand angibt.</span><span class="sxs-lookup"><span data-stu-id="e71fd-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="e71fd-111">Sie müssen die Member **CBSIZE** und **uedge** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e71fd-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71fd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e71fd-112">Return value</span></span>

<span data-ttu-id="e71fd-113">Gibt das Handle für die automatisch Ausblend-appbar zurück.</span><span class="sxs-lookup"><span data-stu-id="e71fd-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="e71fd-114">Der Rückgabewert ist **null** , wenn ein Fehler auftritt oder wenn dem angegebenen Edge keine Automatisches Ausblenden-appbar zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e71fd-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71fd-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e71fd-115">Requirements</span></span>



| <span data-ttu-id="e71fd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e71fd-116">Requirement</span></span> | <span data-ttu-id="e71fd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e71fd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e71fd-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e71fd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e71fd-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e71fd-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e71fd-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e71fd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e71fd-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e71fd-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e71fd-122">Header</span><span class="sxs-lookup"><span data-stu-id="e71fd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e71fd-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e71fd-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e71fd-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e71fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71fd-125">**ABM-Bild-auf \_**</span><span class="sxs-lookup"><span data-stu-id="e71fd-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="e71fd-126">**ABM \_ getautohidebarex**</span><span class="sxs-lookup"><span data-stu-id="e71fd-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="e71fd-127">**ABM \_ .**</span><span class="sxs-lookup"><span data-stu-id="e71fd-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




