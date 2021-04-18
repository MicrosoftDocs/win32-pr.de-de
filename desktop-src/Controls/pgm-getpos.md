---
title: PGM_GETPOS Meldung (kommstrg. h)
description: Ruft die aktuelle Bild Lauf Position des Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das Pager- \_ GetPos-Makro verwenden.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Windows-Steuerelemente für PGM_GETPOS Meldung
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344485"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="f9234-105">PGM- \_ GetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f9234-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="f9234-106">Ruft die aktuelle Bild Lauf Position des Pager-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="f9234-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="f9234-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9234-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9234-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9234-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9234-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9234-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f9234-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f9234-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f9234-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9234-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f9234-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f9234-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9234-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9234-113">Return value</span></span>

<span data-ttu-id="f9234-114">Gibt einen int-Wert zurück, der die aktuelle Bild Lauf Position in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="f9234-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9234-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9234-115">Requirements</span></span>



| <span data-ttu-id="f9234-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9234-116">Requirement</span></span> | <span data-ttu-id="f9234-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f9234-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9234-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9234-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9234-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9234-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9234-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9234-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9234-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9234-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9234-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9234-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9234-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9234-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





