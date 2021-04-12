---
title: ITSRemoteProgram2 remoteapplicationargs (Eigenschaft)
description: Die Befehlszeilenargumente für RemoteApp.
ms.assetid: c1c36876-df3d-4ef9-a5ac-f623bc51fe7b
ms.tgt_platform: multiple
keywords:
- Remoteapplicationargs-Eigenschaft Remotedesktopdienste
- Remoteapplicationargs-Eigenschaft Remotedesktopdienste, ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2 Interface Remotedesktopdienste, remoteapplicationargs-Eigenschaft
- Remoteapplicationargs-Eigenschaft Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, remoteapplicationargs-Eigenschaft
topic_type:
- apiref
api_name:
- ITSRemoteProgram2.RemoteApplicationArgs
- ITSRemoteProgram2.put_RemoteApplicationArgs
- ITSRemoteProgram3.RemoteApplicationArgs
- ITSRemoteProgram3.put_RemoteApplicationArgs
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b77cc7259520156321140c8f85713095f02e2b78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105861"
---
# <a name="itsremoteprogram2remoteapplicationargs-property"></a><span data-ttu-id="8285d-108">ITSRemoteProgram2:: remoteapplicationargs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8285d-108">ITSRemoteProgram2::RemoteApplicationArgs property</span></span>

<span data-ttu-id="8285d-109">Die Befehlszeilenargumente für RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8285d-109">The command-line arguments for the RemoteApp.</span></span>

<span data-ttu-id="8285d-110">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="8285d-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8285d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8285d-111">Syntax</span></span>


```C++
HRESULT put_RemoteApplicationArgs(
  [in] BSTR bstrRemoteApplicationArgs
);
```



## <a name="property-value"></a><span data-ttu-id="8285d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8285d-112">Property value</span></span>

<span data-ttu-id="8285d-113">Die RemoteApp-Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="8285d-113">The RemoteApp command-line arguments.</span></span>

## <a name="requirements"></a><span data-ttu-id="8285d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8285d-114">Requirements</span></span>



| <span data-ttu-id="8285d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8285d-115">Requirement</span></span> | <span data-ttu-id="8285d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8285d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8285d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8285d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8285d-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8285d-118">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="8285d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8285d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8285d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8285d-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8285d-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8285d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8285d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8285d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8285d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8285d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8285d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8285d-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8285d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8285d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8285d-126">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="8285d-126">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="8285d-127">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="8285d-127">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> </dl>

 

 





