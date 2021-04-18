---
description: Ein &\# 0034;-Zeichensatz&\# 0034; ist eine Zuordnung von Zeichen zu ihren identifizierenden Codewerten.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347744"
---
# <a name="character-sets"></a>Zeichensätze

Ein "Zeichensatz" ist eine Zuordnung von Zeichen zu ihren identifizierenden Codewerten. Der Zeichensatz, der am häufigsten in Computern verwendet wird, ist [Unicode](unicode.md), ein globaler Standard für die Zeichencodierung. Intern verwenden Windows-Anwendungen die UTF-16-Implementierung von Unicode. In UTF-16 werden die meisten Zeichen durch zwei Byte-Codes identifiziert. Die weniger häufig verwendeten ergänzenden Zeichen werden jeweils durch ein Ersatz Zeichenpaar dargestellt, das ein paar von 2-Byte-Codes ist. Weitere Informationen finden Sie unter [Surrogates und ergänzende Zeichen](surrogates-and-supplementary-characters.md).

Einige Windows-Anwendungen müssen mit den älteren Zeichensätzen arbeiten, die für Windows Me/98/95 einheitlich sind. [Windows-Codepages](code-pages.md) ermöglichen es Ihrer Anwendung, mit diesen Zeichensätzen zu arbeiten. Diese Zeichensätze können in Folgendes unterteilt werden:

-   [Einzel Byte-Zeichensätze](single-byte-character-sets.md) (SBCS). In einer SBCS wird jedes Zeichen durch einen Wert von einem Byte breit identifiziert.
-   Multibyte-Zeichensätze, insbesondere die [Doppelbyte-Zeichensätze](double-byte-character-sets.md) (DBCS). Multibyte-Zeichensätze bieten eine Möglichkeit, die große Anzahl von Zeichen in vielen asiatischen Sprachen darzustellen.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Codepages](code-pages.md)
-   [Doppelbyte-Zeichensätze](double-byte-character-sets.md)
-   [Einzel Byte-Zeichensätze](single-byte-character-sets.md)
-   [Surrogate und ergänzende Zeichen](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Unicode und Zeichensätzen](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



