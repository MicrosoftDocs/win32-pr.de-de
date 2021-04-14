---
title: Itssbsession-Status Eigenschaft
description: Ruft den Sitzungszustand ab oder legt ihn fest.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- State-Eigenschaft Remotedesktopdienste
- State-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, State-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479101"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="e6197-106">Itssbsession:: State (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e6197-106">ITsSbSession::State property</span></span>

<span data-ttu-id="e6197-107">Ruft den Sitzungszustand ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e6197-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="e6197-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e6197-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6197-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6197-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="e6197-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e6197-110">Property value</span></span>

<span data-ttu-id="e6197-111">Ein Wert der [**tssession- \_ Zustands**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) Enumeration, die den Status einer Sitzung angibt.</span><span class="sxs-lookup"><span data-stu-id="e6197-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6197-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6197-112">Requirements</span></span>



| <span data-ttu-id="e6197-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6197-113">Requirement</span></span> | <span data-ttu-id="e6197-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e6197-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6197-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6197-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e6197-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e6197-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e6197-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6197-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e6197-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6197-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e6197-119">IDL</span><span class="sxs-lookup"><span data-stu-id="e6197-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6197-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6197-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6197-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6197-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6197-122">**Itssbsession**</span><span class="sxs-lookup"><span data-stu-id="e6197-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="e6197-123">**tssession- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="e6197-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





