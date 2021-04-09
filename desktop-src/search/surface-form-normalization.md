---
description: Obwohl sich Wörter und linguistische Regeln erheblich unterscheiden, gibt es einige Überlegungen, wie z. b. Zahlen, Datumsangaben und Uhrzeiten, die konsistent über alle Wörter Trennungen hinweg behandelt werden.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalisierung des Oberflächen Formulars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b058be00e046ffc17ebd6c13178313267a47079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128488"
---
# <a name="surface-form-normalization"></a>Normalisierung des Oberflächen Formulars

Obwohl sich Wörter und linguistische Regeln erheblich unterscheiden, gibt es einige Überlegungen, wie z. b. Zahlen, Datumsangaben und Uhrzeiten, die konsistent über alle Wörter Trennungen hinweg behandelt werden. In diesem Thema werden normalisierungs Aspekte beschrieben, die sich auf Ihre Implementierung der Wörter Trennung auswirken können

Dieses Thema ist wie folgt organisiert:

-   [Silben Trennung](#hyphenation)
-   [Possessiv Formen](#possessives)
-   [Diakritische Zeichen](#diacritics)
-   [Clitik](#clitics)

## <a name="hyphenation"></a>Silben Trennung

Bindestriche (-) werden zwischen den Teilen eines zusammengesetzten Worts oder Namens verwendet. Sie werden auch zwischen den Silben eines Worts verwendet, wenn das Wort am Ende einer Textzeile aufgeteilt ist. In englischer Sprache werden Wörter mit Bindestrichen verknüpft, um eine spezielle Beziehung im Kontext anzugeben. diese Wörter werden jedoch normalerweise in anderen Kontexten nicht als Bindestriche angezeigt. beispielsweise "Schritt für Schritt". Während der Indexerstellung sollte die Wörter Trennung den Bindestrich als Wort Trennzeichen behandeln. Beispielsweise würde "Data-Base" als "Data" Plus "Base" gespeichert werden. Zum Zeitpunkt der Abfrage sollte ein Bindestrich durch zwei Alternativen ersetzt werden: die zwei-Wort-Variante und die echte Verbund-. Beispielsweise würde "Data-Base" durch "Data" Plus "Base" und "Database" ersetzt werden. Dieser Unterschied zwischen Index-und Abfragezeit erhöht die Kombinationen von Darstellungen für hyphenierte Wörter und erleichtert das Abgleichen von Wörtern in einer Abfrage.

In der folgenden Tabelle wird gezeigt, wie die Behandlung von Bindestrichen als Wort Trennzeichen in englischer Sprache die Anzahl der übereinstimmenden Abfrage Begriffe für jeden im Index enthaltenen Begriff erhöht.



| Im Index enthaltene Begriffe | Abfragezeit Übereinstimmungen   |
|-----------------------------|----------------------|
| Datenbasis                   | Data Base, Datenbasis |
| Datenbasis                   | Data Base, Datenbasis |
| Datenbank                    | Data-Base, Datenbank  |



 

## <a name="possessives"></a>Possessiv Formen

Possessiven sind Variationen in einem Substantiv, die den Besitz angeben. Englische Besitztümer werden dargestellt, indem ein Apostroph (') oder ein Apostroph und ein s (es) an ein Wort angehängt werden. Um z. b. den Besitz anzugeben, wird das Wort "Mary" als "Mary es" dargestellt. Die Wörter Trennung generiert zum Zeitpunkt der Abfrage sowohl das Apostroph-als auch das Apostroph-s-Formular. Abfragen für "Mary" sollten sowohl "Mary" als auch "Mary es" entsprechen.

## <a name="diacritics"></a>Diakritische Zeichen

Diakritik sind Markierungen, die einem Buchstaben oder Phonem hinzugefügt werden, um einen speziellen phonetischen Wert für die Aussprache anzugeben. Die Diakritik kann Wörter unterscheiden, die anderweitig grafisch identisch sind. Beispiel: "Resume" und "Resumé" in englischer Sprache. Das Speichern der Diakritik im Index erhöht jedoch die Anzahl eindeutiger Wort Schlüssel im Index, was die Abfrageleistung verlangsamt. Wenn die Diakritik nur minimal in einer Sprache verwendet wird, sollte Sie von der Wörter Trennung für diese Sprache während der Indexerstellung und-Abfrage entfernt werden. Beispielsweise generiert die englische Wörter Trennung "Resume", wenn "Resumé" verarbeitet wird, was nur minimale Auswirkung auf die Relevanz der Abfrageergebnisse verursacht.

## <a name="clitics"></a>Clitik

Ein clitic ist ein nicht ausgefülltes Wort, das nicht eigenständig stehen und an ein gebetontes Wort angehängt werden kann, um eine einzelne Einheit zu bilden. Clitics kann nicht einfach als phonologisch, syntaktisch oder morphologisch klassifiziert werden. Clitics gibt es in zwei Typen: *proclitics* und *interclitik*. Die proclitik hängt an den Anfang eines Worts an. Die enclitik hängt an das Ende eines Worts an.

Das Analysieren von clitics in Sprachen wie z. b. Spanisch ist schwieriger. Ein spanisches Verb kann je nach Spannung viele Oberflächen Formulare generieren. Es müssen Überlegungen zwischen dem Entfernen der clitic während der Indexerstellung und dem Erzeugen der Oberflächen Formen durch Wort Stamm Erkennung zum Zeitpunkt der Abfrage vorgenommen werden. Das Entfernen von clitics in Fällen, in denen die Morphologie der clitischen Komposition mehrdeutig ist, kann zu unvorhersehbaren Ergebnissen führen. Das Erstellen einer großen Anzahl von Oberflächen Formularen für ein Wort erhöht die Größe des voll Text Indexes und verlangsamt möglicherweise die Abfrageleistung. Es wird empfohlen, dass die Wort Stamm Erkennung nur eine kleine Anzahl von Oberflächen Formularen generiert.

 

 



