---
description: Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.
title: ABM_SETAUTOHIDEBAR Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977449"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="c8419-104">ABM- \_ Meldung "logdehidebar"</span><span class="sxs-lookup"><span data-stu-id="c8419-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="c8419-105">Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf.</span><span class="sxs-lookup"><span data-stu-id="c8419-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="c8419-106">Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="c8419-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="c8419-107">Verwenden Sie zum Registrieren oder Aufheben der Registrierung einer appbar für das automatische Ausblenden eines bestimmten Monitors [**ABM \_**](abm-setautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="c8419-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="c8419-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8419-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8419-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="c8419-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c8419-110">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8419-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="c8419-111">Legen Sie den **LPARAM** -Member auf " **true** " fest, um die appbar **zu registrieren**</span><span class="sxs-lookup"><span data-stu-id="c8419-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="c8419-112">Sie müssen die Member **CBSIZE**, **HWND**, **uedge** und **LPARAM** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c8419-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8419-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8419-113">Return value</span></span>

<span data-ttu-id="c8419-114">Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler auftritt oder wenn eine APP-Leiste zum automatischen Ausblenden für den angegebenen Edge bereits registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c8419-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8419-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8419-115">Remarks</span></span>

<span data-ttu-id="c8419-116">Das System lässt nur eine automatische Ausblend-appbar für jeden Bildschirmrand zu.</span><span class="sxs-lookup"><span data-stu-id="c8419-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="c8419-117">Dies wird bestimmt, wenn der Member **uedge** der [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c8419-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8419-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c8419-118">Requirements</span></span>



| <span data-ttu-id="c8419-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8419-119">Requirement</span></span> | <span data-ttu-id="c8419-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c8419-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8419-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8419-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8419-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8419-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c8419-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8419-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8419-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8419-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8419-125">Header</span><span class="sxs-lookup"><span data-stu-id="c8419-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8419-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8419-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8419-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8419-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8419-128">**ABM-Bild-auf \_**</span><span class="sxs-lookup"><span data-stu-id="c8419-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="c8419-129">**ABM \_ getautohidebarex**</span><span class="sxs-lookup"><span data-stu-id="c8419-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="c8419-130">**ABM \_ .**</span><span class="sxs-lookup"><span data-stu-id="c8419-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




