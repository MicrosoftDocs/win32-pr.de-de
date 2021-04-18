---
description: Dieses Attribut gibt an, ob das angegebene Steuerelement aktiviert oder deaktiviert ist. Die meisten Steuerelemente werden bei deaktiviertem grau angezeigt.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Aktiviertes Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347878"
---
# <a name="enabled-control-attribute"></a>Aktiviertes Steuerelement Attribut

Dieses Attribut gibt an, ob das angegebene Steuerelement aktiviert oder deaktiviert ist. Die meisten Steuerelemente werden bei deaktiviertem grau angezeigt.

Wenn dieses Bit festgelegt ist, wird das Steuerelement als aktiviert erstellt.

Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement als deaktiviert erstellt.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle-Steuerelemente. Die Darstellung einiger Steuerelemente, die keiner Eigenschaft zugeordnet sind, wie z. b. Bitmaps und Symbole, ist nicht durch Festlegen dieses Attributs beeinträchtigt.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbcontrolattributesaktivierte** |



 

## <a name="remarks"></a>Bemerkungen

Sie können auch die [Tabelle "ControlCondition](controlcondition-table.md) " verwenden, um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung zu deaktivieren oder zu aktivieren.

Sie können ein Steuerelement auch aktivieren oder deaktivieren, indem Sie das Steuerelement mit einem [ControlEvent](control-events.md)abonnieren. Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner des Ereignisses in der Spalte Ereignis der [Tabelle EventMapping](eventmapping-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



