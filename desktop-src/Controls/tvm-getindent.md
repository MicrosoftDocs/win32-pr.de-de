---
title: TVM_GETINDENT Meldung (kommstrg. h)
description: Ruft den Betrag in Pixel ab, in dem untergeordnete Elemente relativ zu ihren übergeordneten Elementen eingezogen werden. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "GetIndent" senden.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- Windows-Steuerelemente für TVM_GETINDENT Meldung
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859233"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="6ee5b-105">TVM- \_ GetIndent-Meldung</span><span class="sxs-lookup"><span data-stu-id="6ee5b-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="6ee5b-106">Ruft den Betrag in Pixel ab, in dem untergeordnete Elemente relativ zu ihren übergeordneten Elementen eingezogen werden.</span><span class="sxs-lookup"><span data-stu-id="6ee5b-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="6ee5b-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) " senden.</span><span class="sxs-lookup"><span data-stu-id="6ee5b-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ee5b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ee5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ee5b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ee5b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6ee5b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6ee5b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ee5b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ee5b-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6ee5b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee5b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ee5b-113">Return value</span></span>

<span data-ttu-id="6ee5b-114">Gibt die Einzugs Menge zurück.</span><span class="sxs-lookup"><span data-stu-id="6ee5b-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee5b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ee5b-115">Requirements</span></span>



| <span data-ttu-id="6ee5b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ee5b-116">Requirement</span></span> | <span data-ttu-id="6ee5b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6ee5b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee5b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ee5b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee5b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ee5b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ee5b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ee5b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee5b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ee5b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ee5b-122">Header</span><span class="sxs-lookup"><span data-stu-id="6ee5b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee5b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee5b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





