---
description: Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf. Diese Meldung erweitert ABM-Abbild-Abbild \_ , indem Sie einen bestimmten Monitor zur Verwendung in mehreren Monitor Situationen angeben können.
title: ABM_SETAUTOHIDEBAREX Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996466"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="81407-104">ABM-Nachricht "- \_ Abmeldung"</span><span class="sxs-lookup"><span data-stu-id="81407-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="81407-105">Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf.</span><span class="sxs-lookup"><span data-stu-id="81407-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="81407-106">Diese Meldung erweitert [**ABM \_ -Abbild-Abbild**](abm-setautohidebar.md) , indem Sie einen bestimmten Monitor zur Verwendung in mehreren Monitor Situationen angeben können.</span><span class="sxs-lookup"><span data-stu-id="81407-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="81407-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="81407-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81407-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="81407-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="81407-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="81407-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="81407-110">Legen Sie den **LPARAM** -Member auf " **true** " fest, um die appbar **zu registrieren**</span><span class="sxs-lookup"><span data-stu-id="81407-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="81407-111">Sie müssen die Member **CBSIZE**, **HWND**, **uedge**, **RC** und **LPARAM** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="81407-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81407-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81407-112">Return value</span></span>

<span data-ttu-id="81407-113">Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler auftritt oder wenn für den angegebenen Edge für den angegebenen Monitor bereits eine appbar zum automatischen Ausblenden registriert ist.</span><span class="sxs-lookup"><span data-stu-id="81407-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="81407-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81407-114">Remarks</span></span>

<span data-ttu-id="81407-115">Das System lässt nur eine automatisch Ausblend Ende appbar für jeden Rand jedes Monitors zu.</span><span class="sxs-lookup"><span data-stu-id="81407-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="81407-116">Der Monitor wird durch das **RC** -Element bestimmt, und der Edge wird vom **uedge** -Member der [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur bestimmt.</span><span class="sxs-lookup"><span data-stu-id="81407-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="81407-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="81407-117">Requirements</span></span>



| <span data-ttu-id="81407-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81407-118">Requirement</span></span> | <span data-ttu-id="81407-119">Wert</span><span class="sxs-lookup"><span data-stu-id="81407-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81407-120">Header</span><span class="sxs-lookup"><span data-stu-id="81407-120">Header</span></span><br/> | <dl> <span data-ttu-id="81407-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="81407-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81407-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81407-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81407-123">**ABM \_ getautohidebar**</span><span class="sxs-lookup"><span data-stu-id="81407-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="81407-124">**ABM \_ getautohidebarex**</span><span class="sxs-lookup"><span data-stu-id="81407-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="81407-125">**ABM-Bild-auf \_**</span><span class="sxs-lookup"><span data-stu-id="81407-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 




