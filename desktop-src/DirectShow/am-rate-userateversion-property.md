---
description: Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Rate Change-Eigenschaft den Decoder verwenden soll.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910218"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="cb05e-103">AM \_ RATE \_ UseRateVersion-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb05e-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="cb05e-104">Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Rate Change-Eigenschaft den Decoder verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="cb05e-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="cb05e-105">Der Wert ist ein **WORD-Typ.**</span><span class="sxs-lookup"><span data-stu-id="cb05e-105">The value is a **WORD** type.</span></span> <span data-ttu-id="cb05e-106">Das obere Byte enthält die Nebenversionsnummer, und das niedrige Byte enthält das niedrige Byte.</span><span class="sxs-lookup"><span data-stu-id="cb05e-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="cb05e-107">Daher wird Version 1.1 mit dem Wert 0x0101.</span><span class="sxs-lookup"><span data-stu-id="cb05e-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="cb05e-108">Wenn der Decoder die angegebene Version nicht unterstützt, sollte der Aufruf von [**IKsPropertySet::Set**](ikspropertyset-set.md) fehlschlagen und E \_ NOINTERFACE zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cb05e-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="cb05e-109">Wenn der Quellfilter die Version nicht festgelegt, sollte der Decoder standardmäßig auf Version 1.0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb05e-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



| <span data-ttu-id="cb05e-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="cb05e-110">Label</span></span> | <span data-ttu-id="cb05e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="cb05e-111">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="cb05e-112">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="cb05e-112">Property Set GUID</span></span> | <span data-ttu-id="cb05e-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="cb05e-113">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="cb05e-114">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="cb05e-114">Property ID</span></span>       | <span data-ttu-id="cb05e-115">AM \_ RATE \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="cb05e-115">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="cb05e-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cb05e-116">Data Type</span></span>         | <span data-ttu-id="cb05e-117">**WORD**</span><span class="sxs-lookup"><span data-stu-id="cb05e-117">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="cb05e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb05e-118">Requirements</span></span>



| <span data-ttu-id="cb05e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb05e-119">Requirement</span></span> | <span data-ttu-id="cb05e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cb05e-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb05e-121">Header</span><span class="sxs-lookup"><span data-stu-id="cb05e-121">Header</span></span><br/> | <dl> <span data-ttu-id="cb05e-122"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="cb05e-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb05e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb05e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb05e-124">**Rate Change Property Set**</span><span class="sxs-lookup"><span data-stu-id="cb05e-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




