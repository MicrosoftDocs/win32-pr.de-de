---
description: Ruft das umgebende Rechteck der Windows-Taskleiste ab.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: ABM_GETTASKBARPOS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525430"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="86a36-103">ABM \_ gettaskbarpos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="86a36-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="86a36-104">Ruft das umgebende Rechteck der Windows-Taskleiste ab.</span><span class="sxs-lookup"><span data-stu-id="86a36-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="86a36-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="86a36-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a36-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="86a36-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="86a36-107">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, deren **RC** -Member das umschließende Rechteck (in Bildschirm Koordinaten) der Taskleiste empfängt.</span><span class="sxs-lookup"><span data-stu-id="86a36-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="86a36-108">Beim Senden dieser Nachricht muss **CBSIZE** angegeben werden. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="86a36-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a36-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86a36-109">Return value</span></span>

<span data-ttu-id="86a36-110">Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="86a36-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a36-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86a36-111">Remarks</span></span>

<span data-ttu-id="86a36-112">Beachten Sie, dass dies nur für die Taskleiste des Systems gilt.</span><span class="sxs-lookup"><span data-stu-id="86a36-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="86a36-113">Andere Objekte, insbesondere Symbolleisten, die mit Software von Drittanbietern bereitgestellt werden, können auch vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="86a36-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="86a36-114">Folglich sind einige der Bildschirmbereiche, die nicht von der Windows-Taskleiste abgedeckt werden, für den Benutzer möglicherweise nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="86a36-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="86a36-115">Verwenden Sie die [**getmonitorinfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) -Funktion, um den Bereich des Bildschirms abzurufen, der nicht von der Taskleiste und anderen APP-leisten für den Arbeitsbereich der Anwendung abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="86a36-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a36-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="86a36-116">Requirements</span></span>



| <span data-ttu-id="86a36-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86a36-117">Requirement</span></span> | <span data-ttu-id="86a36-118">Wert</span><span class="sxs-lookup"><span data-stu-id="86a36-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86a36-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86a36-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86a36-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86a36-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="86a36-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86a36-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86a36-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86a36-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86a36-123">Header</span><span class="sxs-lookup"><span data-stu-id="86a36-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="86a36-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86a36-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

