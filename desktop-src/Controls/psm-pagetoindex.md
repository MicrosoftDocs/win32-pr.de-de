---
title: PSM_PAGETOINDEX Meldung (prsht. h)
description: Nimmt das hpropsheetpage-Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das "propsheet \_ Page$ Index"-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Windows-Steuerelemente für PSM_PAGETOINDEX Meldung
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344064"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="217c9-105">PSM- \_ pageumindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="217c9-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="217c9-106">Nimmt das hpropsheetpage-Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück.</span><span class="sxs-lookup"><span data-stu-id="217c9-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="217c9-107">Sie können diese Nachricht explizit senden oder das " [**propsheet \_ Page$ Index**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) "-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="217c9-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="217c9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="217c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="217c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="217c9-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="217c9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="217c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="217c9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="217c9-112">Hpropsheetpage-Handle für die Eigenschaften Blattseite.</span><span class="sxs-lookup"><span data-stu-id="217c9-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217c9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="217c9-113">Return value</span></span>

<span data-ttu-id="217c9-114">Gibt bei erfolgreicher Ausführung den NULL basierten Index der Eigenschaften Blattseite zurück, die von *LPARAM* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="217c9-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="217c9-115">Andernfalls wird –1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="217c9-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="217c9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="217c9-116">Requirements</span></span>



| <span data-ttu-id="217c9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="217c9-117">Requirement</span></span> | <span data-ttu-id="217c9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="217c9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="217c9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="217c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="217c9-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="217c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="217c9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="217c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="217c9-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="217c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="217c9-123">Header</span><span class="sxs-lookup"><span data-stu-id="217c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="217c9-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="217c9-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





