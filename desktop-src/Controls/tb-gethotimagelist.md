---
title: TB_GETHOTIMAGELIST Meldung (kommstrg. h)
description: Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Windows-Steuerelemente für TB_GETHOTIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104030"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="4e1cb-104">TB- \_ gethotimagelist-Meldung</span><span class="sxs-lookup"><span data-stu-id="4e1cb-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="4e1cb-105">Ruft die Bildliste ab, die ein ToolBar-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4e1cb-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e1cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e1cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e1cb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4e1cb-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4e1cb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4e1cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e1cb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e1cb-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4e1cb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1cb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e1cb-111">Return value</span></span>

<span data-ttu-id="4e1cb-112">Gibt das Handle für die Bildliste zurück, die das-Steuerelement verwendet, um Hot-Schaltflächen anzuzeigen, oder **null** , wenn keine Liste mit den heißen Bildern festgelegt</span><span class="sxs-lookup"><span data-stu-id="4e1cb-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1cb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e1cb-113">Remarks</span></span>

<span data-ttu-id="4e1cb-114">Eine Schaltfläche ist heiß, wenn sich der Cursor darüber befindet.</span><span class="sxs-lookup"><span data-stu-id="4e1cb-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="4e1cb-115">Für Symbolleisten-Steuerelemente muss der [**tbstyle- \_ Flat**](toolbar-control-and-button-styles.md) -oder [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil für heiße Elemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e1cb-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1cb-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e1cb-116">Requirements</span></span>



| <span data-ttu-id="4e1cb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e1cb-117">Requirement</span></span> | <span data-ttu-id="4e1cb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4e1cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1cb-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e1cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1cb-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e1cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e1cb-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e1cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1cb-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e1cb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e1cb-123">Header</span><span class="sxs-lookup"><span data-stu-id="4e1cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e1cb-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1cb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





