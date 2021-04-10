---
title: CQPM_PERSIST Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seite Abfrage Daten aus persistenten Speicher lesen oder schreiben kann.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040551"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="f2e39-104">Cqpm- \_ persistenznachricht</span><span class="sxs-lookup"><span data-stu-id="f2e39-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="f2e39-105">Die **cqpm \_ -persistenznachricht** wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seite Abfrage Daten aus persistenten Speicher lesen oder schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="f2e39-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2e39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e39-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2e39-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e39-108">Enthält einen Wert ungleich 0, um die Abfrage Daten zu lesen, oder NULL, um die Abfrage Daten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f2e39-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="f2e39-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2e39-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e39-110">Zeiger auf eine [**ipersistquery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) -Schnittstelle, von der die Abfrage Daten gelesen oder geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2e39-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e39-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2e39-111">Return value</span></span>

<span data-ttu-id="f2e39-112">Gibt bei Erfolg **S \_ OK** oder andernfalls einen Standard- **HRESULT** -Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="f2e39-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e39-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2e39-113">Requirements</span></span>



| <span data-ttu-id="f2e39-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2e39-114">Requirement</span></span> | <span data-ttu-id="f2e39-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e39-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e39-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2e39-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e39-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2e39-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f2e39-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2e39-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e39-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2e39-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f2e39-120">Header</span><span class="sxs-lookup"><span data-stu-id="f2e39-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e39-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e39-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e39-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2e39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e39-123">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="f2e39-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="f2e39-124">**Ipersistquery**</span><span class="sxs-lookup"><span data-stu-id="f2e39-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

