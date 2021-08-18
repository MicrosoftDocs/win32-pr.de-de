---
description: '\_LOCALE-SGROUPING'
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476fa80a22e55791ca7b5636237540c457480ff0bd9c808b99ef3c6e46a17dce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106210"
---
# <a name="locale_sgrouping"></a>\_LOCALE-SGROUPING

Größen für jede Gruppe von Ziffern links vom Dezimaltrennzeichen. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, beträgt zehn, einschließlich eines beendenden NULL-Zeichens. Für jede Gruppe ist eine explizite Größe erforderlich, und die Größen werden durch Semikolons getrennt. Wenn der letzte Wert 0 ist, wird der vorherige Wert wiederholt. Um beispielsweise Tausende zu gruppen, geben Sie 3;0 an. Indic locales gruppiert den ersten Tausender und dann nach Hunderten. Beispielsweise wird 12.34.56.789 durch 3;2;0 dargestellt.

Weitere Beispiele:



| Spezifikation | Resultierende Zeichenfolge   |
|---------------|--------------------|
| 3;0           | 3,000,000,000,000  |
| 3;2;0         | 30,00,00,00,00,000 |
| 3             | 3000000000,000     |
| 3;2           | 30000000,00,000    |



 

 

 



