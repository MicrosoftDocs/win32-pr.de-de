---
description: Obwohl Wörter und linguistische Regeln sich erheblich unterscheiden, gibt es einige Überlegungen, z. B. Zahlen, Datumsangaben und Zeiten, die über alle Wörterbrechen hinweg konsistent behandelt werden.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalisierung von Oberflächenformularen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f96ce5c90075c49608ad386b64514e4d003e5b5b4c6fc582441fd7e110d1921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862434"
---
# <a name="surface-form-normalization"></a>Normalisierung von Oberflächenformularen

Obwohl Wörter und linguistische Regeln sich erheblich unterscheiden, gibt es einige Überlegungen, z. B. Zahlen, Datumsangaben und Zeiten, die über alle Wörterbrechen hinweg konsistent behandelt werden. In diesem Thema werden Normalisierungsüberlegungen beschrieben, die sich möglicherweise auf die Implementierung der Wörterumbruch-Funktion auswirken.

Dieses Thema ist wie folgt organisiert:

-   [Hyphenation](#hyphenation)
-   [Possessives](#possessives)
-   [Diakritische Zeichen](#diacritics)
-   [Clitics](#clitics)

## <a name="hyphenation"></a>Hyphenation

Bindestriche (-) werden zwischen den Teilen eines zusammengesetzten Worts oder Namens verwendet. Sie werden auch zwischen den Silben eines Worts verwendet, wenn das Wort am Ende einer Textzeile geteilt wird. Im Englischen werden Wörter mit Bindestrichen verbunden, um eine besondere Beziehung im Kontext anzugeben, aber diese Wörter sind normalerweise in anderen Kontexten möglicherweise nicht mit Bindestrichen verbunden. Beispiel: "Schritt für Schritt". Während der Indexerstellung sollte die Wörtertrennung den Bindestrich als Worttrennzeichen behandeln. Beispielsweise würde "data-base" als "data" plus "base" gespeichert. Zur Abfragezeit sollte ein bindestrichierter Ausdruck durch zwei Alternativen ersetzt werden: die Zwei-Wort-Variante und die true-Verbindung. Beispielsweise würde "data-base" durch "data" plus "base" und "database" ersetzt. Dieser Unterschied zwischen Index- und Abfragezeit erhöht die Kombinationen von Darstellungen für Wörter mit Bindestrichen und erleichtert die Übereinstimmung der Wörter in einer Abfrage.

Die folgende Tabelle zeigt, wie die Behandlung von Bindestrichen als Worttrennzeichen in der englischen Sprache die Anzahl der übereinstimmenden Abfragebegriffe für jeden im Index enthaltenen Begriff erhöht.



| Im Index enthaltene Begriffe | Übereinstimmungen zur Abfragezeit   |
|-----------------------------|----------------------|
| Datenbank                   | -Datenbank, -Datenbank |
| Data-Base                   | -Datenbank, -Datenbank |
| Datenbank                    | Data Base, Datenbank  |



 

## <a name="possessives"></a>Possessives

Possessives sind Variationen in einem Nomen, die den Besitz angeben. Englische Possessive werden durch Anfügen eines Apostrophs (') oder eines Apostrophs und eines s (s) an ein Wort dargestellt. Um beispielsweise den Besitz anzugeben, wird das Wort "Mary" als "Mary" dargestellt. Die Wörterpause generiert zur Abfragezeit sowohl das Apostroph als auch das Apostroph. Abfragen für "Mary" sollten sowohl mit "Mary" als auch mit "Mary's" übereinstimmen.

## <a name="diacritics"></a>Diakritische Zeichen

Diakritische Zeichen sind Markierungen, die einem Buchstaben oder Phonem hinzugefügt werden, um einen speziellen phonetischen Wert für die Aussprache anzugeben. Diakritische Zeichen können Wörter unterscheiden, die ansonsten grafisch identisch sind. beispielsweise "resume" und "resumé" auf Englisch. Das Speichern von diakritischen Zeichen im Index erhöht jedoch die Anzahl eindeutiger Wortschlüssel im Index, wodurch die Abfrageleistung verlangsamt wird. Wenn diakritische Zeichen nur minimal in einer Sprache verwendet werden, sollten sie in der Wörterpause für diese Sprache sowohl während der Indexerstellung als auch bei Abfragen entfernt werden. Beispielsweise generiert die englische Wörterpause "resume" bei der Verarbeitung von "resumé", was nur minimale Auswirkungen auf die Relevanz der Abfrageergebnisse hat.

## <a name="clitics"></a>Clitics

Eine Clitic ist ein unstressiertes Wort, das nicht allein stehen kann und an ein wortvergningbares Wort angefügt wird, um eine einzelne Einheit zu bilden. Clitics können nicht einfach als morphologisch, syntaktisch oder ungespähnt klassifiziert werden. Clitics gibt es in zwei Typen: *proklidische* und *enklidische*. Proklidische Zeichen fügen sich an den Anfang eines Worts an. Enclitics fügen sich selbst an das Ende eines Worts an.

Clitics sind in Sprachen wie Spanisch schwieriger zu analysieren. Ein spanischer Verb kann je nach Angespann viele Oberflächenformen generieren. Es muss zwischen dem Entfernen der Clitic während der Indexerstellung und dem Generieren der Oberflächenformulare durch Diemung zur Abfragezeit berücksichtigt werden. Das Entfernen von Clitics in Fällen, in denen die Hemmung der clitic composition mehrdeutig ist, kann zu unvorhersehbaren Ergebnissen führen. Das Generieren einer großen Anzahl von Oberflächenformen für ein Wort erhöht die Größe des Volltextindexes und kann die Abfrageleistung verlangsamen. Es wird empfohlen, dass der Stammstamm nur eine kleine Anzahl von Oberflächenformen generiert.

 

 



