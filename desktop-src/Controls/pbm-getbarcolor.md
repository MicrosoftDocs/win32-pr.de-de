---
title: PBM_GETBARCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe der Statusanzeige ab.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- Windows-Steuerelemente für PBM_GETBARCOLOR Meldung
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104799"
---
# <a name="pbm_getbarcolor-message"></a><span data-ttu-id="103d2-104">PBM \_ getbarcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="103d2-104">PBM\_GETBARCOLOR message</span></span>

<span data-ttu-id="103d2-105">Ruft die Farbe der Statusanzeige ab.</span><span class="sxs-lookup"><span data-stu-id="103d2-105">Gets the color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="103d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="103d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="103d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="103d2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="103d2-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="103d2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="103d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="103d2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="103d2-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="103d2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="103d2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="103d2-111">Return value</span></span>

<span data-ttu-id="103d2-112">Gibt die Farbe der Statusanzeige zurück.</span><span class="sxs-lookup"><span data-stu-id="103d2-112">Returns the color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="103d2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="103d2-113">Remarks</span></span>

<span data-ttu-id="103d2-114">Dies ist die Farbe, die von der [**PBM- \_ setbarcolor**](pbm-setbarcolor.md) -Nachricht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="103d2-114">This is the color set by the [**PBM\_SETBARCOLOR**](pbm-setbarcolor.md) message.</span></span> <span data-ttu-id="103d2-115">Der Standardwert ist CLR \_ Default, der in "kommctrl. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="103d2-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="103d2-116">Diese Funktion wirkt sich nur auf den klassischen Modus aus, nicht auf einen visuellen Stil.</span><span class="sxs-lookup"><span data-stu-id="103d2-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="103d2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="103d2-117">Requirements</span></span>



| <span data-ttu-id="103d2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="103d2-118">Requirement</span></span> | <span data-ttu-id="103d2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="103d2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="103d2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="103d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="103d2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="103d2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="103d2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="103d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="103d2-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="103d2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="103d2-124">Header</span><span class="sxs-lookup"><span data-stu-id="103d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="103d2-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="103d2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





