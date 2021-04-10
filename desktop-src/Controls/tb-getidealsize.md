---
title: TB_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die ideale Größe der Symbolleiste ab.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Windows-Steuerelemente für TB_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040234"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="e9778-104">TB- \_ getidealsize-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e9778-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="e9778-105">Ruft die ideale Größe der Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="e9778-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9778-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9778-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9778-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e9778-108">Ein **boolescher** Wert, der angibt, ob die ideale Höhe oder Breite der Symbolleiste abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e9778-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="e9778-109">Verwenden Sie " **true** ", um die ideale Höhe abzurufen, " **false** ", um die ideale Breite abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9778-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="e9778-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9778-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9778-111">Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die Höhe oder Breite empfängt, bei der alle Schaltflächen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e9778-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="e9778-112">Wenn *wParam* den Wert **true** hat, ist nur der **CY** -Member (Height) gültig.</span><span class="sxs-lookup"><span data-stu-id="e9778-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="e9778-113">Wenn *wParam* den Wert **false** hat, ist nur der **CX** -Member (Width) gültig.</span><span class="sxs-lookup"><span data-stu-id="e9778-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9778-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9778-114">Return value</span></span>

<span data-ttu-id="e9778-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e9778-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9778-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9778-116">Requirements</span></span>



| <span data-ttu-id="e9778-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9778-117">Requirement</span></span> | <span data-ttu-id="e9778-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e9778-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9778-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9778-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e9778-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9778-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9778-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9778-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e9778-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9778-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9778-123">Header</span><span class="sxs-lookup"><span data-stu-id="e9778-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9778-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9778-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

