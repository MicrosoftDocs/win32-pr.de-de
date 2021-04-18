---
title: IMsRdpClientAdvancedSettings8 bandwidtherkennungs (Eigenschaft)
description: Gibt an, ob Bandbreiten Änderungen automatisch erkannt werden.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Bandwidtherkennungs-Eigenschaft Remotedesktopdienste
- Bandwidtherkennungs-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, bandwidtherkennungs (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338526"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="c6af0-106">IMsRdpClientAdvancedSettings8:: bandwidtherkennungs (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6af0-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="c6af0-107">Gibt an, ob Bandbreiten Änderungen automatisch erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="c6af0-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="c6af0-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c6af0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6af0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6af0-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="c6af0-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c6af0-110">Property value</span></span>

<span data-ttu-id="c6af0-111">**Variant \_ TRUE** , wenn Bandbreiten Änderungen automatisch erkannt werden, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="c6af0-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6af0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6af0-112">Requirements</span></span>



| <span data-ttu-id="c6af0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6af0-113">Requirement</span></span> | <span data-ttu-id="c6af0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c6af0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6af0-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6af0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c6af0-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6af0-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="c6af0-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6af0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c6af0-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6af0-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="c6af0-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c6af0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6af0-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6af0-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c6af0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c6af0-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6af0-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6af0-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6af0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6af0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6af0-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c6af0-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





