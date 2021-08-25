---
description: Wenn dieses Bit festgelegt ist, werden die Bilder im Dialogfeld mit der benutzerdefinierten Palette erstellt (eine pro Dialog, die vom ersten erstellten Steuerelement empfangen wurde). Wenn das Bit nicht festgelegt ist, werden die Bilder mithilfe einer Standardpalette gerendert.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: UseCustomPalette Dialog Style Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9863f9b20ad85caf3712c3cfa00fd88de72f82b947a329d367d06f02ba06163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809480"
---
# <a name="usecustompalette-dialog-style-bit"></a>UseCustomPalette Dialog Style Bit

Wenn dieses Bit festgelegt ist, werden die Bilder im Dialogfeld mit der benutzerdefinierten Palette erstellt (eine pro Dialog, die vom ersten erstellten Steuerelement empfangen wurde). Wenn das Bit nicht festgelegt ist, werden die Bilder mithilfe einer Standardpalette gerendert.

In der Regel wird dieses Bit festgelegt, wenn der Dialog ein Bild mit einer speziellen Palette oder mehrere Bilder enthält, die eine benutzerdefinierte Palette gemeinsam nutzen. Das Bit sollte nicht festgelegt werden, wenn das Dialogfeld mehrere Bilder mit unterschiedlichen Paletten enthält. In diesem Fall führt die Standardpalette höchstwahrscheinlich zu einem zufriedenstellenden Ergebnis für alle Bilder.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



