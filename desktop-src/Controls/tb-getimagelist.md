---
title: TB_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Schaltflächen im Standardzustand anzuzeigen. Ein Symbolleisten-Steuerelement verwendet diese Bildliste zum Anzeigen von Schaltflächen, wenn diese nicht heiß oder deaktiviert sind.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- Windows-Steuerelemente für TB_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740273"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="811d0-105">TB \_ GetImageList-Nachricht</span><span class="sxs-lookup"><span data-stu-id="811d0-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="811d0-106">Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Schaltflächen im Standardzustand anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="811d0-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="811d0-107">Ein Symbolleisten-Steuerelement verwendet diese Bildliste zum Anzeigen von Schaltflächen, wenn diese nicht heiß oder deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="811d0-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="811d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="811d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="811d0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="811d0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="811d0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="811d0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="811d0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="811d0-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="811d0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811d0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="811d0-113">Return value</span></span>

<span data-ttu-id="811d0-114">Gibt das Handle für die Bildliste zurück, oder **null** , wenn keine Bildliste festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="811d0-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="811d0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="811d0-115">Requirements</span></span>



| <span data-ttu-id="811d0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="811d0-116">Requirement</span></span> | <span data-ttu-id="811d0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="811d0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="811d0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="811d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="811d0-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="811d0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="811d0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="811d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="811d0-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="811d0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="811d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="811d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="811d0-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="811d0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





