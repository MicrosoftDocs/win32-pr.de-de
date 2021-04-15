---
title: CCM_SETWINDOWTHEME Meldung (kommstrg. h)
description: Legt den visuellen Stil eines Steuer Elements fest.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- Windows-Steuerelemente für CCM_SETWINDOWTHEME Meldung
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477631"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="8d95a-104">CCM- \_ SetWindowTheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="8d95a-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="8d95a-105">Legt den visuellen Stil eines Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="8d95a-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d95a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d95a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d95a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d95a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d95a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8d95a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d95a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d95a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d95a-110">Ein Zeiger auf eine Unicode-Zeichenfolge, die den festzulegenden visuellen Stil des Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="8d95a-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d95a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d95a-111">Return value</span></span>

<span data-ttu-id="8d95a-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d95a-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d95a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d95a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8d95a-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="8d95a-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8d95a-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8d95a-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d95a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d95a-116">Requirements</span></span>



| <span data-ttu-id="8d95a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d95a-117">Requirement</span></span> | <span data-ttu-id="8d95a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8d95a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d95a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d95a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d95a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d95a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d95a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d95a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d95a-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d95a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d95a-123">Header</span><span class="sxs-lookup"><span data-stu-id="8d95a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d95a-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d95a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





