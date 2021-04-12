---
description: Beschreibt, wie Eingabe Bereiche für die Erkennung verwendet werden.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Eingabe Bereiche und Faktoide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218374"
---
# <a name="input-scopes-and-factoids"></a>Eingabe Bereiche und Faktoide

Ein Eingabebereich ist ein definierter Satz von Wörtern, Ziffern, Interpunktions Zeichen und syntaktischen Sortierungen, die innerhalb eines bestimmten Sprach Modells zulässig sind. Eingabe Bereiche können von Anwendungen verwendet werden, um das Sprachmodell, das von der Erkennung verwendet wird, auf einen bestimmten Kontext einzuschränken. Ein Eingabebereich von is \_ Email \_ smtpeer MailAddress wirkt sich beispielsweise auf die Erkennungsergebnisse aus, indem angegeben wird, dass ein bestimmtes Feld eine e-Mail-Adresse ist. Daher enthält das Feld wahrscheinlich Zeichen wie z. b. " @" and " \_ " und darf keine Zeichen wie " \* " und Leerzeichen enthalten.

> [!Note]  
> Andere Microsoft-Technologien verwenden auch Eingabe Bereiche. Dieser Artikel konzentriert sich auf die Verwendung des Kontexts zur Verbesserung der Genauigkeit von Handschrift Erkennungs Modulen für Tablet PC-Anwendungen.

 

In früheren Versionen der Tablet PC-Technologie-API wurden Faktoide verwendet, um Kontext zu definieren. Aus praktischen Gründen ist ein Faktoid das gleiche wie ein Eingabebereich. Version eine der Tablet PC SDK-Plattform hat eine Reihe von Faktoid-Werten im [**Faktoid**](factoid-constants.md) -Objekt definiert. Diese Werte wurden zum Festlegen von Kontext-und Einfluss Erkennungs Ergebnissen verwendet, wenn das [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt für die Erkennung verwendet wird. Für Erkennungs Modul von lateinischen Skripts ab Windows XP Tablet PC Edition 2005 verwenden Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " des " **erkennzercontext** "-Objekts, um Kontext festzulegen. Sie sollten jedoch einen Eingabebereich, eine Ausdrucks Liste oder einen regulären Ausdruckswert für die Handschrift anstelle eines der versionsfaktoidwerte übergeben. Die Microsoft-Erkennungs Modul für ostasiatische Zeichen unterstützen nicht die Verwendung der Enumerationswerte für den Eingabebereich. Sie sollten weiterhin Faktoid-Werte für erkennererkennerzeichen verwenden.

Eingabe Bereiche und Faktoide sind Einschränkungen bei den Alternativen auf Wort Ebene; die Zeichen Alternativen können sich außerhalb des angegebenen Eingabe Bereichs befinden, auch wenn das **coerce** -Flag festgelegt ist.

Wenn das **coerce** -Flag mit einer restriktiven Faktoid festgelegt wird, kann es vorkommen, dass die Erkennung keine Antwort erzeugt, die beide mit dem frei Handzeichen übereinstimmt und das Faktoid erfüllt. Ein anderes Szenario, in dem die Erkennung möglicherweise keine zufriedenstellende Antwort erzeugt, ist, wenn die Sprache der Erkennung nicht mit der Sprache der frei Hand Eingabe (z. b. der US-englischen Erkennung und chinesischen frei Handzeichen) identisch ist.

Wenn die Handschrifterkennung die frei Hand Eingabe für ein bestimmtes Wort oder Zeichen nicht erkennt, kann Sie entweder eine leere Alternative Liste oder eine Alternative Liste zurückgeben, in der die erste Auswahl Code Punkt 0xFFFF (nicht definiertes Zeichen) ist. Dies ist besonders nützlich in den Eingabemodi für die einführenden Führungslinien, in denen jede Box mit Ink eine nicht leere Liste von alternativen aufweisen soll. Die Anwendung kann dann dieses undefinierte Zeichen in beliebiger Weise anzeigen (z. b. als "???").

> [!Note]  
> Die Faktoid-Werte funktionieren weiterhin mit erkenzern von lateinischen Skripts aus Gründen der Abwärtskompatibilität.

 

Weitere Informationen zu Faktoids finden Sie unter [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).

Informationen zu ostasiatischen Faktoiden finden Sie [unter Unterstützte Faktoide aus Version 1](supported-factoids-from-version-1.md).

 

 



