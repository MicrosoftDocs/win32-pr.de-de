---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster abzurufen (entweder im Verzeichnisfenster oder im Fenster Suchergebnisse).
title: FM_GETSELCOUNT (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842371"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="108c1-103">FM \_ GETSELCOUNT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="108c1-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="108c1-104">Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster abzurufen (entweder im Verzeichnisfenster oder im Fenster Suchergebnisse).</span><span class="sxs-lookup"><span data-stu-id="108c1-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="108c1-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="108c1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="108c1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="108c1-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="108c1-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="108c1-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="108c1-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="108c1-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="108c1-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="108c1-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="108c1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="108c1-110">Return value</span></span>

<span data-ttu-id="108c1-111">Gibt die Anzahl der ausgewählten Dateien zurück.</span><span class="sxs-lookup"><span data-stu-id="108c1-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="108c1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="108c1-112">Requirements</span></span>



| <span data-ttu-id="108c1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="108c1-113">Requirement</span></span> | <span data-ttu-id="108c1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="108c1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="108c1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="108c1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="108c1-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="108c1-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="108c1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="108c1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="108c1-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="108c1-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="108c1-119">Header</span><span class="sxs-lookup"><span data-stu-id="108c1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="108c1-120"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="108c1-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="108c1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="108c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108c1-122">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="108c1-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="108c1-123">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="108c1-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="108c1-124">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="108c1-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




