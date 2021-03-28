---
description: Ruft die Zustände "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste ab.
title: ABM_GETSTATE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342869"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="f71be-103">ABM \_ GetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f71be-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="f71be-104">Ruft die Zustände "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste ab.</span><span class="sxs-lookup"><span data-stu-id="f71be-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="f71be-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f71be-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71be-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="f71be-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="f71be-107">Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f71be-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="f71be-108">Beim Senden dieser Nachricht muss das **CBSIZE** -Element angegeben werden. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f71be-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71be-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f71be-109">Return value</span></span>

<span data-ttu-id="f71be-110">Gibt 0 (null) zurück, wenn sich die Taskleiste weder im automatisch ausblenden-noch bei Always on-Top-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="f71be-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="f71be-111">Andernfalls ist der Rückgabewert eine oder beide der folgenden:</span><span class="sxs-lookup"><span data-stu-id="f71be-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f71be-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f71be-112">Return code</span></span></th>
<th><span data-ttu-id="f71be-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f71be-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="f71be-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f71be-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f71be-115">Die Taskleiste befindet sich im Status "Always on-Top".</span><span class="sxs-lookup"><span data-stu-id="f71be-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f71be-116">Ab Windows 7 wird ABS_ALWAYSONTOP nicht mehr zurückgegeben, da sich die Taskleiste immer in diesem Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="f71be-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="f71be-117">Der ältere Code sollte aktualisiert werden, damit das Fehlen dieses Werts ignoriert wird. angenommen, der Rückgabewert bedeutet, dass sich die Taskleiste nicht im Status "Always on-Top" befindet.</span><span class="sxs-lookup"><span data-stu-id="f71be-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f71be-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f71be-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f71be-119">Die Taskleiste befindet sich im Zustand "automatisch ausblenden".</span><span class="sxs-lookup"><span data-stu-id="f71be-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f71be-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f71be-120">Requirements</span></span>



| <span data-ttu-id="f71be-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f71be-121">Requirement</span></span> | <span data-ttu-id="f71be-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f71be-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f71be-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f71be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f71be-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f71be-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f71be-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f71be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f71be-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f71be-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f71be-127">Header</span><span class="sxs-lookup"><span data-stu-id="f71be-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71be-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71be-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




