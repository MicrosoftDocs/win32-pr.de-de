---
description: Der FORMSOF-Begriff führt Übereinstimmungen mit anderen linguistischen Formen des Worts aus.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF-Begriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345015"
---
# <a name="formsof-term"></a>FORMSOF-Begriff

Der FORMSOF-Begriff führt Übereinstimmungen mit anderen linguistischen Formen des Worts aus. Im folgenden finden Sie die Begriffs Syntax für FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



Der generierungstyp gibt an, wie Microsoft Windows Search die alternativen Word-Formulare auswählt. Der Flexions Wert wählt Alternative Wende-Formulare für die **Übereinstimmungs** Wörter aus. Wenn das Wort ein Verb ist, werden alternative Mandanten verwendet. Wenn es sich bei dem Wort um ein Substantiv handelt, werden die Formen Singular, Plural und possessiv verwendet, um Übereinstimmungen zu erkennen.

Der \_ Wert für die Übereinstimmungs Wörter ist ein oder mehrere Wörter, die durch Kommas getrennt sind.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird nach Flexions Übereinstimmungen für das Wort "Run" gesucht. Dieses Beispiel entspricht Dokumenten, die "Run", "Running" oder "ran" enthalten.


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Frei Text Prädikat](-search-sql-freetext.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



