---
title: CBEM_SETWINDOWTHEME Meldung (kommstrg. h)
description: Legt den visuellen Stil eines ComboBoxEx-Steuer Elements fest.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- Windows-Steuerelemente für CBEM_SETWINDOWTHEME Meldung
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cda1e5c46bb6216c413737c44b5785ac26925f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342445"
---
# <a name="cbem_setwindowtheme-message"></a><span data-ttu-id="6f5c4-104">CBEM- \_ SetWindowTheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="6f5c4-104">CBEM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="6f5c4-105">Legt den visuellen Stil eines ComboBoxEx-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="6f5c4-105">Sets the visual style of a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f5c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f5c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f5c4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f5c4-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6f5c4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f5c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f5c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f5c4-110">Ein Zeiger auf eine Unicode-Zeichenfolge, die den festzulegenden visuellen Stil des Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="6f5c4-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5c4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f5c4-111">Return value</span></span>

<span data-ttu-id="6f5c4-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f5c4-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f5c4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f5c4-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f5c4-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, in dem die Comclt32-Version 6,0 angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f5c4-114">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="6f5c4-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f5c4-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f5c4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f5c4-116">Requirements</span></span>



| <span data-ttu-id="6f5c4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f5c4-117">Requirement</span></span> | <span data-ttu-id="6f5c4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6f5c4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f5c4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5c4-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f5c4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f5c4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f5c4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5c4-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f5c4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f5c4-123">Header</span><span class="sxs-lookup"><span data-stu-id="6f5c4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f5c4-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





