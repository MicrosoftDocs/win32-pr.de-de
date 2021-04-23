---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Tracknummer (ATN) zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909447"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="53812-104">KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="53812-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="53812-105">Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Tracknummer (ATN) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="53812-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="53812-106">Der UVC-Gerätetreiber unterstützt diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="53812-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="53812-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="53812-107">Label</span></span> | <span data-ttu-id="53812-108">Wert</span><span class="sxs-lookup"><span data-stu-id="53812-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="53812-109">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="53812-109">Property Set GUID</span></span> | <span data-ttu-id="53812-110">PROPSETID \_ \_ EXT-TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="53812-110">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="53812-111">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="53812-111">Property ID</span></span>       | <span data-ttu-id="53812-112">KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="53812-112">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="53812-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="53812-113">Data Type</span></span>         | <span data-ttu-id="53812-114">**KSPROPERTY \_ EXTXPORT \_ S-Struktur**</span><span class="sxs-lookup"><span data-stu-id="53812-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="53812-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53812-115">Remarks</span></span>

<span data-ttu-id="53812-116">Legen Sie **das dwAbsTrackNumber-Member** der **KSPROPERTY \_ EXTXPORT \_ S-Struktur** auf den folgenden Wert fest:</span><span class="sxs-lookup"><span data-stu-id="53812-116">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="53812-117">Die UVC-Spezifikation definiert nicht, wie das Gerät das Kontinuitätsbit verwendet.</span><span class="sxs-lookup"><span data-stu-id="53812-117">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="53812-118">Die **KSPROPERTY \_ EXTXPORT \_ S-Struktur** wird im Windows-DDK beschrieben.</span><span class="sxs-lookup"><span data-stu-id="53812-118">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="53812-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53812-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53812-120">Transporteigenschaftssatz für externe Geräte</span><span class="sxs-lookup"><span data-stu-id="53812-120">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



