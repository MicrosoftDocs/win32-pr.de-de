---
title: Itssbtaskinfo-Status Eigenschaft
description: Ruft einen RDV- \_ \_ aufgabenstatusenumerationswert ab, der den Zustand der Aufgabe darstellt.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Status Eigenschaften Remotedesktopdienste
- Status Eigenschaften Remotedesktopdienste, itssbtaskinfo-Schnittstelle
- Itssbtaskinfo-Schnittstelle Remotedesktopdienste, Status-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741312"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="5347f-106">Itssbtaskinfo:: Status-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5347f-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="5347f-107">Ruft einen RDV-aufgabenstatusenumerationswert ab, der den Zustand der Aufgabe darstellt. [**\_ \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)</span><span class="sxs-lookup"><span data-stu-id="5347f-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="5347f-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5347f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5347f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5347f-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="5347f-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5347f-110">Property value</span></span>

<span data-ttu-id="5347f-111">Ein RDV-aufgabenstatusenumerationswert, der den Zustand der Aufgabe darstellt. [**\_ \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)</span><span class="sxs-lookup"><span data-stu-id="5347f-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="5347f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5347f-112">Requirements</span></span>



| <span data-ttu-id="5347f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5347f-113">Requirement</span></span> | <span data-ttu-id="5347f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="5347f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5347f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5347f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5347f-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5347f-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5347f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5347f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5347f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5347f-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="5347f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="5347f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5347f-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5347f-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5347f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5347f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5347f-122">**Itssbtaskinfo**</span><span class="sxs-lookup"><span data-stu-id="5347f-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





