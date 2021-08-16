---
description: Durch Festlegen der Factoid-Eigenschaft auf None erkennt die Zeichenerkennung handschriftliche Zeichen.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Wort- und Zeichenerkennung im Vergleich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e704943afb2b411441752056aace0889e87483fc4992d59c39ea6a135ef76b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966599"
---
# <a name="word-vs-character-recognition"></a>Wort- und Zeichenerkennung im Vergleich

Durch Festlegen der [Factoid-Eigenschaft](/previous-versions/ms835848(v=msdn.10)) auf **None** erkennt die Zeichenerkennung handschriftliche Zeichen.

Die [RecoTimeout -Eigenschaft](/previous-versions/ms835852(v=msdn.10)) [**(RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) gibt die Anzahl [](/previous-versions/ms552692(v=vs.100)) der Millisekunden der Verzögerung zwischen dem letzten Strich und dem Ende der Handschrifteingabe an. Sie können diesen Wert erhöhen, um Text zu erkennen, bevor ganze Wörter oder Sätze geschrieben werden. Sie können die Erkennung von Ink auch sofort erzwingen, indem Sie die [Recognize-Methode](/previous-versions/ms836275(v=msdn.10)) verwenden.

 

 
