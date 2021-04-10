---
description: Microsoft stellt Wörter Trennungen und Wort Stamm Erkennungen für eine Reihe von Sprachen bereit. In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Wörter Trennungen und Wort Stamm Erkennungen für Sprachen und Gebiets Schemata, die von Microsoft bereitgestellt werden, implementieren und verwenden.
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: Implementieren von Wörter Trennungen und Wort Stamm Erkennungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd4f4e3210e7f4e17bb035115fd694656cc6e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041626"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>Implementieren von Wörter Trennungen und Wort Stamm Erkennungen

Microsoft stellt Wörter Trennungen und Wort Stamm Erkennungen für eine Reihe von Sprachen bereit. In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Wörter Trennungen und Wort Stamm Erkennungen für Sprachen und Gebiets Schemata, die von Microsoft bereitgestellt werden, implementieren und verwenden.

> [!Note]
> Seit Juli 2018 wurde eine Sicherheitsänderung an Windows Server 2019 vorgenommen, wodurch verhindert wird, dass DLLs ohne Microsoft-Signatur von SearchIndexer.exe geladen werden. Daher unterstützt Windows Server 2019 nicht mehr die von Microsoft signierten benutzerdefinierten Wörter Trennungen. 

Dieses Thema ist wie folgt organisiert:

