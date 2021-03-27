---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen. Die Anzahl umfasst Dateien mit langen Dateinamen.
title: FM_GETSELCOUNTLFN Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994758"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="ace74-104">FM \_ getselzähltlfn-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ace74-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="ace74-105">Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ace74-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="ace74-106">Die Anzahl umfasst Dateien mit langen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="ace74-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="ace74-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace74-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace74-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ace74-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ace74-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ace74-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ace74-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ace74-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ace74-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ace74-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace74-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ace74-112">Return value</span></span>

<span data-ttu-id="ace74-113">Gibt die Anzahl der ausgewählten Dateien zurück.</span><span class="sxs-lookup"><span data-stu-id="ace74-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace74-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ace74-114">Remarks</span></span>

<span data-ttu-id="ace74-115">Diese Nachricht sollte nur von Erweiterungen verwendet werden, die lange Dateinamen unterstützen (z. b. Netzwerk abhängige Erweiterungen).</span><span class="sxs-lookup"><span data-stu-id="ace74-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace74-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ace74-116">Requirements</span></span>



| <span data-ttu-id="ace74-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ace74-117">Requirement</span></span> | <span data-ttu-id="ace74-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ace74-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ace74-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ace74-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ace74-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ace74-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ace74-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ace74-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ace74-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ace74-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ace74-123">Header</span><span class="sxs-lookup"><span data-stu-id="ace74-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace74-124"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace74-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace74-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ace74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace74-126">**FM \_ getfilesel**</span><span class="sxs-lookup"><span data-stu-id="ace74-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="ace74-127">**FM \_ getfilesellfn**</span><span class="sxs-lookup"><span data-stu-id="ace74-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="ace74-128">**FM \_ getselcount**</span><span class="sxs-lookup"><span data-stu-id="ace74-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




