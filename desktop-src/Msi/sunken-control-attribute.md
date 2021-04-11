---
description: Wenn dieses Bit festgelegt ist, wird das Steuerelement mit einem abgesenkten, dreidimensionalen Erscheinungsbild angezeigt.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Senktes Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130273"
---
# <a name="sunken-control-attribute"></a>Senktes Steuerungs Attribut

Wenn dieses Bit festgelegt ist, wird das Steuerelement mit einem abgesenkten, dreidimensionalen Erscheinungsbild angezeigt. Die Auswirkung dieses stilbits unterscheidet sich in verschiedenen Steuerelementen und Versionen von Windows. Bei manchen Steuerelementen hat Sie keinen sichtbaren Effekt. Wenn das System das senkensteuerelement-Attribut nicht unterstützt, wird das Steuerelement im visuellen Standardstil angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement mit dem visuellen Standardstil angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle-Steuerelemente.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbcontrolattributess Unken** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das abgesenkten Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



