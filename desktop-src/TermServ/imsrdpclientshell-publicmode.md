---
title: Imsrdpclientshell publicmode (Eigenschaft)
description: Gibt an oder Ruft ab, ob der öffentliche Modus aktiviert ist.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Publicmode-Eigenschaft Remotedesktopdienste
- Publicmode-Eigenschaft Remotedesktopdienste, imsrdpclientshell-Schnittstelle
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, publicmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477760"
---
# <a name="imsrdpclientshellpublicmode-property"></a><span data-ttu-id="0f0b6-106">Imsrdpclientshell::P ublicmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0f0b6-106">IMsRdpClientShell::PublicMode property</span></span>

<span data-ttu-id="0f0b6-107">Gibt an oder Ruft ab, ob der öffentliche Modus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f0b6-107">Specifies or retrieves whether public mode is enabled.</span></span>

<span data-ttu-id="0f0b6-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0f0b6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0b6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f0b6-109">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="0f0b6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0f0b6-110">Property value</span></span>

<span data-ttu-id="0f0b6-111">Gibt an, ob der öffentliche Modus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f0b6-111">Specifies whether public mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f0b6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f0b6-112">Requirements</span></span>



| <span data-ttu-id="0f0b6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f0b6-113">Requirement</span></span> | <span data-ttu-id="0f0b6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0f0b6-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0b6-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f0b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0b6-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f0b6-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0f0b6-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f0b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0b6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f0b6-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0f0b6-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0f0b6-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f0b6-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f0b6-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f0b6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0b6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f0b6-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f0b6-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f0b6-123">IID</span><span class="sxs-lookup"><span data-stu-id="0f0b6-123">IID</span></span><br/>                      | <span data-ttu-id="0f0b6-124">IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.</span><span class="sxs-lookup"><span data-stu-id="0f0b6-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0f0b6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f0b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0b6-126">**Imsrdpclientshell**</span><span class="sxs-lookup"><span data-stu-id="0f0b6-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





