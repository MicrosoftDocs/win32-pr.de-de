---
description: Benachrichtigt das System, dass eine appbar aktiviert wurde. Eine appbar sollte diese Meldung als Antwort auf die WM- \_ Aktivierungs Nachricht anrufen.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128481"
---
# <a name="abm_activate-message"></a><span data-ttu-id="4d34b-104">ABM- \_ Aktivierungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="4d34b-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="4d34b-105">Benachrichtigt das System, dass eine appbar aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="4d34b-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="4d34b-106">Eine appbar sollte diese Meldung als Antwort auf die [**WM- \_ Aktivierungs**](/windows/desktop/inputdev/wm-activate) Nachricht anrufen.</span><span class="sxs-lookup"><span data-stu-id="4d34b-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="4d34b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d34b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d34b-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="4d34b-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="4d34b-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die die zu aktivierende appbar identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4d34b-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="4d34b-110">Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4d34b-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d34b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d34b-111">Return value</span></span>

<span data-ttu-id="4d34b-112">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="4d34b-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d34b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d34b-113">Remarks</span></span>

<span data-ttu-id="4d34b-114">Diese Meldung wird ignoriert, wenn der **HWND** -Member der Struktur, auf die von der *pabd* verwiesen wird, eine appbar zum automatischen Ausblenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4d34b-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="4d34b-115">Das System legt automatisch die z-Reihenfolge für automatische Ausblenden von appbars fest.</span><span class="sxs-lookup"><span data-stu-id="4d34b-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d34b-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4d34b-116">Requirements</span></span>



| <span data-ttu-id="4d34b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d34b-117">Requirement</span></span> | <span data-ttu-id="4d34b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4d34b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d34b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d34b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d34b-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d34b-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4d34b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d34b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d34b-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d34b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d34b-123">Header</span><span class="sxs-lookup"><span data-stu-id="4d34b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d34b-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d34b-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

