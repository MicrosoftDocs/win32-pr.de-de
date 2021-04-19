---
title: Itssbsession-TargetName-Eigenschaft
description: Ruft den Namen des Ziels ab, auf dem diese Sitzung erstellt wurde.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- TargetName-Eigenschaft Remotedesktopdienste
- TargetName-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, TargetName-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342481"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="d88cf-106">Itssbsession:: TargetName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d88cf-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="d88cf-107">Ruft den Namen des Ziels ab, auf dem diese Sitzung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d88cf-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="d88cf-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d88cf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88cf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d88cf-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="d88cf-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d88cf-110">Property value</span></span>

<span data-ttu-id="d88cf-111">Ein Zeiger auf eine **BSTR** -Variable, die den Namen des Ziels empfängt, auf dem diese Sitzung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d88cf-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88cf-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d88cf-112">Requirements</span></span>



| <span data-ttu-id="d88cf-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d88cf-113">Requirement</span></span> | <span data-ttu-id="d88cf-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d88cf-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d88cf-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d88cf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d88cf-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d88cf-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d88cf-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d88cf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d88cf-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d88cf-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d88cf-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d88cf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d88cf-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d88cf-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88cf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d88cf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88cf-122">**Itssbsession**</span><span class="sxs-lookup"><span data-stu-id="d88cf-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





