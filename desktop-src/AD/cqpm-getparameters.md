---
title: CQPM_GETPARAMETERS Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um Daten zu der von der Seite ausgeführten Abfrage abzurufen.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858714"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="0ba33-104">Cqpm \_ GetParameters-Meldung</span><span class="sxs-lookup"><span data-stu-id="0ba33-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="0ba33-105">Die **cqpm \_ GetParameters** -Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um Daten zu der von der Seite ausgeführten Abfrage abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0ba33-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ba33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba33-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ba33-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba33-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ba33-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ba33-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ba33-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba33-110">Zeiger auf einen [**lpdsqueryparametwert**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) , der Daten über die von der Seite ausgeführte Abfrage empfängt.</span><span class="sxs-lookup"><span data-stu-id="0ba33-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="0ba33-111">Wenn dieser Parameter **null** ist, muss die **dsqueryparams** -Struktur durch die Erweiterung mithilfe der [**cotaskmemzuzug-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0ba33-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba33-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ba33-112">Return value</span></span>

<span data-ttu-id="0ba33-113">Gibt bei Erfolg **S \_ OK** oder andernfalls einen Standard- **HRESULT** -Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="0ba33-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba33-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ba33-114">Requirements</span></span>



| <span data-ttu-id="0ba33-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ba33-115">Requirement</span></span> | <span data-ttu-id="0ba33-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0ba33-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba33-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ba33-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba33-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ba33-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="0ba33-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ba33-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba33-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba33-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="0ba33-121">Header</span><span class="sxs-lookup"><span data-stu-id="0ba33-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ba33-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba33-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba33-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ba33-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba33-124">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="0ba33-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="0ba33-125">**Dsquerypara meters**</span><span class="sxs-lookup"><span data-stu-id="0ba33-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="0ba33-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="0ba33-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

