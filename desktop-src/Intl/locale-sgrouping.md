---
description: Gebiets Schema- \_ sgruppierung
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961007"
---
# <a name="locale_sgrouping"></a>Gebiets Schema- \_ sgruppierung

Größen für jede Gruppe von Ziffern auf der linken Seite des Dezimal Trennzeichens. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist zehn, einschließlich eines abschließenden NULL-Zeichens. Für jede Gruppe ist eine explizite Größe erforderlich, und die Größen werden durch Semikolons getrennt. Wenn der letzte Wert 0 ist, wird der vorangehende Wert wiederholt. Wenn Sie z. b. Tausende gruppieren möchten, geben Sie 3; 0 an. Indic-Gebiets Schemas gruppieren die ersten Tausender und Gruppieren dann nach Hunderten. Beispielsweise wird der Wert 12, 34, 56789 durch 3; 2; 0 dargestellt.

Weitere Beispiele:



| Spezifikation | Resultierende Zeichenfolge   |
|---------------|--------------------|
| 3; 0           | 3 Billionen  |
| 3; 2; 0         | 30, 00, 00, 00, 00000 |
| 3             | 3 Billionen     |
| 3; 2           | 30000000, 00000    |



 

 

 



