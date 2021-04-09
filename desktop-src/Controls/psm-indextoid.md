---
title: PSM_INDEXTOID Meldung (prsht. h)
description: Nimmt den Index einer Eigenschaften Blattseite an und gibt die zugehörige Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ indextoid-Makro verwenden.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Windows-Steuerelemente für PSM_INDEXTOID Meldung
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040761"
---
# <a name="psm_indextoid-message"></a><span data-ttu-id="a2cc5-105">PSM- \_ indextoid-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a2cc5-105">PSM\_INDEXTOID message</span></span>

<span data-ttu-id="a2cc5-106">Nimmt den Index einer Eigenschaften Blattseite an und gibt die zugehörige Ressourcen-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-106">Takes the index of a property sheet page and returns its resource ID.</span></span> <span data-ttu-id="a2cc5-107">Sie können diese Nachricht explizit senden oder das [**propsheet- \_ indextoid**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-107">You can send this message explicitly or use the [**PropSheet\_IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2cc5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2cc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2cc5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2cc5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2cc5-110">Der null basierte Index der Seite.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="a2cc5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2cc5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2cc5-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2cc5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2cc5-113">Return value</span></span>

<span data-ttu-id="a2cc5-114">Gibt bei erfolgreicher Ausführung die Ressourcen-ID der Eigenschaften Blattseite zurück, die von *wParam* angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-114">Returns the resource ID of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="a2cc5-115">Andernfalls wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2cc5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2cc5-116">Requirements</span></span>



| <span data-ttu-id="a2cc5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2cc5-117">Requirement</span></span> | <span data-ttu-id="a2cc5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a2cc5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2cc5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2cc5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2cc5-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2cc5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a2cc5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2cc5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2cc5-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2cc5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a2cc5-123">Header</span><span class="sxs-lookup"><span data-stu-id="a2cc5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2cc5-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc5-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





