---
title: Itssbtaskinfo-Bezeichnereigenschaft
description: Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Bezeichnereigenschaft Remotedesktopdienste
- Bezeichnereigenschaft Remotedesktopdienste, itssbtaskinfo-Schnittstelle
- Itssbtaskinfo-Schnittstelle Remotedesktopdienste, Bezeichnereigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743640"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="b87c3-106">Itssbtaskinfo:: Identifier-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b87c3-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="b87c3-107">Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b87c3-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="b87c3-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b87c3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87c3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b87c3-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="b87c3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b87c3-110">Property value</span></span>

<span data-ttu-id="b87c3-111">Ein Zeiger auf einen **BSTR** -Wert, der die GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="b87c3-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87c3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b87c3-112">Requirements</span></span>



| <span data-ttu-id="b87c3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b87c3-113">Requirement</span></span> | <span data-ttu-id="b87c3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b87c3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b87c3-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b87c3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b87c3-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b87c3-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b87c3-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b87c3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b87c3-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b87c3-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="b87c3-119">IDL</span><span class="sxs-lookup"><span data-stu-id="b87c3-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b87c3-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b87c3-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b87c3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b87c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87c3-122">**Itssbtaskinfo**</span><span class="sxs-lookup"><span data-stu-id="b87c3-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





