---
description: Benachrichtigt das System, wenn sich die Position einer appbar geändert hat. Eine appbar sollte diese Meldung als Antwort auf die WM- \_ windowposchge-Nachricht anrufen.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: ABM_WINDOWPOSCHANGED Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484395"
---
# <a name="abm_windowposchanged-message"></a><span data-ttu-id="fc9e6-104">ABM \_ windowposchge-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fc9e6-104">ABM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="fc9e6-105">Benachrichtigt das System, wenn sich die Position einer appbar geändert hat.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-105">Notifies the system when an appbar's position has changed.</span></span> <span data-ttu-id="fc9e6-106">Eine appbar sollte diese Meldung als Antwort auf die [**WM- \_ windowposchge**](/windows/desktop/winmsg/wm-windowposchanged) -Nachricht anrufen.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-106">An appbar should call this message in response to the [**WM\_WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) message.</span></span>


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="fc9e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc9e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc9e6-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="fc9e6-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9e6-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die die zu aktivierende appbar identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="fc9e6-110">Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc9e6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc9e6-111">Return value</span></span>

<span data-ttu-id="fc9e6-112">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc9e6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc9e6-113">Remarks</span></span>

<span data-ttu-id="fc9e6-114">Diese Meldung wird ignoriert, wenn der **HWND** -Member der Struktur, auf die von der *pabd* verwiesen wird, eine appbar zum automatischen Ausblenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc9e6-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fc9e6-115">Requirements</span></span>



| <span data-ttu-id="fc9e6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc9e6-116">Requirement</span></span> | <span data-ttu-id="fc9e6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fc9e6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9e6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc9e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc9e6-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc9e6-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fc9e6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc9e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc9e6-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc9e6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc9e6-122">Header</span><span class="sxs-lookup"><span data-stu-id="fc9e6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc9e6-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc9e6-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

