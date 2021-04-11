---
title: PSM_IDTOINDEX Meldung (prsht. h)
description: Übernimmt die Ressourcen-ID einer Eigenschaften Blattseite und gibt ihren Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ iddeindex-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Windows-Steuerelemente für PSM_IDTOINDEX Meldung
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105273"
---
# <a name="psm_idtoindex-message"></a><span data-ttu-id="447e1-105">PSM- \_ idumindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="447e1-105">PSM\_IDTOINDEX message</span></span>

<span data-ttu-id="447e1-106">Übernimmt die Ressourcen-ID einer Eigenschaften Blattseite und gibt ihren Null basierten Index zurück.</span><span class="sxs-lookup"><span data-stu-id="447e1-106">Takes the resource ID of a property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="447e1-107">Sie können diese Nachricht explizit senden oder das [**propsheet- \_ iddeindex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="447e1-107">You can send this message explicitly or use the [**PropSheet\_IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="447e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="447e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="447e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="447e1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="447e1-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="447e1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="447e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="447e1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="447e1-112">Die Ressourcen-ID der Seite.</span><span class="sxs-lookup"><span data-stu-id="447e1-112">Resource ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="447e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="447e1-113">Return value</span></span>

<span data-ttu-id="447e1-114">Gibt bei erfolgreicher Ausführung den NULL basierten Index der Eigenschaften Blattseite zurück, die von *LPARAM* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="447e1-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="447e1-115">Andernfalls wird –1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="447e1-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="447e1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="447e1-116">Requirements</span></span>



| <span data-ttu-id="447e1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="447e1-117">Requirement</span></span> | <span data-ttu-id="447e1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="447e1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="447e1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="447e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="447e1-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="447e1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="447e1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="447e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="447e1-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="447e1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="447e1-123">Header</span><span class="sxs-lookup"><span data-stu-id="447e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="447e1-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="447e1-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





