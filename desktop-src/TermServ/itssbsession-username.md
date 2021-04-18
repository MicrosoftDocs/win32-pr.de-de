---
title: Itssbsession username (Eigenschaft)
description: Ruft den Benutzernamen für diese Sitzung ab.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Remotedesktopdienste
- Username-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344104"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="d70f1-106">Itssbsession:: username (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d70f1-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="d70f1-107">Ruft den Benutzernamen für diese Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="d70f1-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="d70f1-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70f1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d70f1-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="d70f1-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d70f1-110">Property value</span></span>

<span data-ttu-id="d70f1-111">Ein Zeiger auf eine **BSTR** -Variable, die den Benutzernamen für diese Sitzung empfängt.</span><span class="sxs-lookup"><span data-stu-id="d70f1-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70f1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d70f1-112">Requirements</span></span>



| <span data-ttu-id="d70f1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d70f1-113">Requirement</span></span> | <span data-ttu-id="d70f1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d70f1-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d70f1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d70f1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d70f1-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d70f1-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d70f1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d70f1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d70f1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d70f1-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d70f1-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d70f1-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d70f1-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d70f1-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70f1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d70f1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70f1-122">**Itssbsession**</span><span class="sxs-lookup"><span data-stu-id="d70f1-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





