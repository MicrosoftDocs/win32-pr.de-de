---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entlädt.
title: FMEVENT_UNLOAD (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843071"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="21785-103">FMEVENT \_ UNLOAD-Nachricht</span><span class="sxs-lookup"><span data-stu-id="21785-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="21785-104">Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entlädt.</span><span class="sxs-lookup"><span data-stu-id="21785-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="21785-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="21785-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21785-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21785-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="21785-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="21785-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="21785-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21785-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="21785-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="21785-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21785-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21785-110">Return value</span></span>

<span data-ttu-id="21785-111">Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn sie diese Meldung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="21785-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="21785-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21785-112">Remarks</span></span>

<span data-ttu-id="21785-113">Die *hwnd-* und **hMenu-Werte,** die mit den [**FMEVENT \_ LOAD-**](fmevent-load.md) und [**FMEVENT \_ INITMENU-Nachrichten**](fmevent-initmenu.md) übergeben werden, sind möglicherweise zum Zeitpunkt des Sendens dieser Nachricht ungültig.</span><span class="sxs-lookup"><span data-stu-id="21785-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="21785-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21785-114">Requirements</span></span>



| <span data-ttu-id="21785-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21785-115">Requirement</span></span> | <span data-ttu-id="21785-116">Wert</span><span class="sxs-lookup"><span data-stu-id="21785-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21785-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21785-117">Minimum supported client</span></span><br/> | <span data-ttu-id="21785-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21785-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="21785-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21785-119">Minimum supported server</span></span><br/> | <span data-ttu-id="21785-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21785-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="21785-121">Header</span><span class="sxs-lookup"><span data-stu-id="21785-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="21785-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="21785-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21785-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21785-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21785-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="21785-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




