---
description: Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Eigenschaften Satzänderung vom Decoder verwendet werden soll.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371425"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="5a5ce-103">\_Ate \_ userateversion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a5ce-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="5a5ce-104">Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Eigenschaften Satzänderung vom Decoder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a5ce-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="5a5ce-105">Der Wert ist ein **Worttyp** .</span><span class="sxs-lookup"><span data-stu-id="5a5ce-105">The value is a **WORD** type.</span></span> <span data-ttu-id="5a5ce-106">Das hochwertige Byte enthält die neben Versionsnummer, und das nieder wertige Byte enthält das nieder wertige Byte.</span><span class="sxs-lookup"><span data-stu-id="5a5ce-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="5a5ce-107">Daher wird Version 1,1 mit dem Wert 0x0101 signalisiert.</span><span class="sxs-lookup"><span data-stu-id="5a5ce-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="5a5ce-108">Wenn der Decoder die angegebene Version nicht unterstützt, sollte er den [**callspropertyset:: Set**](ikspropertyset-set.md) -Befehl nicht ausführen und E \_ nointerface zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5a5ce-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="5a5ce-109">Wenn der Quell Filter die Version nicht festgelegt hat, sollte der Decoder standardmäßig auf Version 1,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a5ce-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="5a5ce-110">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="5a5ce-110">Property Set GUID</span></span> | <span data-ttu-id="5a5ce-111">AM \_ kspropltid \_</span><span class="sxs-lookup"><span data-stu-id="5a5ce-111">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="5a5ce-112">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="5a5ce-112">Property ID</span></span>       | <span data-ttu-id="5a5ce-113">\_ \_ Userateversion für ATE</span><span class="sxs-lookup"><span data-stu-id="5a5ce-113">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="5a5ce-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5a5ce-114">Data Type</span></span>         | <span data-ttu-id="5a5ce-115">**WORD**</span><span class="sxs-lookup"><span data-stu-id="5a5ce-115">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="5a5ce-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a5ce-116">Requirements</span></span>



| <span data-ttu-id="5a5ce-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a5ce-117">Requirement</span></span> | <span data-ttu-id="5a5ce-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5a5ce-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5ce-119">Header</span><span class="sxs-lookup"><span data-stu-id="5a5ce-119">Header</span></span><br/> | <dl> <span data-ttu-id="5a5ce-120"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a5ce-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a5ce-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a5ce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a5ce-122">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="5a5ce-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




