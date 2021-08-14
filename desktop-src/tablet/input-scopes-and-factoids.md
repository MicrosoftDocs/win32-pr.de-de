---
description: Beschreibt, wie Eingabebereiche für die Erkennung verwendet werden.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Eingabebereiche und Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881ebd26cbfb70cb215103b9a6face356af078e47b74a2e9140886f81f457eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450970"
---
# <a name="input-scopes-and-factoids"></a>Eingabebereiche und Factoids

Ein Eingabebereich ist ein definierter Satz von Wörtern, Zahlen, Satzzeichen und syntaktischen Sortierungen, die innerhalb eines bestimmten Sprachmodells zulässig sind. Eingabebereiche können von Anwendungen verwendet werden, um das von der Erkennung verwendete Sprachmodell auf einen bestimmten Kontext zu beschränken. Beispielsweise beeinflusst ein Eingabebereich von IS \_ EMAIL \_ SMTPEMAILADDRESS die Erkennungsergebnisse, indem angegeben wird, dass ein bestimmtes Feld eine E-Mail-Adresse ist. Daher enthält das Feld wahrscheinlich Zeichen wie " @" and " \_ " und darf keine Zeichen wie " \* " und Leerzeichen enthalten.

> [!Note]  
> Andere Microsoft-Technologien verwenden auch Eingabebereiche. Dieser Artikel konzentriert sich auf die Verwendung von Kontext zur Verbesserung der Genauigkeit von Handschrifterkennungs-Engines für Tablet PC-Anwendungen.

 

Frühere Versionen der Api für die Tablet PC-Technologie verwendeten Factoids, um den Kontext zu definieren. Aus praktischen Gründen ist ein Factoid dasselbe wie ein Eingabebereich. Version 1 der Tablet PC SDK-Plattform hat einen Satz von Factoidwerten im [**Factoid-Objekt**](factoid-constants.md) definiert. Diese Werte wurden verwendet, um Kontext festzulegen und die Erkennungsergebnisse zu beeinflussen, wenn das [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) für die Erkennung verwendet wird. Für Erkennungen von lateinischen Skripts, die mit Windows XP Tablet PC Edition 2005 beginnen, verwenden Sie weiterhin die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) des **RecognizerContext-Objekts,** um den Kontext festzulegen. Sie sollten jedoch einen Eingabebereich, eine Ausdrucksliste oder einen Handschriftwert für reguläre Ausdrücke anstelle eines der Factoidwerte der Version eins übergeben. Die Microsoft-Erkennungen ostasiatischer Zeichen unterstützen die Verwendung der aufzählten Werte des Eingabebereichs nicht. Sie sollten weiterhin Faktenwerte für Erkennungen ostasiatischer Zeichen verwenden.

Eingabebereiche und Factoids sind Einschränkungen für die Alternativen auf Wortebene. die Zeichenwechsel können sich außerhalb des angegebenen Eingabebereichs befindet, auch wenn das **COERCE-Flag** festgelegt ist.

Wenn das **COERCE-Flag** mit einem restriktiven Factoid festgelegt wird, kann es vorkommen, dass die Erkennung keine Antwort erzeugen kann, die sowohl mit der Freihand als auch mit dem Factoid übereinstimmt. Ein weiteres Szenario, in dem die Erkennung möglicherweise keine zufriedenstellende Antwort erzeugt, ist, wenn die Sprache der Erkennung nicht mit der Sprache der Ink übereinstimmt (z. B. die US-englische Erkennung und chinesische Ink-Zeichen).

Wenn die Handschrifterkennung die Freihand für ein bestimmtes Wort oder Zeichen nicht erkennen kann, kann sie entweder eine leere alternative Liste oder eine alternative Liste zurückgeben, in der die erste Wahl code point 0xffff (undefiniertes Zeichen) ist. Dies ist besonders nützlich in geschachtelten Eingabemodi, bei denen für jedes Feld mit Freihandeingaben eine nicht leere Liste alternativer Methoden erwartet wird. Die Anwendung kann dieses nicht definierte Zeichen dann auf beliebige Weise anzeigen (z. B. als "???").

> [!Note]  
> Die Factoidwerte funktionieren aus Gründen der Abwärtskompatibilität weiterhin mit Erkennungen des lateinischen Skripts.

 

Weitere Informationen zu Factoiden finden Sie unter [Festlegen des Kontexts für Ink-Enabled-Steuerelemente.](setting-context-for-ink-enabled-controls.md)

Informationen zu ostasiatischen Factoiden finden Sie unter [Supported Factoids from Version 1 (Unterstützte Factoids aus Version 1).](supported-factoids-from-version-1.md)

 

 



