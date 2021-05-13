---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster abzurufen (entweder im Verzeichnisfenster oder im Fenster Suchergebnisse). Die Anzahl umfasst Dateien mit langen Dateinamen.
title: FM_GETSELCOUNTLFN (Wfext.h)
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
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841341"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="4149f-104">FM \_ GETSELCOUNTLFN-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4149f-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="4149f-105">Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster abzurufen (entweder im Verzeichnisfenster oder im Fenster Suchergebnisse).</span><span class="sxs-lookup"><span data-stu-id="4149f-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="4149f-106">Die Anzahl umfasst Dateien mit langen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="4149f-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="4149f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4149f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4149f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4149f-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4149f-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4149f-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4149f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4149f-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4149f-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4149f-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4149f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4149f-112">Return value</span></span>

<span data-ttu-id="4149f-113">Gibt die Anzahl der ausgewählten Dateien zurück.</span><span class="sxs-lookup"><span data-stu-id="4149f-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="4149f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4149f-114">Remarks</span></span>

<span data-ttu-id="4149f-115">Nur Erweiterungen, die lange Dateinamen unterstützen (z. B. netzwerkspezifische Erweiterungen), sollten diese Meldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4149f-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4149f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4149f-116">Requirements</span></span>



| <span data-ttu-id="4149f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4149f-117">Requirement</span></span> | <span data-ttu-id="4149f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4149f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4149f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4149f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4149f-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4149f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4149f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4149f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4149f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4149f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4149f-123">Header</span><span class="sxs-lookup"><span data-stu-id="4149f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4149f-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="4149f-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4149f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4149f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4149f-126">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="4149f-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="4149f-127">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="4149f-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="4149f-128">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="4149f-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




