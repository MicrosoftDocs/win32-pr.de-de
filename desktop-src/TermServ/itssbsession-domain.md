---
title: Itssbsession-Domänen Eigenschaft
description: Ruft den Domänen Namen des Benutzers ab.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Domänen Eigenschaft Remotedesktopdienste
- Domänen Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, Domain-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339598"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="c97da-106">Itssbsession::D omain-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c97da-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="c97da-107">Ruft den Domänen Namen des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="c97da-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="c97da-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c97da-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97da-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97da-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="c97da-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c97da-110">Property value</span></span>

<span data-ttu-id="c97da-111">Ein Zeiger auf eine **BSTR** -Variable, die den Domänen Namen des Benutzers empfängt.</span><span class="sxs-lookup"><span data-stu-id="c97da-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97da-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c97da-112">Requirements</span></span>



| <span data-ttu-id="c97da-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c97da-113">Requirement</span></span> | <span data-ttu-id="c97da-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c97da-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c97da-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c97da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c97da-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c97da-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c97da-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c97da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c97da-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c97da-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c97da-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c97da-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c97da-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c97da-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97da-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c97da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97da-122">**Itssbsession**</span><span class="sxs-lookup"><span data-stu-id="c97da-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





