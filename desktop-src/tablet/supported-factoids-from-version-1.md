---
description: Die Tablet PC-Plattform unterstützt eine Reihe von Faktoiden, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Unterstützte Faktoide aus Version 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357079"
---
# <a name="supported-factoids-from-version-1"></a>Unterstützte Faktoide aus Version 1

\[Beachten Sie, dass die folgende Beschreibung der in Version 1 des Microsoft Windows XP Tablet PC Edition-SDK (Software Development Kit) unterstützten Faktoids weiterhin von Erkennungs Programmen unterstützt wird. es wird jedoch empfohlen, dass für alle neuen Entwicklungen (für erkenungen von lateinischen Skripts) die in der [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration definierten Werte verwendet werden.\]

Die Tablet PC-Plattform unterstützt eine Reihe von Faktoiden, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen. Bei der Verwendung von Faktoiden ist es wichtig, dass die erwartete Eingabe genau mit der Definition von "Faktoid" übereinstimmt. Wenn die Eingabe nicht mit der Definition des Faktoid identisch ist, leidet die Erkennungsgenauigkeit. Wenn beispielsweise die **Zahl** "Faktoid" festgelegt ist und der Benutzer Buchstaben eingibt, ist die Erkennungsgenauigkeit für Buchstaben unzureichend.

Bestimmte Faktoide, z. b. **e-Mail** und **Ziffern**, sind fast identisch in den Sprachen. Andere Faktoide, z. b. **Telefon** -und **PostalCode**, variieren je nach Sprache. Überprüfen Sie das Format der einzelnen Faktoid für die verwendete Sprache. Eine Liste der Formate für jedes Faktoid in jeder Sprache finden Sie in den Tabellen in den Themen in diesem Thema.

> [!Note]  
> Es gibt einen geringfügigen, aber wichtigen Unterschied zwischen den Faktoiden für westliche Sprachen und den Faktoiden für ostasiatische Sprachen. Faktoide für westliche Sprachen werden mithilfe von Ausdrücken implementiert, die das gewünschte Ergebnis beschreiben. Die Erkennung wird dann so verzerrt, dass Ergebnisse erzeugt werden, die diesem Ausdruck entsprechen. Faktoide für ostasiatische Sprachen werden implementiert, indem ein akzeptabler Bereich von Unicode-Zeichen angegeben wird. Beispielsweise akzeptiert das **Date** -Faktoid für ostasiatische Sprachen nur Unicode-Zeichen innerhalb eines bestimmten Bereichs.

 

Zu den Faktoiden für westliche Sprachen zählen u. a. Faktoide für Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch. Zu den Faktoiden für ostasiatische Sprachen zählen Faktoide für Chinesisch (vereinfacht), Chinesisch (traditionell), Japanisch und Koreanisch.

In den folgenden Abschnitten sind die Formate aufgeführt, die für jedes Faktoid in jeder Sprache unterstützt werden:

-   [Sprachen übergreifende Facetten übergreifende Faktoide](factoids-common-across-languages.md)
-   [Faktoide für westliche Sprachen](factoids-for-western-languages.md)
-   [Faktoide für ostasiatische Sprachen](factoids-for-east-asian-languages.md)

Wenn Sie davon ausgehen, dass es sich um Eingaben handelt, die sich von den in den Tabellen in diesen Abschnitten aufgeführten Formaten unterscheiden, verwenden Sie kein Faktoid. Außerdem sind die Faktoide in die Erkennung der einzelnen Sprachen integriert. Sie können keine Faktoide in einer Sprache verwenden, die eine Erkennung einer anderen Sprache hat. Beispielsweise können Sie das französische **Telefon** -Faktoid nicht mit einer japanischen Erkennungsfunktion verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Faktoid-Konstanten**](factoid-constants.md)
</dt> <dt>

[Microsoft. Ink. Factoid-Klasse](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
