---
title: Itssbtaskinfo-Bezeichnung (Eigenschaft)
description: Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Eigenschaft "Bezeichnung" Remotedesktopdienste
- Label-Eigenschaft Remotedesktopdienste, itssbtaskinfo-Schnittstelle
- Itssbtaskinfo-Schnittstelle Remotedesktopdienste, Label-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743505"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="68664-106">Itssbtaskinfo:: Label-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68664-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="68664-107">Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="68664-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="68664-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="68664-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68664-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68664-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="68664-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="68664-110">Property value</span></span>

<span data-ttu-id="68664-111">Ein Zeiger auf einen **BSTR** -Wert, der die Bezeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="68664-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="68664-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68664-112">Requirements</span></span>



| <span data-ttu-id="68664-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68664-113">Requirement</span></span> | <span data-ttu-id="68664-114">Wert</span><span class="sxs-lookup"><span data-stu-id="68664-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68664-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68664-115">Minimum supported client</span></span><br/> | <span data-ttu-id="68664-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68664-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="68664-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68664-117">Minimum supported server</span></span><br/> | <span data-ttu-id="68664-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68664-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="68664-119">IDL</span><span class="sxs-lookup"><span data-stu-id="68664-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68664-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68664-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68664-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68664-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68664-122">**Itssbtaskinfo**</span><span class="sxs-lookup"><span data-stu-id="68664-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





