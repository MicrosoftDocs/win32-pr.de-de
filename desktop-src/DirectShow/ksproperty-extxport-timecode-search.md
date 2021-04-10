---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeit Code zu suchen. Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041166"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="62472-104">ksproperty \_ extxport- \_ \_ timecodesuche</span><span class="sxs-lookup"><span data-stu-id="62472-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="62472-105">Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einem angegebenen Zeit Code zu suchen.</span><span class="sxs-lookup"><span data-stu-id="62472-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="62472-106">Der UVC-Gerätetreiber unterstützt diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="62472-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="62472-107">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="62472-107">Property Set GUID</span></span> | <span data-ttu-id="62472-108">propseetid- \_ Ext- \_ Transport</span><span class="sxs-lookup"><span data-stu-id="62472-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="62472-109">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="62472-109">Property ID</span></span>       | <span data-ttu-id="62472-110">ksproperty \_ extxport- \_ \_ timecodesuche</span><span class="sxs-lookup"><span data-stu-id="62472-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="62472-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="62472-111">Data Type</span></span>         | <span data-ttu-id="62472-112">**Ksproperty \_ Extxport \_ S** -Struktur</span><span class="sxs-lookup"><span data-stu-id="62472-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="62472-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62472-113">Remarks</span></span>

<span data-ttu-id="62472-114">Füllen Sie den **Timecode** -Member der **ksproperty \_ extxport \_ S** -Struktur mit dem gewünschten Frame, dem zweiten, der Minute und der Stunde aus.</span><span class="sxs-lookup"><span data-stu-id="62472-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="62472-115">Die Struktur von **ksproperty \_ extxport \_ S** wird im Windows-DDK beschrieben.</span><span class="sxs-lookup"><span data-stu-id="62472-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="62472-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62472-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62472-117">Eigenschaften Satz für externen Geräte Transport</span><span class="sxs-lookup"><span data-stu-id="62472-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



