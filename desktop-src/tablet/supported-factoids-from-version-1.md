---
description: Die Tablet PC-Plattform unterstützt eine Reihe von Factoiden, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Unterstützte Factoids von Version 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c24c192bcbda04be7ea25deb0c7b1cb7b392de57c43ce7a509e0ceaac31002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934350"
---
# <a name="supported-factoids-from-version-1"></a>Unterstützte Factoids von Version 1

\[Beachten Sie die folgende Beschreibung der Factoids, die in Version 1 des Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) von Erkennungen unterstützt werden. Es wird jedoch empfohlen, dass alle Neuentwicklungen (für Erkennungen lateinischer Skripts) die in der [InputScope-Enumeration](/windows/win32/api/inputscope/ne-inputscope-inputscope) definierten Werte verwenden.\]

Die Tablet PC-Plattform unterstützt eine Reihe von Factoiden, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen. Bei der Verwendung von Factoiden ist es wichtig, dass die erwartete Eingabe genau der Definition des Factoids entspricht. Wenn die Eingabe nicht mit der Definition des Factoids übereinstimmt, wird die Erkennungsgenauigkeit beeinträchtigt. Wenn beispielsweise das  Zahlen-Factoid festgelegt ist und der Benutzer Buchstaben eingibt, ist die Erkennungsgenauigkeit für Buchstaben schlecht.

Bestimmte Factoids, z. B. **E-Mail** und **Ziffer,** sind sprachenübergreifend fast identisch. Andere Factoids, z. B. **Telefon** und **Postleitzahl,** variieren je nach Sprache. Überprüfen Sie das Format jedes Factoids für die Sprache, die Sie verwenden. Eine Liste der Formate für jedes Factoid in jeder Sprache finden Sie in den Tabellen in den Themen nach diesem Thema.

> [!Note]  
> Es gibt einen feinen, aber wichtigen Unterschied zwischen Factoids für Westsprachen und Factoiden für ostasiatische Sprachen. Factoids für Westsprachen werden mithilfe von Ausdrücken implementiert, die das gewünschte Ergebnis beschreiben. Die Erkennung wird dann voreingenommen, um Ergebnisse zu erzeugen, die diesem Ausdruck entsprechen. Factoids für ostasiatische Sprachen werden implementiert, indem ein zulässiger Bereich von Unicode-Zeichen angegeben wird. Beispielsweise akzeptiert  das Date-Factoid für ostasiatische Sprachen nur Unicode-Zeichen innerhalb eines bestimmten Bereichs.

 

Zu den Factoiden für Westsprachen gehören Factoids für Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch. Factoids für ostasiatische Sprachen umfassen Factoids für Chinesisch (vereinfacht), Chinesisch (traditionell), Japanisch und Koreanisch.

In den folgenden Abschnitten werden die Formate beschrieben, die für jedes Factoid in jeder Sprache unterstützt werden:

-   [Häufig in verschiedenen Sprachen vorkommende Factoids](factoids-common-across-languages.md)
-   [Factoids für Westsprachen](factoids-for-western-languages.md)
-   [Factoids für ostasiatische Sprachen](factoids-for-east-asian-languages.md)

Wenn Sie eine Eingabe erwarten, die sich von den in den Tabellen in diesen Abschnitten aufgeführten Formaten unterscheidet, verwenden Sie kein Factoid. Darüber hinaus sind Factoids für jede Sprache in die Erkennung integriert. Sie können keine Factoids aus einer Sprache mit einer Erkennung aus einer anderen Sprache verwenden. Beispielsweise können Sie das  französische Telefon-Factoid nicht mit einer japanischen Erkennung verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Factoidkonstanten**](factoid-constants.md)
</dt> <dt>

[Microsoft.Ink.Factoid-Klasse](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
