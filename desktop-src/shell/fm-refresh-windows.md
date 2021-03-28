---
description: Wird von einer Datei-Manager-Erweiterung gesendet, die bewirkt, dass der Datei-Manager entweder das aktive Fenster oder alle zugehörigen Fenster neu zeichnet.
title: FM_REFRESH_WINDOWS Meldung (WF. h)
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
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214306"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="7fd63-103">FM \_ Windows-Aktualisierungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="7fd63-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="7fd63-104">Wird von einer Datei-Manager-Erweiterung gesendet, die bewirkt, dass der Datei-Manager entweder das aktive Fenster oder alle zugehörigen Fenster neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd63-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fd63-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fd63-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd63-106">*frepaint*</span><span class="sxs-lookup"><span data-stu-id="7fd63-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="7fd63-107">Ein Wert, der angibt, ob der Datei-Manager das aktive Fenster oder alle zugehörigen Fenster neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fd63-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="7fd63-108">Wenn dieser Parameter auf **true** gesetzt ist, zeichnet der Datei-Manager alle zugehörigen Fenster auf.</span><span class="sxs-lookup"><span data-stu-id="7fd63-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="7fd63-109">Andernfalls zeichnet der Datei-Manager nur das aktive Fenster.</span><span class="sxs-lookup"><span data-stu-id="7fd63-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="7fd63-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fd63-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7fd63-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7fd63-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd63-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fd63-112">Return value</span></span>

<span data-ttu-id="7fd63-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7fd63-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd63-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fd63-114">Remarks</span></span>

<span data-ttu-id="7fd63-115">Dateisystem Änderungen, die durch eine Erweiterung verursacht werden, werden automatisch vom Datei-Manager erkannt.</span><span class="sxs-lookup"><span data-stu-id="7fd63-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="7fd63-116">Eine Erweiterung sollte diese Nachricht nur in Situationen verwenden, in denen Laufwerk Verbindungen hergestellt oder abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="7fd63-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd63-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7fd63-117">Requirements</span></span>



| <span data-ttu-id="7fd63-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fd63-118">Requirement</span></span> | <span data-ttu-id="7fd63-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd63-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd63-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fd63-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd63-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fd63-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7fd63-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fd63-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd63-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fd63-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7fd63-124">Header</span><span class="sxs-lookup"><span data-stu-id="7fd63-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd63-125"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd63-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd63-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7fd63-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd63-127">**"F"**</span><span class="sxs-lookup"><span data-stu-id="7fd63-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




