---
description: Wenn dieses Bit festgelegt ist, werden die Bilder im Dialogfeld mit der benutzerdefinierten Palette erstellt (eine pro Dialogfeld, die vom ersten erstellten Steuerelement empfangen wurde). Wenn das-Bit nicht festgelegt ist, werden die Bilder mithilfe einer Standardpalette gerendert.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Usecustompalette-Dialog Feld-Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350955"
---
# <a name="usecustompalette-dialog-style-bit"></a>Usecustompalette-Dialog Feld-Stilbit

Wenn dieses Bit festgelegt ist, werden die Bilder im Dialogfeld mit der benutzerdefinierten Palette erstellt (eine pro Dialogfeld, die vom ersten erstellten Steuerelement empfangen wurde). Wenn das-Bit nicht festgelegt ist, werden die Bilder mithilfe einer Standardpalette gerendert.

In der Regel wird dieses Bit festgelegt, wenn das Dialogfeld ein Bild mit einer speziellen Palette enthält, oder wenn mehrere Bilder eine benutzerdefinierte Palette gemeinsam nutzen. Das Bit sollte nicht festgelegt werden, wenn das Dialogfeld mehrere Bilder mit unterschiedlichen Paletten enthält. In diesem Fall wird mit der Standardpalette höchstwahrscheinlich ein zufriedenstellendes Ergebnis für alle Bilder angezeigt.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbdialogattributesusecustompalette** |



 

 

 



