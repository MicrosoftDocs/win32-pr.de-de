---
description: Ein &\# 0034;Zeichensatz&\# 0034; ist eine Zuordnung von Zeichen zu ihren identifizierenden Codewerten.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f9bb57dad6924e2bbc9390d7315dbed0c59647cacefb932d7055ea8fdd3385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898800"
---
# <a name="character-sets"></a>Zeichensätze

Ein "Zeichensatz" ist eine Zuordnung von Zeichen zu ihren identifizierenden Codewerten. Der Zeichensatz, der heute am häufigsten auf Computern verwendet wird, ist [Unicode,](unicode.md)ein globaler Standard für die Zeichencodierung. Intern verwenden Windows Anwendungen die UTF-16-Implementierung von Unicode. In UTF-16 werden die meisten Zeichen durch Zwei-Byte-Codes identifiziert. Die weniger häufig verwendeten ergänzenden Zeichen werden jeweils durch ein Ersatzzeichenpaar dargestellt, bei dem es sich um ein Paar von Zwei-Byte-Codes handelt. Weitere Informationen finden Sie unter [Ersatzzeichen und ergänzende Zeichen.](surrogates-and-supplementary-characters.md)

Einige Windows Anwendungen müssen mit den älteren Zeichensätzen arbeiten, die für Windows Me/98/95 nativ sind. [Windows Codepages](code-pages.md) ermöglichen es Ihrer Anwendung, mit diesen Zeichensätzen zu arbeiten. Diese Zeichensätze können in Folgendes unterteilt werden:

-   [Einzel byte-Zeichensätze (Single-Byte Character Sets,](single-byte-character-sets.md) SBCS). In einem SBCS wird jedes Zeichen durch einen Wert von einem Byte breit identifiziert.
-   Multibyte-Zeichensätze, insbesondere [die Doppelbyte-Zeichensätze (Double-Byte Character Sets,](double-byte-character-sets.md) DBCS). Multibyte-Zeichensätze bieten eine Möglichkeit, die große Anzahl von Zeichen in vielen asienischen Sprachen darzustellen.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Codepages](code-pages.md)
-   [Doppel-Byte-Zeichensätze](double-byte-character-sets.md)
-   [Einzel byte-Zeichensätze](single-byte-character-sets.md)
-   [Surrogate und ergänzende Zeichen](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Unicode und Zeichensätzen](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



