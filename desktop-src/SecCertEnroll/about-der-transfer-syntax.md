---
description: Das Anwenden einer Codierungs Regel auf die Datenstrukturen, die durch eine abstrakte Syntax beschrieben werden, bietet eine Übertragungs Syntax, die festlegt, wie Bytes in einem Stream beim Senden zwischen Computern organisiert werden.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: DER-Übertragungs Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569479"
---
# <a name="der-transfer-syntax"></a>DER-Übertragungs Syntax

Das Anwenden einer Codierungs Regel auf die Datenstrukturen, die durch eine abstrakte Syntax beschrieben werden, bietet eine Übertragungs Syntax, die festlegt, wie Bytes in einem Stream beim Senden zwischen Computern organisiert werden. Die von Distinguished Encoding Rules verwendete Übertragungs Syntax folgt immer einem *Tag, einer Länge und einem Wert* Format. Das Format wird in der Regel als TLV-dreier bezeichnet, in dem jedes Feld (T, L oder V) mindestens ein Byte enthält.

![der Typ, Länge und Wert (TLV)-dreier](images/der-tlv-basic.png)

Das *Tagfeld* gibt den Typ der zu sendenden Datenstruktur an, das *Längen* Feld gibt die Anzahl der Bytes an Inhalt an, die übertragen werden, und das *Wertfeld* enthält den Inhalt. Beachten Sie, dass das *Wertfeld* ein Dreier sein kann, wenn es einen konstruierten Datentyp enthält, wie in der folgenden Abbildung dargestellt.

![der-TLV-replerekursion](images/der-tlv-recursive.png)

In den folgenden Themen finden Sie ausführliche Informationen zu den Komponenten eines TLV-Dreiecks.

-   [Codierte tagbytes](about-encoded-tag-bytes.md)
-   [Codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstruierte Typen](about-constructed-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 



