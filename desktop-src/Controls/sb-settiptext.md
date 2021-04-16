---
title: SB_SETTIPTEXT Meldung (kommstrg. h)
description: Legt den QuickInfo-Text für einen Teil in einer Statusleiste fest. Die Statusleiste muss mit dem SBT-Tooltips-Stil erstellt worden sein \_ , um Quick Infos zu aktivieren.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Windows-Steuerelemente für SB_SETTIPTEXT Meldung
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478096"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="805e1-105">SB-Setup \_ Textnachricht</span><span class="sxs-lookup"><span data-stu-id="805e1-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="805e1-106">Legt den QuickInfo-Text für einen Teil in einer Statusleiste fest.</span><span class="sxs-lookup"><span data-stu-id="805e1-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="805e1-107">Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt worden sein, um Quick Infos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="805e1-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="805e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="805e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="805e1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="805e1-110">NULL basierter Index des Teils, der den QuickInfo-Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="805e1-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="805e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="805e1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="805e1-112">Zeiger auf einen Zeichen Puffer, der den neuen QuickInfo-Text enthält.</span><span class="sxs-lookup"><span data-stu-id="805e1-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="805e1-113">Return value</span></span>

<span data-ttu-id="805e1-114">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="805e1-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="805e1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="805e1-115">Remarks</span></span>

<span data-ttu-id="805e1-116">Dieser QuickInfo-Text wird in zwei Situationen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="805e1-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="805e1-117">Wenn der entsprechende Bereich in der Statusleiste nur ein Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="805e1-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="805e1-118">Wenn der entsprechende Bereich in der Statusleiste Text enthält, der aufgrund der Größe des Bereichs abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="805e1-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="805e1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="805e1-119">Requirements</span></span>



| <span data-ttu-id="805e1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="805e1-120">Requirement</span></span> | <span data-ttu-id="805e1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="805e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="805e1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="805e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="805e1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="805e1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="805e1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="805e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="805e1-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="805e1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="805e1-126">Header</span><span class="sxs-lookup"><span data-stu-id="805e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="805e1-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="805e1-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="805e1-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="805e1-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="805e1-129">**SB \_ "Sttiptextw** (Unicode)" und " **SB \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="805e1-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 