-   [Registrieren einer Sprachressourcen-dll](#registering-a-language-resource-dll)
-   [Registrieren einer Sprache](#registering-a-language-resource-dll)
-   [Implementieren eines Wort Bechers](#implementing-a-word-beaker)
    -   [Wordsink und phrasesink](#wordsink-and-phrasesink)
    -   [Zeilenumbrüche](#breaks)
    -   [Skalierbarkeit, Leistung und Sicherheit](#scalability-performancy-and-security)
-   [Implementieren einer Wort Stamm Erkennung](#implementing-a-stemmer)
    -   [Skalierbarkeit, Leistung und Sicherheit](#scalability-performancy-and-security)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-a-language-resource-dll"></a>Registrieren einer Sprachressourcen-dll

Jede Sprachressourcen-dll muss die folgenden Einstiegspunkte implementieren und exportieren. Die dll kann in einem beliebigen Ordner registriert werden.

-   DllMain ist der Standard Einstiegspunkt für die dll.
-   DllRegisterServer registriert die dll in der Registrierung, z. b. `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   DllCanUnloadNow ermöglicht Clients, diesen Einstiegspunkt über Component Object Model (com) aufzurufen, um zu bestimmen, ob es möglich ist, die Sprachressourcen-dll zu entladen.
-   DllUnregisterServer entfernt die dll aus der Registrierung.

## <a name="registering-a-language"></a>Registrieren einer Sprache

Die Registrierung enthält sprachspezifische Einträge für die zu indizierende Sprache. diese Einträge steuern die Teile der Indizierungs-und Abfrage Prozesse, die sprachspezifisch sind. Diese Registrierungseinträge finden Sie unter dem folgenden Registrierungsschlüssel.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>Implementieren eines Wort Bechers

Die Wörter Trennung implementiert [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker). Die [**iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode führt die gesamte Textverarbeitung und-Verarbeitung aus. Zum Implementieren einer Wörter Trennungs Komponente müssen Sie über eine sprach-Heuristik für Ihre Sprache verfügen. Dies schließt Informationen über Syntax und Morphologie ein. Möglicherweise benötigen Sie auch eine Liste von Wörtern, die ausgeschlossen oder eingeschlossen werden sollen. Sie erstellen die Datei mit Füll Wörtern für das Gebiets Schema der Sprache aus der Liste der ausgeschlossenen Wörter. Weitere Informationen zu linguistischen Überlegungen und deren Auswirkungen auf die Implementierung von Wörter Trennungen finden Sie unter [Überlegungen zu linguistischen und Unicode](linguistic-and-unicode-considerations.md)

Der Hauptzweck von [**iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) besteht darin, Text kontinuierlich von der [**Text \_ Quelle**](/windows/win32/api/indexsrv/ns-indexsrv-text_source) zu verarbeiten, bis der gesamte Text verarbeitet wird oder wenn die Wörter Trennung auf einen Fehler stößt. In dieser Datenverarbeitungs Schleife ruft **iwordbreaker:: breaktext** die Methoden zum Durchführen von Vorgängen und Dienstprogrammen auf, die bestimmte Aufgaben für diesen Prozess ausführen. Die deutsche Wörter Trennung kann z. b. zusammengesetzte Wörter verarbeiten, während die französische Wörter Trennung [Diakritik](surface-form-normalization.md) oder [clitics](surface-form-normalization.md)verarbeiten kann. Die spezifischen Funktionen, die die Wörter Trennung durchführt, und die Strategie, die für die Ausführung dieser Aufgaben verwendet wird, sind vollständig von den Anforderungen für diese Sprache abhängig.

Beim Abbrechen von Text identifiziert die Wörter Trennung "Alternative" Formulare für Wörter, die mehrere Darstellungen aufweisen können. Zwischen den generierten Wörtern wird keine Semantik Beziehung impliziert. Tatsächlich ist das ursprüngliche Wort möglicherweise nicht in der Liste der alternativen enthalten. Die alternativen Formulare werden an derselben Position im Index gespeichert wie das ursprüngliche Wort, um anzugeben, dass Sie identisch sind.

Wenn ein Dokument im Index enthalten ist, wird jedem Wort ein ganzzahliger Wert zugewiesen, der den Offset darstellt, oder der Abstand des Worts vom Anfang eines Dokuments. Der relative Abstand zwischen Wörtern in einer Abfrage wird mit den im Volltextindex gespeicherten Offsets verglichen. Die Abfrage "Where is Document es Document" entspricht jedem Dokument mit "Where" bei Offset n, "is" bei n + 1, "Kyle es" bei n + 2 und "Document" bei n + 3. "Wo ist das Dokument von Kyle in der Data Base abgelegt?" wird wie folgt dargestellt:



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Hierbei gilt: | is  | Kyle Kyle<br/> | Dokument | Fassung | in  | the | Datenbank-Datenbasis<br/> |



 

In diesem Beispiel speichert die Wörter Trennung Alternative Formulare für "Kyle" ("Kyle es") und "Database" ("Data Base") im Index. Die Wörter Trennung generiert und speichert Alternative Wörter während des Index Erstellungs Prozesses unter den folgenden Bedingungen:

-   Wenn ein alternatives Wort wahrscheinlich als einzelnes Wort in einer Abfrage angezeigt wird.
-   Wenn eine Wort Stamm Erkennung das ursprüngliche Wort von der Alternativen nicht ableiten kann

Das Erstellen von alternativen Wort Formularen erhöht die Anzahl der Methoden, die Abfragen darstellen und einem Satz entsprechen, wie in den folgenden Variationen dargestellt:

1.  Wo ist das Kyle-Dokument in der Datenbank abgelegt?
2.  Wo ist das Dokument von Kyle in der Datenbank abgelegt?
3.  Wo ist das Kyle-Dokument in der Datenbasis abgelegt?
4.  Wo ist das Dokument von Kyle in der datendatenbank abgelegt?

### <a name="wordsink-and-phrasesink"></a>Wordsink und phrasesink

Die Wörter Trennungen verwenden die [**iwordsink**](iwordsink.md) -und [**iphrasesink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) -Objekte, um alle Wörter und Ausdrücke zu erfassen und zu speichern, die Sie aus Text extrahieren. Eine Wörter Trennung speichert Wörter in einem Formular, das so nah wie möglich für das ursprüngliche Word-Formular im Dokument ist. **Iphrasesink** speichert Ausdrücke zum Zeitpunkt der Abfrage. Ausdrücke verbessern die Relevanz von Abfrage Ergebnissen, da längere Sequenzen von Wörtern seltener sind und größere Unterschiede als kleinere Ausdrücke ermöglichen. Wenn der Indexer einen Ausdruck in **iphrasesink** zur Abfragezeit platziert, erstellt er eine Instanz der Wörter Trennung, um den Ausdruck in Wörter zu unterbrechen. Der Indexer wertet dann den Ausdruck aus, indem überprüft wird, ob die Wörter im Ausdruck in der Nähe zueinander im Index vorkommen. Wenn z. b. "abcd" im Index an den Positionen *x*, *x*+ 1, *x*+ 2 und *x*+ 3 auftritt, erfolgt die Ausdrucks Übereinstimmung, wenn eine benachbarte Teil Zeichenfolge von "abcd" in einer Abfrage übermittelt wird. Diese Strategie ist für zeichenbasierte Wörter Trennungen wirksam, die während der Indexerstellung Ausdrücke und lange Wörter aufteilen und während der Abfragezeit Ausdrücke generieren.

### <a name="breaks"></a>Zeilenumbrüche

Unterbrechungen sind die Leerzeichen zwischen Wörtern. Leerraum, Interpunktions Zeichen, Formatierung oder nur die Natur der Sprache selbst können zu Unterbrechungen führen. Es gibt vier verschiedene Arten von Umbrüchen, die der Indexer verwendet: Ende des Worts (EOW), Ende des Satzes (EOS), Ende des Absatzes (EoP) und das Ende des Kapitels (EOC). Die EOW-Unterbrechung ist die Standardeinstellung. Nach jedem Token gibt jeder Break-Wert einen anderen semantischen Abstand zwischen den Wörtern auf beiden Seiten an. Wörter, die durch EOW getrennt sind, haben den Link zur semantischen Semantik, gefolgt von EOS, EoP und EOC. Mehrere Aufrufe von [**iwordsink::P utbreak**](iwordsink-putbreak.md) sind kumulativ und sind analog zum Einfügen von NULL-Wörtern oder-Sätzen.

### <a name="scalability-performancy-and-security"></a>Skalierbarkeit, Leistung und Sicherheit

Die Art und Weise, wie die Wörter Trennung auf gleichzeitige Aufrufe antwortet, hängt größtenteils von der Auswahl des Threading Modells ab. Der Indexer ist eine Single Thread-Anwendung. Damit die Wörter Trennung in einer Single Thread-Umgebung funktioniert, muss die Wörter Trennung mithilfe eines "kostenlosen" oder "beiden" Threading Modells geschrieben werden. Wörter Trennungen dürfen nicht bei com registriert werden, indem das Threading Modell "Apartment" verwendet wird.

Es wird empfohlen, dass Wörter Trennungen globale Zustände vermeiden und Daten in der Instanz für die Wörter Trennung speichern. Der einzige Inhalt, der in der Implementierung der Wörter Trennung gespeichert werden soll, ist für die Parameter " *f Query* " und " *ulmaxtokensize*". Die Wörter Trennungen sollten nicht mehr als zwei Mal langsamer sein als der von der englischen Wörter Trennung festgelegte Benchmarkwert. Die Leistung der Wörter Trennung sollte auch mit erhöhter Hardware Funktion verbessert werden.

Die Wörter Trennungen für den Indexer werden im Sicherheitskontext des lokalen Systems ausgeführt. Sie sollten so geschrieben werden, dass Sie Puffer verwalten und ordnungsgemäß stapeln. Alle Zeichen folgen Kopien müssen über explizite Überprüfungen zum Schutz vor Pufferüberläufen verfügen. Sie sollten stets die zugeordnete Größe des Puffers überprüfen und die Größe der Daten mit der Größe des Puffers testen. Die Wörter Trennung kann nicht davon ausgehen, dass der an die [**iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode übergebenen Text wohl geformt ist. Weitere Informationen zur Problembehandlung von Wörter Trennungen finden Sie unter Problembehandlung bei [Sprachressourcen und bewährten Methoden](troubleshooting-language-resources.md).

## <a name="implementing-a-stemmer"></a>Implementieren einer Wort Stamm Erkennung

Stemerkennungen implementieren die [**istemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) -Schnittstelle. Die [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) -Methode generiert eine Liste von eingebetteten Wort Formularen für ein bestimmtes Eingabe Wort. Zum Implementieren einer Wort Stamm Erkennung-Komponente müssen Sie über eine sprach-Heuristik für Ihre Sprache verfügen. Dies schließt Informationen über die Morphologie ein. Möglicherweise benötigen Sie auch eine Liste von Wörtern, die ausgeschlossen oder eingeschlossen werden sollen. Weitere Informationen zu linguistischen Überlegungen und dazu, wie sich diese Überlegungen auf Wort Stamm Erkennung-Implementierungen auswirken, finden Sie unter [linguistische und Unicode](linguistic-and-unicode-considerations.md)

Es wird empfohlen, dass Wort Stamm Erkennungen für Wörter nicht den Wert "Genie" oder "possessiv" generieren sollten. Beispielsweise wird "David" nicht als Alternative Form für "David es" generiert. Die Wörter Trennung generiert "David" und "David es", wenn Sie "David es" analysiert.

Die Wort Stamm Erkennung verwendet das [iwordformsink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt, um die Liste der alternativen Wörter zu erfassen. [**Iwordformsink::P utword**](iwordformsink-putword.md) generiert das abschließende Wort aus der Wort Stamm Erkennung. In allen Fällen ist dieses abschließende Wort mit dem Eingabe Wort von [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms)identisch. Beispielsweise generiert die Wort Stamm Erkennung bei Angabe des Worts "Swim" die folgenden Wortformen: "Swimming", "Schwimmer", "swims", "" und "Swap" durch Aufrufe von " [**iwordformsink::P utaltword**](iwordformsink-putphrase.md)". Die Wort Stamm Erkennung generiert "Swimming" über **iwordformsink::P utword**.

### <a name="scalability-performancy-and-security"></a>Skalierbarkeit, Leistung und Sicherheit

Wort Stamm Erkennungen müssen ein "Kostenloses" Threading Modell verwenden und sich bei com registrieren, wobei das Threading Modell auf "Free" oder "both" festgelegt ist. Die Windows-Suche ruft separate Instanzen der Wort Stamm Erkennung aus verschiedenen Threads gleichzeitig auf. Wort Stamm Erkennungen sollten daher nur minimale Instanzdaten aufweisen.

Die Wort Stamm Erkennung hat erhebliche Auswirkungen auf die Relevanz der Abfrage. Wenn die Wort Stamm Erkennung den Text nicht ordnungsgemäß inszeniert, können Abfragen unvorhersehbare und ungenaue Ergebnisse zurückgeben. Wort Stamm Erkennungen müssen Hunderte von Abfragen pro Sekunde verarbeiten, ohne die Abfrageleistung zu beeinträchtigen. Die Wort Stamm Erkennung sollte mit erhöhter Hardware Leistung verbessert werden. Informationen zur Problembehandlung von Wort Stamm Erkennungen finden Sie unter Problembehandlung bei [Sprachressourcen und bewährten Methoden](troubleshooting-language-resources.md).

Die Wort Stamm Erkennung für die Windows-Suche wird im lokalen Sicherheitskontext ausgeführt. Sie sollten so geschrieben werden, dass Sie Puffer verwalten und ordnungsgemäß stapeln. Alle Zeichen folgen Kopien müssen über explizite Überprüfungen zum Schutz vor Pufferüberläufen verfügen. Sie sollten stets die zugeordnete Größe des Puffers überprüfen und die Größe der Daten mit der Größe des Puffers testen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Grundlegendes zu Sprachressourcen Komponenten](understanding-language-resource-components.md)
</dt> <dt>

[Überlegungen zu linguistischer und Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Problembehandlung bei Sprachressourcen und bewährten Methoden](troubleshooting-language-resources.md)
</dt> </dl>

 

 
