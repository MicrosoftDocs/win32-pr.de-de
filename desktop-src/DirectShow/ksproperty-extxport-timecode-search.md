---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeitcode zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909438"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="761c7-104">KSPROPERTY \_ \_ EXTXPORT-ZEITCODESUCHE \_</span><span class="sxs-lookup"><span data-stu-id="761c7-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="761c7-105">Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeitcode zu suchen.</span><span class="sxs-lookup"><span data-stu-id="761c7-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="761c7-106">Der UVC-Gerätetreiber unterstützt diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="761c7-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="761c7-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="761c7-107">Label</span></span> | <span data-ttu-id="761c7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="761c7-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="761c7-109">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="761c7-109">Property Set GUID</span></span> | <span data-ttu-id="761c7-110">PROPSETID \_ \_ EXT-TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="761c7-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="761c7-111">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="761c7-111">Property ID</span></span>       | <span data-ttu-id="761c7-112">KSPROPERTY \_ \_ EXTXPORT-ZEITCODESUCHE \_</span><span class="sxs-lookup"><span data-stu-id="761c7-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="761c7-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="761c7-113">Data Type</span></span>         | <span data-ttu-id="761c7-114">**KSPROPERTY \_ EXTXPORT \_ S-Struktur**</span><span class="sxs-lookup"><span data-stu-id="761c7-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="761c7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="761c7-115">Remarks</span></span>

<span data-ttu-id="761c7-116">Füllen Sie das **Timecode-Member** der **KSPROPERTY \_ EXTXPORT \_ S-Struktur** mit dem gewünschten Frame, der Sekunde, der Minute und der Stunde aus.</span><span class="sxs-lookup"><span data-stu-id="761c7-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="761c7-117">Die **KSPROPERTY \_ EXTXPORT \_ S-Struktur** wird im Windows-DDK beschrieben.</span><span class="sxs-lookup"><span data-stu-id="761c7-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="761c7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="761c7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761c7-119">Transporteigenschaftssatz für externe Geräte</span><span class="sxs-lookup"><span data-stu-id="761c7-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



