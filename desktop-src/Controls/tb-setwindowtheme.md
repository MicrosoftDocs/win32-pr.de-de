---
title: TB_SETWINDOWTHEME Meldung (kommstrg. h)
description: Legt den visuellen Stil eines Symbolleisten-Steuer Elements fest.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- Windows-Steuerelemente für TB_SETWINDOWTHEME Meldung
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106581"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="5f3fd-104">TB \_ SetWindowTheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="5f3fd-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="5f3fd-105">Legt den visuellen Stil eines Symbolleisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="5f3fd-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f3fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f3fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f3fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f3fd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f3fd-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5f3fd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f3fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f3fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f3fd-110">Ein Zeiger auf eine Unicode-Zeichenfolge, die den festzulegenden visuellen Symbolleisten Stil enthält.</span><span class="sxs-lookup"><span data-stu-id="5f3fd-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f3fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f3fd-111">Return value</span></span>

<span data-ttu-id="5f3fd-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f3fd-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f3fd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f3fd-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5f3fd-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="5f3fd-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5f3fd-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5f3fd-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="5f3fd-116">Das Senden dieser Nachricht entspricht dem Aufrufen von [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) auf der Symbolleiste und dem zugehörigen QuickInfo-Steuerelement (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="5f3fd-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f3fd-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f3fd-117">Requirements</span></span>



| <span data-ttu-id="5f3fd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f3fd-118">Requirement</span></span> | <span data-ttu-id="5f3fd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5f3fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f3fd-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f3fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5f3fd-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f3fd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f3fd-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f3fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5f3fd-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f3fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f3fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="5f3fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f3fd-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f3fd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





