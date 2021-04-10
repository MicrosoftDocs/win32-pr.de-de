---
title: PSM_INDEXTOHWND Meldung (prsht. h)
description: Nimmt den Index einer Eigenschaften Blattseite an und gibt das Fenster Handle zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ indexdehwnd-Makro verwenden.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Windows-Steuerelemente für PSM_INDEXTOHWND Meldung
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105261"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="a8cbd-105">PSM- \_ Indexdienst-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a8cbd-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="a8cbd-106">Nimmt den Index einer Eigenschaften Blattseite an und gibt das Fenster Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="a8cbd-107">Sie können diese Nachricht explizit senden oder das [**propsheet- \_ indexdehwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8cbd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8cbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8cbd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8cbd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8cbd-110">Der null basierte Index der Seite.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="a8cbd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8cbd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8cbd-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8cbd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8cbd-113">Return value</span></span>

<span data-ttu-id="a8cbd-114">Gibt das Handle für das Fenster der Eigenschaften Blattseite zurück, das bei erfolgreicher Ausführung von *wParam* angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="a8cbd-115">Andernfalls wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8cbd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8cbd-116">Requirements</span></span>



| <span data-ttu-id="a8cbd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8cbd-117">Requirement</span></span> | <span data-ttu-id="a8cbd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a8cbd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8cbd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8cbd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a8cbd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8cbd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a8cbd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8cbd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a8cbd-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8cbd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a8cbd-123">Header</span><span class="sxs-lookup"><span data-stu-id="a8cbd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8cbd-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8cbd-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





