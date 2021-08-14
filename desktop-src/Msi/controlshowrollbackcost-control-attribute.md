---
description: Dieses Attribut gibt an, ob die Rollbacksicherungsdateien in den Kosten enthalten sind, die vom VolumeCostList-Steuerelement angezeigt werden.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: ControlShowRollbackCost-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a888df328062a81637b36dc3fcfbe178d6e49bd4aee01c65b2d2e3524fb321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379925"
---
# <a name="controlshowrollbackcost-control-attribute"></a>ControlShowRollbackCost-Steuerelementattribut

Dieses Attribut gibt an, ob die Rollbacksicherungsdateien in den Kosten enthalten sind, die vom [VolumeCostList-Steuerelement](volumecostlist-control.md)angezeigt werden.

Wenn dieses Bit festgelegt ist und die [**PROMPTROLLBACKCOST-Eigenschaft**](promptrollbackcost.md) = P ist, sind die Rollbacksicherungsdateien in den Kosten enthalten, die vom [VolumeCostList-Steuerelement](volumecostlist-control.md)angezeigt werden.

Wenn dieses Bit nicht festgelegt ist und [**die PROMPTROLLBACKCOST-Eigenschaft**](promptrollbackcost.md) = P ist, sind die Rollbacksicherungsdateien nicht in den Kosten enthalten, die vom [VolumeCostList-Steuerelement](volumecostlist-control.md)angezeigt werden.

## <a name="valid-controls"></a>Gültige Steuerelemente

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelementattribut wird ignoriert, wenn [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D oder F.

Wenn [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, die Kosten des Rollbacks, Sicherungsdateien enthalten sind.

Wenn [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D oder [**die DISABLEROLLBACK-Eigenschaft**](-disablerollback.md) = 1 ist, sind die Kosten für das Rollback, Sicherungsdateien nicht enthalten.

 

 



