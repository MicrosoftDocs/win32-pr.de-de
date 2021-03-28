---
description: Benachrichtigt eine appbar, wenn eine Vollbildanwendung geöffnet oder geschlossen wird. Diese Benachrichtigung wird in Form einer von der Anwendung definierten Nachricht gesendet, die von der neuen ABM-Nachricht festgelegt wird \_ .
title: ABN_FULLSCREENAPP Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128476"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="9d0d6-104">ABN \_ fullscreenapp-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9d0d6-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="9d0d6-105">Benachrichtigt eine appbar, wenn eine Vollbildanwendung geöffnet oder geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="9d0d6-106">Diese Benachrichtigung wird in Form einer von der Anwendung definierten Nachricht gesendet, die von der [**\_ neuen ABM**](abm-new.md) -Nachricht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="9d0d6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d0d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d0d6-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="9d0d6-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0d6-109">Ein Flag, das angibt, ob eine Vollbildanwendung geöffnet oder geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="9d0d6-110">Dieser Parameter ist " **true** ", wenn die Anwendung geöffnet wird, oder " **false** ", wenn Sie geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d0d6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d0d6-111">Return value</span></span>

<span data-ttu-id="9d0d6-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d0d6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d0d6-113">Remarks</span></span>

<span data-ttu-id="9d0d6-114">Wenn eine Vollbildanwendung geöffnet wird, muss eine appbar am Ende der z-Reihenfolge ablegen.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="9d0d6-115">Beim Schließen sollte die appbar die Position der z-Reihenfolge wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="9d0d6-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d0d6-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9d0d6-116">Requirements</span></span>



| <span data-ttu-id="9d0d6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d0d6-117">Requirement</span></span> | <span data-ttu-id="9d0d6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9d0d6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0d6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d0d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d0d6-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d0d6-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9d0d6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d0d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d0d6-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d0d6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d0d6-123">Header</span><span class="sxs-lookup"><span data-stu-id="9d0d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d0d6-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d0d6-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




