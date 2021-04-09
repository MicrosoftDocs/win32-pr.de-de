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
# <a name="controlshowrollbackcost-control-attribute"></a>Controlshowrollbackcost-Steuerungs Attribut

Dieses Attribut gibt an, ob die Rollback-Sicherungsdateien in die vom [volumecostlist-Steuer](volumecostlist-control.md)Element angezeigten Kosten eingeschlossen werden.

Wenn dieses Bit festgelegt ist und die [**promptrollbackcost**](promptrollbackcost.md) -Eigenschaft = P ist, werden die Rollback-Sicherungsdateien in die Kosten eingeschlossen, die vom [volumecostlist-Steuer](volumecostlist-control.md)Element angezeigt werden.

Wenn dieses Bit nicht festgelegt ist und die [**promptrollbackcost**](promptrollbackcost.md) -Eigenschaft = P ist, werden die Rollback-Sicherungsdateien nicht in den Kosten berücksichtigt, die vom [volumecostlist-Steuer](volumecostlist-control.md)Element angezeigt werden.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Volumecostlist](volumecostlist-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbcontrolshowrollbackcost** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement Attribut wird ignoriert, wenn [**promptrollbackcost**](promptrollbackcost.md) = D oder F ist.

Wenn [**promptrollbackcost**](promptrollbackcost.md) = F, werden die Kosten des Rollbacks, Sicherungsdateien, eingeschlossen.

Wenn [**promptrollbackcost**](promptrollbackcost.md) = D oder [**DISABLEROLLBACK**](-disablerollback.md) Eigenschaft = 1, sind die Kosten für das Rollback und die Sicherungsdateien nicht enthalten.

 

 



