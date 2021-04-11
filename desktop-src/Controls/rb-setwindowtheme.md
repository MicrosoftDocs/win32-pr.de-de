---
title: RB_SETWINDOWTHEME Meldung (kommstrg. h)
description: Legt den visuellen Stil eines Grund leisten-Steuer Elements fest.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- Windows-Steuerelemente für RB_SETWINDOWTHEME Meldung
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104780"
---
# <a name="rb_setwindowtheme-message"></a><span data-ttu-id="c5d61-104">RB \_ SetWindowTheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="c5d61-104">RB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="c5d61-105">Legt den visuellen Stil eines Grund leisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="c5d61-105">Sets the visual style of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5d61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5d61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d61-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5d61-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5d61-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c5d61-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c5d61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5d61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5d61-110">Ein Zeiger auf eine Unicode-Zeichenfolge, die den festzulegenden visuellen Stil der Grund Leiste enthält.</span><span class="sxs-lookup"><span data-stu-id="c5d61-110">Pointer to a Unicode string that contains the rebar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d61-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5d61-111">Return value</span></span>

<span data-ttu-id="c5d61-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5d61-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5d61-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5d61-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c5d61-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="c5d61-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c5d61-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c5d61-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5d61-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5d61-116">Requirements</span></span>



| <span data-ttu-id="c5d61-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5d61-117">Requirement</span></span> | <span data-ttu-id="c5d61-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d61-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d61-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5d61-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d61-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5d61-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5d61-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5d61-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d61-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5d61-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5d61-123">Header</span><span class="sxs-lookup"><span data-stu-id="c5d61-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d61-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d61-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





