---
title: PSM_SETNEXTTEXT Meldung (prsht. h)
description: Legt den Text der Schaltfläche weiter in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setnexttext senden.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- Windows-Steuerelemente für PSM_SETNEXTTEXT Meldung
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740096"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="ea185-105">PSM- \_ setnexttext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ea185-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="ea185-106">Legt den Text der Schaltfläche **weiter** in einem Assistenten fest.</span><span class="sxs-lookup"><span data-stu-id="ea185-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="ea185-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setnexttext**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) senden.</span><span class="sxs-lookup"><span data-stu-id="ea185-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea185-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea185-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea185-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea185-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ea185-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea185-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea185-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea185-112">Zeiger auf einen Puffer, der den Text enthält.</span><span class="sxs-lookup"><span data-stu-id="ea185-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea185-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea185-113">Return value</span></span>

<span data-ttu-id="ea185-114">Kein aussagekräftiger Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ea185-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea185-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea185-115">Requirements</span></span>



| <span data-ttu-id="ea185-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea185-116">Requirement</span></span> | <span data-ttu-id="ea185-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ea185-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea185-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea185-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea185-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea185-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ea185-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea185-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea185-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea185-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea185-122">Header</span><span class="sxs-lookup"><span data-stu-id="ea185-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea185-123"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea185-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="ea185-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ea185-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea185-125">**PSM \_ Setnexttextw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ea185-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 





