---
description: Gebiets Schema- \_ smon- \* Konstanten
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: LOCALE_SMON *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343776"
---
# <a name="locale_smon-constants"></a>Gebiets Schema- \_ smon- \* Konstanten

In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema-smon- \* Konstanten zum Darstellen von Währungswerten definiert.



| Wert                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Gebiets Schema smondecimalsep  | Als zimales Dezimaltrennzeichen verwendete Zeichen. Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist vier, einschließlich eines abschließenden NULL-Zeichens. Wenn z. b. ein Währungsbetrag als "$3,40" angezeigt wird, so wie "drei Dollar und 40 Cent" im USA angezeigt wird, ist das Dezimaltrennzeichen ".".                                                                                                                                             |
| Gebiets Schema- \_ smongruppierung    | Größen für jede Gruppe von monetären Ziffern links vom Dezimaltrennzeichen. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist zehn, einschließlich eines abschließenden NULL-Zeichens. Für jede Gruppe ist eine explizite Größe erforderlich, und die Größen werden durch Semikolons getrennt. Wenn der letzte Wert 0 ist, wird der vorangehende Wert wiederholt. Wenn Sie z. b. Tausende gruppieren möchten, geben Sie 3; 0 an. Indic-Sprachen gruppieren die ersten tausend und Gruppieren dann nach Hunderten. Beispielsweise ist der Wert 12, 34, 56789 durch 3; 2; 0 (null) dargestellt. |
| \_Gebiets Schema smontausendandsep | Zeichen, die als Währungs Trennzeichen zwischen Ziffern Gruppen Links vom Dezimaltrennzeichen verwendet werden. Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist vier, einschließlich eines abschließenden NULL-Zeichens. In der Regel stellen die Gruppen Tausende dar. Abhängig von dem für locale \_ smongruppierung angegebenen Wert können Sie jedoch etwas anderes darstellen.                                                                                                                                 |



 

 

 



