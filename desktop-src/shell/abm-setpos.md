---
description: Legt die Größe und Bildschirmposition einer appbar fest.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: ABM_SETPOS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525427"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="b2bae-103">ABM- \_ SetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b2bae-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="b2bae-104">Legt die Größe und Bildschirmposition einer appbar fest.</span><span class="sxs-lookup"><span data-stu-id="b2bae-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="b2bae-105">Die Meldung gibt eine Bildschirm Kante und das umgebende Rechteck für die appbar an.</span><span class="sxs-lookup"><span data-stu-id="b2bae-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="b2bae-106">Das System kann das umgebende Rechteck so anpassen, dass die APP-Leiste die Windows-Taskleiste oder andere appbars nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="b2bae-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="b2bae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2bae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2bae-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="b2bae-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="b2bae-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2bae-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="b2bae-110">Der **uedge** -Member gibt einen Bildschirmrand an, und das **RC** -Element enthält das umgebende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="b2bae-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="b2bae-111">Wenn die [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) -Funktion zurückgegeben wird, enthält **RC** das genehmigte umschließende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="b2bae-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="b2bae-112">Sie müssen die Member **CBSIZE**, **HWND**, **uedge** und **RC** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b2bae-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2bae-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2bae-113">Return value</span></span>

<span data-ttu-id="b2bae-114">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2bae-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2bae-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2bae-115">Remarks</span></span>

<span data-ttu-id="b2bae-116">Diese Meldung bewirkt, dass das System die [**ABN \_**](abn-poschanged.md) -Benachrichtigungs Meldung an alle appbars sendet.</span><span class="sxs-lookup"><span data-stu-id="b2bae-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bae-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b2bae-117">Requirements</span></span>



| <span data-ttu-id="b2bae-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2bae-118">Requirement</span></span> | <span data-ttu-id="b2bae-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b2bae-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2bae-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2bae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2bae-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2bae-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b2bae-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2bae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2bae-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2bae-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2bae-124">Header</span><span class="sxs-lookup"><span data-stu-id="b2bae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2bae-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2bae-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




