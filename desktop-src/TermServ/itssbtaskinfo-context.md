---
title: Itssbtaskinfo-Kontext Eigenschaft
description: Ruft die dem Task zugeordneten Kontext Bytes ab.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- Kontext Eigenschaft Remotedesktopdienste
- Kontext Eigenschaft Remotedesktopdienste, itssbtaskinfo-Schnittstelle
- Itssbtaskinfo-Schnittstelle Remotedesktopdienste, Kontext Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106083"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="cccec-106">Itssbtaskinfo:: Context-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cccec-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="cccec-107">Ruft die dem Task zugeordneten Kontext Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="cccec-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="cccec-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cccec-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cccec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cccec-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="cccec-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cccec-110">Property value</span></span>

<span data-ttu-id="cccec-111">Der Kontext der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="cccec-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="cccec-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cccec-112">Requirements</span></span>



| <span data-ttu-id="cccec-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cccec-113">Requirement</span></span> | <span data-ttu-id="cccec-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cccec-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cccec-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cccec-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cccec-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cccec-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="cccec-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cccec-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cccec-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cccec-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="cccec-119">IDL</span><span class="sxs-lookup"><span data-stu-id="cccec-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cccec-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cccec-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cccec-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cccec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cccec-122">**Itssbtaskinfo**</span><span class="sxs-lookup"><span data-stu-id="cccec-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





