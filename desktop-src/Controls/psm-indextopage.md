---
title: PSM_INDEXTOPAGE Meldung (prsht. h)
description: Nimmt den Index einer Eigenschaften Blattseite an und gibt das hpropsheetpage-Handle zurück. Sie können diese Nachricht explizit senden oder das propsheet \_ indextopage-Makro verwenden.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Windows-Steuerelemente für PSM_INDEXTOPAGE Meldung
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478240"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="36e4e-105">PSM- \_ indextopage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="36e4e-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="36e4e-106">Nimmt den Index einer Eigenschaften Blattseite an und gibt das hpropsheetpage-Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="36e4e-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="36e4e-107">Sie können diese Nachricht explizit senden oder das [**propsheet \_ indextopage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="36e4e-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36e4e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="36e4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e4e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36e4e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36e4e-110">Der null basierte Index der Seite.</span><span class="sxs-lookup"><span data-stu-id="36e4e-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="36e4e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36e4e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36e4e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="36e4e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36e4e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36e4e-113">Return value</span></span>

<span data-ttu-id="36e4e-114">Gibt das hpropsheetpage-Handle der von *wParam* angegebenen Eigenschaften Blattseite zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="36e4e-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="36e4e-115">Andernfalls wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="36e4e-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="36e4e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36e4e-116">Requirements</span></span>



| <span data-ttu-id="36e4e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36e4e-117">Requirement</span></span> | <span data-ttu-id="36e4e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="36e4e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36e4e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36e4e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36e4e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36e4e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="36e4e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36e4e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36e4e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36e4e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36e4e-123">Header</span><span class="sxs-lookup"><span data-stu-id="36e4e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36e4e-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="36e4e-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





