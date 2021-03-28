---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen.
title: FM_GETSELCOUNT Meldung (WF. h)
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
ms.openlocfilehash: aac7d08de3785bb02c31dabc1ef7a25fea0d5b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993702"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="3149b-103">FM \_ getselcount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3149b-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="3149b-104">Wird von einer Datei-Manager-Erweiterung gesendet, um die Anzahl der ausgewählten Dateien im aktiven Datei-Manager-Fenster (entweder im Verzeichnis Fenster oder im Fenster "Suchergebnisse") abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3149b-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="3149b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3149b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3149b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3149b-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3149b-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3149b-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3149b-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3149b-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3149b-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3149b-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3149b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3149b-110">Return value</span></span>

<span data-ttu-id="3149b-111">Gibt die Anzahl der ausgewählten Dateien zurück.</span><span class="sxs-lookup"><span data-stu-id="3149b-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="3149b-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3149b-112">Requirements</span></span>



| <span data-ttu-id="3149b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3149b-113">Requirement</span></span> | <span data-ttu-id="3149b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3149b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3149b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3149b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3149b-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3149b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3149b-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3149b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3149b-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3149b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3149b-119">Header</span><span class="sxs-lookup"><span data-stu-id="3149b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3149b-120"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="3149b-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3149b-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3149b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3149b-122">**FM \_ getfilesel**</span><span class="sxs-lookup"><span data-stu-id="3149b-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="3149b-123">**FM \_ getfilesellfn**</span><span class="sxs-lookup"><span data-stu-id="3149b-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="3149b-124">**FM \_ getselzähltlfn**</span><span class="sxs-lookup"><span data-stu-id="3149b-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




