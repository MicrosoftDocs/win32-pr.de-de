---
title: Imsrdpdrive-Name (Eigenschaft)
description: Ruft den Namen des Laufwerks ab.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Name-Eigenschaft Remotedesktopdienste
- Name-Eigenschaft Remotedesktopdienste, imsrdpdrive-Schnittstelle
- Imsrdpdrive-Schnittstelle Remotedesktopdienste, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477739"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="f52dd-106">Imsrdpdrive:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f52dd-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="f52dd-107">Ruft den Namen des Laufwerks ab.</span><span class="sxs-lookup"><span data-stu-id="f52dd-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="f52dd-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f52dd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f52dd-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="f52dd-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f52dd-110">Property value</span></span>

<span data-ttu-id="f52dd-111">Der Name des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="f52dd-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f52dd-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f52dd-112">Error codes</span></span>

<span data-ttu-id="f52dd-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f52dd-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="f52dd-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f52dd-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52dd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f52dd-115">Requirements</span></span>



| <span data-ttu-id="f52dd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f52dd-116">Requirement</span></span> | <span data-ttu-id="f52dd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f52dd-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f52dd-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f52dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f52dd-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f52dd-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f52dd-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f52dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f52dd-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f52dd-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f52dd-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f52dd-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f52dd-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f52dd-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f52dd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f52dd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f52dd-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f52dd-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f52dd-126">IID</span><span class="sxs-lookup"><span data-stu-id="f52dd-126">IID</span></span><br/>                      | <span data-ttu-id="f52dd-127">IID \_ imsrdpdrive ist als d28b5458-f694-47a8-8e61-40356a767e46 definiert.</span><span class="sxs-lookup"><span data-stu-id="f52dd-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f52dd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f52dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52dd-129">**Imsrdpdrive**</span><span class="sxs-lookup"><span data-stu-id="f52dd-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





