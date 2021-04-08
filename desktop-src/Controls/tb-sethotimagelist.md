---
title: TB_SETHOTIMAGELIST Meldung (kommstrg. h)
description: Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Hot-Schaltflächen verwendet.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Windows-Steuerelemente für TB_SETHOTIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956876"
---
# <a name="tb_sethotimagelist-message"></a><span data-ttu-id="ac01d-104">TB \_ SetHotImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="ac01d-104">TB\_SETHOTIMAGELIST message</span></span>

<span data-ttu-id="ac01d-105">Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen von Hot-Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac01d-105">Sets the image list that the toolbar control will use to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac01d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac01d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac01d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac01d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ac01d-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ac01d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ac01d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac01d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac01d-110">Handle für die Bildliste, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ac01d-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac01d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac01d-111">Return value</span></span>

<span data-ttu-id="ac01d-112">Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Hot-Schaltflächen verwendet wurde, oder **null** , wenn zuvor keine Bildliste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ac01d-112">Returns the handle to the image list previously used to display hot buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac01d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac01d-113">Remarks</span></span>

<span data-ttu-id="ac01d-114">Eine Schaltfläche ist heiß, wenn sich der Cursor darüber befindet.</span><span class="sxs-lookup"><span data-stu-id="ac01d-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="ac01d-115">Für Symbolleisten-Steuerelemente muss der [**tbstyle- \_ Flat**](toolbar-control-and-button-styles.md) -oder [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil für heiße Elemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac01d-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac01d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac01d-116">Requirements</span></span>



| <span data-ttu-id="ac01d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac01d-117">Requirement</span></span> | <span data-ttu-id="ac01d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ac01d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac01d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac01d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac01d-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac01d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac01d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac01d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac01d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac01d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac01d-123">Header</span><span class="sxs-lookup"><span data-stu-id="ac01d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac01d-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac01d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





