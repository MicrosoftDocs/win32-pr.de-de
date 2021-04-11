---
title: SB_GETBORDERS Meldung (kommstrg. h)
description: Ruft die aktuelle Breite der horizontalen und vertikalen Rahmen eines Status Fensters ab.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Windows-Steuerelemente für SB_GETBORDERS Meldung
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105081"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="51883-104">SB \_ getborders-Nachricht</span><span class="sxs-lookup"><span data-stu-id="51883-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="51883-105">Ruft die aktuelle Breite der horizontalen und vertikalen Rahmen eines Status Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="51883-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="51883-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51883-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51883-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51883-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="51883-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="51883-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="51883-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51883-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51883-110">Zeiger auf ein ganzzahliges Array, das über drei Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="51883-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="51883-111">Das erste Element empfängt die Breite des horizontalen Rahmens, das zweite empfängt die Breite des vertikalen Rahmens, und das dritte empfängt die Breite des Rahmens zwischen Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="51883-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51883-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51883-112">Return value</span></span>

<span data-ttu-id="51883-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="51883-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="51883-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51883-114">Remarks</span></span>

<span data-ttu-id="51883-115">Die Rahmen bestimmen den Abstand zwischen dem äußeren Rand des Fensters und den Rechtecke innerhalb des Fensters, die Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="51883-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="51883-116">Die Rahmen bestimmen auch den Abstand zwischen Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="51883-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="51883-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51883-117">Requirements</span></span>



| <span data-ttu-id="51883-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51883-118">Requirement</span></span> | <span data-ttu-id="51883-119">Wert</span><span class="sxs-lookup"><span data-stu-id="51883-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51883-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51883-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51883-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51883-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51883-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51883-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51883-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51883-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51883-124">Header</span><span class="sxs-lookup"><span data-stu-id="51883-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51883-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="51883-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





