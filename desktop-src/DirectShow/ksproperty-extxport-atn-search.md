---
description: Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Nachverfolgung zu suchen (ATN). Der UVC-Gerätetreiber unterstützt diese Eigenschaft.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344770"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="9b6fc-104">ksproperty \_ extxport- \_ Atn- \_ Suche</span><span class="sxs-lookup"><span data-stu-id="9b6fc-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="9b6fc-105">Diese Eigenschaft sendet einen Befehl an das Gerät, um nach einer absoluten Nachverfolgung zu suchen (ATN).</span><span class="sxs-lookup"><span data-stu-id="9b6fc-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="9b6fc-106">Der UVC-Gerätetreiber unterstützt diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="9b6fc-107">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="9b6fc-107">Property Set GUID</span></span> | <span data-ttu-id="9b6fc-108">propseetid- \_ Ext- \_ Transport</span><span class="sxs-lookup"><span data-stu-id="9b6fc-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="9b6fc-109">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="9b6fc-109">Property ID</span></span>       | <span data-ttu-id="9b6fc-110">ksproperty \_ extxport- \_ Atn- \_ Suche</span><span class="sxs-lookup"><span data-stu-id="9b6fc-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="9b6fc-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9b6fc-111">Data Type</span></span>         | <span data-ttu-id="9b6fc-112">**Ksproperty \_ Extxport \_ S** -Struktur</span><span class="sxs-lookup"><span data-stu-id="9b6fc-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9b6fc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b6fc-113">Remarks</span></span>

<span data-ttu-id="9b6fc-114">Legen Sie den **dwabstracknumber** -Member der **ksproperty \_ extxport \_ S** -Struktur auf den folgenden Wert fest:</span><span class="sxs-lookup"><span data-stu-id="9b6fc-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="9b6fc-115">Die UVC-Spezifikation definiert nicht, wie das Gerät das Kontinuitäts Bit verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="9b6fc-116">Die Struktur von **ksproperty \_ extxport \_ S** wird im Windows-DDK beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b6fc-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b6fc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6fc-118">Eigenschaften Satz für externen Geräte Transport</span><span class="sxs-lookup"><span data-stu-id="9b6fc-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



