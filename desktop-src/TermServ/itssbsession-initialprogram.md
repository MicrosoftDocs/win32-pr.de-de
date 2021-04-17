---
title: Itssbsession InitialProgram (Eigenschaft)
description: Ruft das Anfangs Programm für diese Sitzung ab oder legt es fest.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- InitialProgram-Eigenschaft Remotedesktopdienste
- InitialProgram-Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, InitialProgram-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476728"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="1fb0c-106">Itssbsession:: InitialProgram-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1fb0c-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="1fb0c-107">Ruft das Anfangs Programm für diese Sitzung ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="1fb0c-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="1fb0c-108">Das erste Programm ist das Programm, das beim Starten der Benutzersitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1fb0c-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="1fb0c-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1fb0c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb0c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fb0c-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="1fb0c-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1fb0c-111">Property value</span></span>

<span data-ttu-id="1fb0c-112">Eine **BSTR** -Variable, die das ursprüngliche Programm enthält.</span><span class="sxs-lookup"><span data-stu-id="1fb0c-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb0c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fb0c-113">Requirements</span></span>



| <span data-ttu-id="1fb0c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fb0c-114">Requirement</span></span> | <span data-ttu-id="1fb0c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1fb0c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb0c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fb0c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb0c-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1fb0c-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="1fb0c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fb0c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb0c-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fb0c-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="1fb0c-120">IDL</span><span class="sxs-lookup"><span data-stu-id="1fb0c-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fb0c-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fb0c-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb0c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fb0c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb0c-123">**Itssbsession**</span><span class="sxs-lookup"><span data-stu-id="1fb0c-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





