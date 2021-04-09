---
description: Dieses Attribut gibt an, ob die Rollback-Sicherungsdateien in die vom volumecostlist-Steuerelement angezeigten Kosten eingeschlossen werden.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Controlshowrollbackcost-Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867296"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="5f453-103">Controlshowrollbackcost-Steuerungs Attribut</span><span class="sxs-lookup"><span data-stu-id="5f453-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="5f453-104">Dieses Attribut gibt an, ob die Rollback-Sicherungsdateien in die vom [volumecostlist-Steuer](volumecostlist-control.md)Element angezeigten Kosten eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5f453-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="5f453-105">Wenn dieses Bit festgelegt ist und die [**promptrollbackcost**](promptrollbackcost.md) -Eigenschaft = P ist, werden die Rollback-Sicherungsdateien in die Kosten eingeschlossen, die vom [volumecostlist-Steuer](volumecostlist-control.md)Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5f453-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="5f453-106">Wenn dieses Bit nicht festgelegt ist und die [**promptrollbackcost**](promptrollbackcost.md) -Eigenschaft = P ist, werden die Rollback-Sicherungsdateien nicht in den Kosten berücksichtigt, die vom [volumecostlist-Steuer](volumecostlist-control.md)Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5f453-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="5f453-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5f453-107">Valid Controls</span></span>

[<span data-ttu-id="5f453-108">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="5f453-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="5f453-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5f453-109">Value</span></span>



| <span data-ttu-id="5f453-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="5f453-110">Decimal</span></span> | <span data-ttu-id="5f453-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="5f453-111">Hexadecimal</span></span> | <span data-ttu-id="5f453-112">Konstante</span><span class="sxs-lookup"><span data-stu-id="5f453-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="5f453-113">4194304</span><span class="sxs-lookup"><span data-stu-id="5f453-113">4194304</span></span> | <span data-ttu-id="5f453-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="5f453-114">0x00400000</span></span>  | <span data-ttu-id="5f453-115">**msidbcontrolshowrollbackcost**</span><span class="sxs-lookup"><span data-stu-id="5f453-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5f453-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f453-116">Remarks</span></span>

<span data-ttu-id="5f453-117">Dieses Steuerelement Attribut wird ignoriert, wenn [**promptrollbackcost**](promptrollbackcost.md) = D oder F ist.</span><span class="sxs-lookup"><span data-stu-id="5f453-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="5f453-118">Wenn [**promptrollbackcost**](promptrollbackcost.md) = F, werden die Kosten des Rollbacks, Sicherungsdateien, eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5f453-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="5f453-119">Wenn [**promptrollbackcost**](promptrollbackcost.md) = D oder [**DISABLEROLLBACK**](-disablerollback.md) Eigenschaft = 1, sind die Kosten für das Rollback und die Sicherungsdateien nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f453-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



