---
description: Der FORMSOF-Begriff führt Übereinstimmungen mit anderen linguistischen Formen des Worts aus.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF-Begriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863443"
---
# <a name="formsof-term"></a>FORMSOF-Begriff

Der FORMSOF-Begriff führt Übereinstimmungen mit anderen linguistischen Formen des Worts aus. Im Folgenden finden Sie die FORMSOF-Begriffssyntax:


```
FORMSOF (<generation_type>,<match_words>)
```



Der Generierungstyp gibt an, wie Microsoft Windows Search die alternativen Wortformen auswählt. Der **WERT INFLECTIONAL** wählt alternative Inflectionformen für die Übereinstimmungswörter aus. Wenn das Wort ein Verb ist, werden alternative Tenses verwendet. Wenn das Wort ein Nomen ist, werden die Singular-, Plural- und Possessivformen verwendet, um Übereinstimmungen zu erkennen.

Der Wert \_ der Übereinstimmungswörter ist mindestens ein Wort, getrennt durch Kommas.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird nach Inflectional-Übereinstimmungen für das Wort "run" gesucht. Dieses Beispiel entspricht Dokumenten, die "run", "running" oder "ran" enthalten.


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[FREETEXT-Prädikat](-search-sql-freetext.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



