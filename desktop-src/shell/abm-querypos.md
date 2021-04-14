---
description: Fordert eine Größe und Bildschirmposition für eine appbar an.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: ABM_QUERYPOS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342868"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="96f87-103">ABM- \_ querypos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="96f87-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="96f87-104">Fordert eine Größe und Bildschirmposition für eine appbar an.</span><span class="sxs-lookup"><span data-stu-id="96f87-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="96f87-105">Wenn die Anforderung erfolgt, schlägt die Meldung einen Bildschirmrand und ein Begrenzungs Rechteck für die appbar vor.</span><span class="sxs-lookup"><span data-stu-id="96f87-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="96f87-106">Das System passt das umgebende Rechteck so an, dass die APP-Leiste die Windows-Taskleiste oder andere appbars nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="96f87-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="96f87-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="96f87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96f87-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="96f87-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="96f87-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="96f87-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="96f87-110">Der **uedge** -Member gibt einen Bildschirmrand an, und das **RC** -Element enthält das vorgeschlagene umgebende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="96f87-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="96f87-111">Wenn die [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) -Funktion zurückgegeben wird, enthält **RC** das genehmigte umschließende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="96f87-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="96f87-112">Sie müssen die Member **CBSIZE**, **HWND**, **uedge** und **RC** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="96f87-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96f87-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96f87-113">Return value</span></span>

<span data-ttu-id="96f87-114">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="96f87-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96f87-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96f87-115">Remarks</span></span>

<span data-ttu-id="96f87-116">Eine appbar sollte diese Nachricht vor dem Senden der [**ABM- \_ SetPos**](abm-setpos.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="96f87-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="96f87-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="96f87-117">Requirements</span></span>



| <span data-ttu-id="96f87-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96f87-118">Requirement</span></span> | <span data-ttu-id="96f87-119">Wert</span><span class="sxs-lookup"><span data-stu-id="96f87-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96f87-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96f87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96f87-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96f87-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96f87-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96f87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96f87-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96f87-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96f87-124">Header</span><span class="sxs-lookup"><span data-stu-id="96f87-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f87-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f87-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




