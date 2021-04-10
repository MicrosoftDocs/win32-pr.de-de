---
title: PSM_HWNDTOINDEX Meldung (prsht. h)
description: Nimmt das Fenster Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ hwnddeindex-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Windows-Steuerelemente für PSM_HWNDTOINDEX Meldung
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104198"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="2e08b-105">PSM \_ hwnddeindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="2e08b-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="2e08b-106">Nimmt das Fenster Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück.</span><span class="sxs-lookup"><span data-stu-id="2e08b-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="2e08b-107">Sie können diese Nachricht explizit senden oder das [**propsheet- \_ hwnddeindex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e08b-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e08b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e08b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e08b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e08b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e08b-110">Handle für das Fenster der Seite.</span><span class="sxs-lookup"><span data-stu-id="2e08b-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="2e08b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e08b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e08b-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e08b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e08b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e08b-113">Return value</span></span>

<span data-ttu-id="2e08b-114">Gibt den NULL basierten Index der von *wParam* angegebenen Eigenschaften Blattseite zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2e08b-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="2e08b-115">Andernfalls wird –1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e08b-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e08b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e08b-116">Requirements</span></span>



| <span data-ttu-id="2e08b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e08b-117">Requirement</span></span> | <span data-ttu-id="2e08b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2e08b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e08b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e08b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2e08b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e08b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e08b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e08b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2e08b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e08b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e08b-123">Header</span><span class="sxs-lookup"><span data-stu-id="2e08b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e08b-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e08b-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





