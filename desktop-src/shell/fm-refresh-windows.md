---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um zu bewirken, dass der Datei-Manager entweder das aktive Fenster oder alle Fenster neu malt.
title: FM_REFRESH_WINDOWS Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842351"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="fa9e4-103">FM \_ REFRESH \_ WINDOWS-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fa9e4-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="fa9e4-104">Wird von einer Datei-Manager-Erweiterung gesendet, damit der Datei-Manager entweder das aktive Fenster oder alle Fenster neu malt.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa9e4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa9e4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9e4-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="fa9e4-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9e4-107">Ein -Wert, der angibt, ob der Datei-Manager das aktive Fenster oder alle Fenster neu malt.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="fa9e4-108">Wenn dieser Parameter **TRUE** ist, zeichnet der Datei-Manager alle Fenster neu.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="fa9e4-109">Andernfalls bemalt der Datei-Manager nur das aktive Fenster neu.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="fa9e4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa9e4-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa9e4-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa9e4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa9e4-112">Return value</span></span>

<span data-ttu-id="fa9e4-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa9e4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa9e4-114">Remarks</span></span>

<span data-ttu-id="fa9e4-115">Dateisystemänderungen, die durch eine Erweiterung verursacht werden, werden automatisch vom Datei-Manager erkannt.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="fa9e4-116">Eine Erweiterung sollte diese Meldung nur in Situationen verwenden, in denen Laufwerkverbindungen hergestellt oder abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="fa9e4-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa9e4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa9e4-117">Requirements</span></span>



| <span data-ttu-id="fa9e4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa9e4-118">Requirement</span></span> | <span data-ttu-id="fa9e4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fa9e4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9e4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa9e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa9e4-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa9e4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fa9e4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa9e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa9e4-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa9e4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fa9e4-124">Header</span><span class="sxs-lookup"><span data-stu-id="fa9e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa9e4-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="fa9e4-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa9e4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa9e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa9e4-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="fa9e4-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




