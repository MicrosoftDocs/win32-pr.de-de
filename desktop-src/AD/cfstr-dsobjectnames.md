---
title: CFSTR_DSOBJECTNAMES (DSClient. h)
description: Das cfstr \_ dsobjectnames-Zwischenablage Format bietet ein globales Speicher handle (HGLOBAL), das die dsobjectnames-Struktur enthält.
ms.assetid: b28428fa-1504-4dcc-9b2b-32ca1ae30ec5
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOBJECTNAMES
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816f99f1b50f97ac362706cc46e4dbe4edf5f486
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103378"
---
# <a name="cfstr_dsobjectnames"></a><span data-ttu-id="9cf44-103">cfstr \_ dsobjectnames</span><span class="sxs-lookup"><span data-stu-id="9cf44-103">CFSTR\_DSOBJECTNAMES</span></span>

<dl> <dt>

<span data-ttu-id="9cf44-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**cfstr \_ dsobjectnames**</span><span class="sxs-lookup"><span data-stu-id="9cf44-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**CFSTR\_DSOBJECTNAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cf44-105">"Dsobjectnames"</span><span class="sxs-lookup"><span data-stu-id="9cf44-105">"DsObjectNames"</span></span>
</dt> <dt>



<span data-ttu-id="9cf44-106">Das Zwischenablage Format von **cfstr \_ dsobjectnames** wird von dem [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) unterstützt, das von der [**icommonquery:: openquerywindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) -Methode bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9cf44-106">The **CFSTR\_DSOBJECTNAMES** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="9cf44-107">Das **cfstr \_ dsobjectnames** -Zwischenablage Format bietet ein globales Speicher handle (**HGLOBAL**), das die [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="9cf44-107">The **CFSTR\_DSOBJECTNAMES** clipboard format provides a global memory handle (**HGLOBAL**) that contains [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9cf44-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cf44-108">Requirements</span></span>



| <span data-ttu-id="9cf44-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cf44-109">Requirement</span></span> | <span data-ttu-id="9cf44-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9cf44-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf44-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cf44-111">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf44-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cf44-112">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="9cf44-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cf44-113">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf44-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cf44-114">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="9cf44-115">Header</span><span class="sxs-lookup"><span data-stu-id="9cf44-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cf44-116"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cf44-116"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cf44-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cf44-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf44-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="9cf44-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="9cf44-119">**Icommonquery:: openquerywindow**</span><span class="sxs-lookup"><span data-stu-id="9cf44-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="9cf44-120">**Dsobjectnames**</span><span class="sxs-lookup"><span data-stu-id="9cf44-120">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> </dl>

 

