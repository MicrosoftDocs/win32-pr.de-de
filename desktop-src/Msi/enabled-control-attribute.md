---
description: Dieses Attribut gibt an, ob das bestimmte Steuerelement aktiviert oder deaktiviert ist. Die meisten Steuerelemente werden grau angezeigt, wenn sie deaktiviert sind.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Aktiviertes Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40de14ac0205c52cce46c6050de0282e62df90d50f3bcdeb576771c9107ffc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763920"
---
# <a name="enabled-control-attribute"></a>Aktiviertes Steuerelementattribut

Dieses Attribut gibt an, ob das bestimmte Steuerelement aktiviert oder deaktiviert ist. Die meisten Steuerelemente werden grau angezeigt, wenn sie deaktiviert sind.

Wenn dieses Bit festgelegt ist, wird das Steuerelement als aktiviert erstellt.

Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement als deaktiviert erstellt.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle Steuerelemente. Die Darstellung einiger Steuerelemente, die nicht einer Eigenschaft zugeordnet sind, z. B. Bitmaps und Symbole, ist durch das Festlegen dieses Attributs nicht betroffen.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Hinweise

Sie können auch die [ControlCondition-Tabelle](controlcondition-table.md) verwenden, um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder bedingungsbedingten Anweisung zu deaktivieren oder zu aktivieren.

Sie können ein Steuerelement auch aktivieren oder deaktivieren, indem Sie das Steuerelement einem [ControlEvent abonnieren.](control-events.md) Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner des Ereignisses in die Spalte Ereignis der [EventMapping-Tabelle ein.](eventmapping-table.md)

Weitere [Informationen finden Sie unter Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter Steuerelemente erstellen [müssen.](controls.md)

 

 



