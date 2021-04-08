---
title: CQPM_CLEARFORM Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrage für die Erweiterungs Seite gesendet, wenn der Inhalt der Seite auf die Standardwerte zurückgesetzt werden soll.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- CQPM_CLEARFORM Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949497"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="44428-104">Cqpm- \_ ClearForm-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44428-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="44428-105">Die **cqpm \_ ClearForm** -Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrage für die Erweiterungs Seite gesendet, wenn der Inhalt der Seite auf die Standardwerte zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44428-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="44428-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44428-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44428-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44428-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44428-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="44428-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44428-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44428-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44428-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44428-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44428-111">Return value</span></span>

<span data-ttu-id="44428-112">Gibt bei Erfolg **S \_ OK** oder andernfalls einen Standard- **HRESULT** -Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="44428-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="44428-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44428-113">Requirements</span></span>



| <span data-ttu-id="44428-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44428-114">Requirement</span></span> | <span data-ttu-id="44428-115">Wert</span><span class="sxs-lookup"><span data-stu-id="44428-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44428-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44428-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44428-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44428-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="44428-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44428-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44428-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44428-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="44428-120">Header</span><span class="sxs-lookup"><span data-stu-id="44428-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44428-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="44428-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44428-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44428-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44428-123">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="44428-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





