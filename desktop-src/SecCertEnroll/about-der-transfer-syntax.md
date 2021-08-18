---
description: Das Anwenden einer Codierungsregel auf die von einer abstrakten Syntax beschriebenen Datenstrukturen stellt eine Übertragungssyntax bereit, die steuert, wie Bytes in einem Stream organisiert werden, wenn sie zwischen Computern gesendet werden.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: DER-Übertragungssyntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6757a22743a2c44abb5ef4c46154a08e425e2b1b7045beaacc7fb4f4f206fed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904517"
---
# <a name="der-transfer-syntax"></a>DER-Übertragungssyntax

Das Anwenden einer Codierungsregel auf die von einer abstrakten Syntax beschriebenen Datenstrukturen stellt eine Übertragungssyntax bereit, die steuert, wie Bytes in einem Stream organisiert werden, wenn sie zwischen Computern gesendet werden. Die von Distinguished Encoding Rules verwendete Übertragungssyntax folgt immer dem Format *Tag, Länge und Wert.* Das Format wird in der Regel als TLV-Triplet bezeichnet, in dem jedes Feld (T, L oder V) ein oder mehrere Bytes enthält.

![der type, length und value (tlv) triplet](images/der-tlv-basic.png)

Das Feld *Tag* gibt den Typ der datenstruktur an, die gesendet wird, das *Feld Length* gibt die Anzahl der übertragenen Bytes an, und das Feld *Wert* enthält den Inhalt. Beachten Sie, dass das Feld *Wert* ein Triplet sein kann, wenn es einen konstruierten Datentyp enthält, wie in der folgenden Abbildung dargestellt.

![der tlv triplet recursion](images/der-tlv-recursive.png)

Ausführliche Informationen zu den Komponenten eines TLV-Triplets finden Sie in den folgenden Themen.

-   [Codierte Tagbytes](about-encoded-tag-bytes.md)
-   [Codierte Länge und Wertbytes](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstruierte Typen](about-constructed-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 



