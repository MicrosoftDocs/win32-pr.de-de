---
title: WM_CAP_GET_USER_DATA Meldung (VFW. h)
description: Die WM- \_ Obergrenze \_ get \_ User \_ Data Ruft einen langen \_ ptr-Datenwert ab, der einem Aufzeichnungs Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des capgetuserdata-Makros senden.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518635"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="fe8bc-105">WM- \_ Cap- \_ Meldung " \_ Benutzer \_ Daten erhalten"</span><span class="sxs-lookup"><span data-stu-id="fe8bc-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="fe8bc-106">Die **WM- \_ Obergrenze \_ get \_ User \_ Data** Ruft einen **langen \_ ptr** -Datenwert ab, der einem Aufzeichnungs Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe8bc-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="fe8bc-107">Sie können diese Nachricht explizit oder mithilfe des [**capgetuserdata**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="fe8bc-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="fe8bc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe8bc-108">Return Value</span></span>

<span data-ttu-id="fe8bc-109">Gibt einen Wert zurück, der zuvor mit [**der \_ \_ \_ Benutzer \_ Daten**](wm-cap-set-user-data.md) Meldung für die WM-Abdeckung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe8bc-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8bc-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe8bc-110">Requirements</span></span>



| <span data-ttu-id="fe8bc-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe8bc-111">Requirement</span></span> | <span data-ttu-id="fe8bc-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fe8bc-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe8bc-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe8bc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8bc-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe8bc-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fe8bc-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe8bc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8bc-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe8bc-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe8bc-117">Header</span><span class="sxs-lookup"><span data-stu-id="fe8bc-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8bc-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe8bc-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe8bc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe8bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe8bc-120">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="fe8bc-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fe8bc-121">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="fe8bc-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





