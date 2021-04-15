---
title: CQPM_SETDEFAULTPARAMETERS Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um alternative Standardparameter für die Seite festzulegen.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- CQPM_SETDEFAULTPARAMETERS Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476491"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="48f4c-104">Cqpm- \_ setdefaultparameters-Meldung</span><span class="sxs-lookup"><span data-stu-id="48f4c-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="48f4c-105">Die **cqpm- \_ setdefaultparameters** -Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um alternative Standardparameter für die Seite festzulegen.</span><span class="sxs-lookup"><span data-stu-id="48f4c-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="48f4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48f4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48f4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48f4c-108">Enthält einen Wert ungleich 0 (null), wenn die Seite die Standardseite ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="48f4c-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="48f4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48f4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48f4c-110">Ein Zeiger auf eine [**openquerywindow**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) -Struktur, die Daten zum Dialogfeld Verzeichnisdienst Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="48f4c-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f4c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48f4c-111">Return value</span></span>

<span data-ttu-id="48f4c-112">Der Rückgabewert für diese Nachricht wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="48f4c-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f4c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48f4c-113">Requirements</span></span>



| <span data-ttu-id="48f4c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48f4c-114">Requirement</span></span> | <span data-ttu-id="48f4c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="48f4c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48f4c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48f4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48f4c-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48f4c-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="48f4c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48f4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48f4c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48f4c-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="48f4c-120">Header</span><span class="sxs-lookup"><span data-stu-id="48f4c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f4c-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f4c-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f4c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48f4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f4c-123">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="48f4c-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="48f4c-124">**Openquerywindow**</span><span class="sxs-lookup"><span data-stu-id="48f4c-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





