---
description: Wenn dieses Bit festgelegt ist, wird das Steuerelement mit einem abgesenkten dreidimensionalen Aussehen angezeigt.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Einsenken-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3547f06d82a66a08a575958eac728051c3315f3382529065c3792cfdb94def
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626930"
---
# <a name="sunken-control-attribute"></a>Einsenken-Steuerelementattribut

Wenn dieses Bit festgelegt ist, wird das Steuerelement mit einem abgesenkten dreidimensionalen Aussehen angezeigt. Die Auswirkungen dieses Stilbits unterscheiden sich auf verschiedene Steuerelemente und Versionen von Windows. Bei einigen Steuerelementen hat dies keine sichtbaren Auswirkungen. Wenn das System das Sunken-Steuerelementattribut nicht unterstützt, wird das Steuerelement im standardmäßigen visuellen Stil angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement mit dem standardmäßigen visuellen Stil angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle Steuerelemente.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das Sunken-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle](control-table.md)ein.

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



