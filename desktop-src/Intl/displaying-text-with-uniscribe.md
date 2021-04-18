---
description: Ihre Anwendungen können uniwriter-API-Funktionen verwenden, um Typografiefunktionen und die Anzeige und Bearbeitung von internationalem Text zu unterstützen. Uniwriter verwendet den Absatz als Einheit für die Textanzeige, und die Funktion uniwriter muss für den gesamten Absatz verwendet werden.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Anzeigen von Text mit uniwriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baeb9a2be4d00efaa2681097ddefe3a6de4c576b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348159"
---
# <a name="displaying-text-with-uniscribe"></a>Anzeigen von Text mit uniwriter

Ihre Anwendungen können uniwriter-API-Funktionen verwenden, um Typografiefunktionen und die Anzeige und Bearbeitung von internationalem Text zu unterstützen. Uniwriter verwendet den Absatz als Einheit für die Textanzeige, und die Funktion uniwriter muss für den gesamten Absatz verwendet werden.

Wenn uniwriter für die Anzeige von Text verwendet wird, muss eine Anwendung einen Formatierungsprozess ("Layout") durchlaufen, der in der Regel "uniwriter" verwendet. Die Anwendung dividiert einen Text Absatz in Zeichen folgen mit dem gleichen Stil, der so genannten "runs". Der Stil wird von der jeweiligen Implementierung bestimmt, enthält jedoch in der Regel Attribute wie Schriftart, Größe und Farbe. Beim Definieren von Ausführungen kann die Anwendung auch andere Informationen anwenden, wie z. b. sprach-und Gebiets Schema Daten, die für die Verwendung mit lexikalischen Tools verwaltet werden. Eine Anwendung kann z. b. als separate Run a Passage in einem primär englischen Text behandeln, der in Französisch gerendert wird.

Nachdem die Ausführungen für alle Absätze ermittelt wurden, dividiert die Anwendung jeden Absatz in Zeichen folgen, die das gleiche Skript und die gleiche Richtung ("Items") aufweisen. Die Anwendung wendet die Element Informationen an, um in Skript und Richtung eindeutige Ausführungen zu erstellen, die vollständig innerhalb eines einzelnen Elements ("Bereiche") liegen.

Die Aufteilung eines Elements in Bereiche ist beliebig, obwohl ein Bereich aus einer oder mehreren aufeinander folgenden Skript definierten, unteilbaren Zeichen Gruppierungen bestehen muss, die als "Cluster" bezeichnet werden. Bei europäischen Sprachen entspricht ein Cluster in der Regel einem einzelnen Codepage-oder Unicode-Codepunkt und besteht aus einem einzelnen [Symbol.](uniscribe-glossary.md) In Sprachen wie Thai ist ein Cluster jedoch eine Gruppierung von Symbolen und entspricht mehreren aufeinander folgenden Zeichen oder Code Punkten. Ein thailändischer Cluster kann z. b. einen Konsonanten, einen vowel und ein Ton Zeichen enthalten. Damit Cluster nicht unterstützt werden, sollte die Anwendung normalerweise die längsten Bereiche verwenden, die Sie verwenden können, oder Ihre eigenen lexikalischen Informationen verwenden, um zwischen Bereichen an Orten zu unterbrechen, die nicht in der Mitte eines Clusters liegen.

Wenn die Cluster in jedem Bereich identifiziert wurden, muss die Größe der einzelnen Cluster von der Anwendung bestimmt werden. Er verwendet uniscri, um die Cluster zusammenzufassen, um die Größe der einzelnen Bereiche zu bestimmen. Dann summiert die Anwendung die Größe der Bereiche, bis Sie eine Linie überschreiten, d. h., der Rand wird erreicht. Der Bereich, in dem die Linie überläuft, ist von der aktuellen Zeile und der nächsten Zeile getrennt. Für jede Zeile erstellt die Anwendung eine Zuordnung von der visuellen Position zur logischen Position für jeden Bereich. Dann formt die Anwendung die Code Punkte für jeden Bereich in Glyphen, die anschließend positioniert und dargestellt werden können.

Eine Anwendung führt ein Text Layout nur ein Mal aus. Anschließend speichert Sie entweder die Symbole und Positionen zu Anzeige Zwecken oder generiert Sie jedes Mal, wenn der Text angezeigt wird, und der Nachteil ist Geschwindigkeit und Arbeitsspeicher. Eine typische Anwendung implementiert den Layoutprozess einmal und generiert dann die Symbole und Positionen jedes Mal, wenn der Text angezeigt wird.

Eine Anwendung, die [komplexe Skripts](uniscribe-glossary.md) verwendet, hat die folgenden Probleme mit einem einfachen Ansatz für Layout und Anzeige.

-   Die Breite eines komplexen Skript Zeichens hängt von seinem Kontext ab. Es ist nicht möglich, die breiten in einfachen Tabellen zu speichern.
-   Das Unterbrechen von Wörtern in Skripts, wie z. b. Thai, erfordert die Beispielsweise wird kein Trennzeichen zwischen thailändischen Wörtern verwendet.
-   Arabisch, Hebräisch, Persian, Urdu und andere [bidirektionale Text](uniscribe-glossary.md) Sprachen erfordern eine Neuanordnung vor der Anzeige.
-   Eine Form der Schriftart Zuordnung ist häufig erforderlich, um komplexe Skripts einfach zu verwenden.

Die Tatsache, dass unischreiber den Absatz als Anzeigeeinheit verwendet, hilft der Anwendung, diese komplexen Skript Probleme adäquat zu beheben.

> [!Note]  
> Unischreiber muss für einen gesamten Absatz verwendet werden, auch wenn Abschnitte des Absatzes keine komplexen Skripts sind.

 

Wie in der folgenden Tabelle gezeigt, unterstützt unischreiber, Version 1,6 oder höher, mehrere Funktionen, die OpenType-Tags nutzen. Sie können die entsprechenden regulären uniscriefunktionen ersetzen. Im Allgemeinen sollten Ihre Anwendungen vollständig mit Funktionen aus einem Satz oder dem anderen arbeiten und sollten nicht versuchen, Funktionen zu "mischen und abzugleichen".



| Reguläre uniscri-Funktion             | Äquivalente OpenType-Funktion                           |
|----------------------------------------|--------------------------------------------------------|
| [**Scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**Scriptitemizeopentype**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**Scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**Scriptshapeopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**Scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**Scriptplaceopentype**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Layout von Text mit uniwriter

Die Anwendung kann mithilfe der folgenden Schritte einen Text Absatz mit uniwriter aufstellen. Bei diesem Verfahren wird davon ausgegangen, dass die Anwendung den Absatz bereits in Ausführungen aufgeteilt hat.

1.  [**Scriptrecorddigitsubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) wird nur beim Starten von oder beim Empfangen einer [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht aufgerufen.
2.  Optionale Wenden Sie [**scriptiscomplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) an, um zu bestimmen, ob der Absatz eine komplexe Verarbeitung erfordert.
3.  Optionale Wenn uniwriter zum Verarbeiten von bidirektionalem Text und/oder Ziffern Ersetzung verwendet wird, wird [**scriptapplydigitsubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) aufgerufen, um das [**Skript \_ Steuer**](/windows/win32/api/usp10/ns-usp10-script_control) Element und die [**Skript \_ Zustands**](/windows/win32/api/usp10/ns-usp10-script_state) Strukturen als Eingaben für [**scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)vorzubereiten. Wenn Sie diesen Schritt überspringen, aber trotzdem eine Ziffern Ersetzung benötigen, ersetzen Sie die Ziffern für Unicode U + 0030 bis u + 0039 (europäische Ziffern). Weitere Informationen zur Ziffern Ersetzung finden Sie unter [Ziffern Formen](digit-shapes.md).
4.  Nennen Sie [**scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) , um den Absatz in Elemente aufzuteilen. Wenn Sie unischreiber nicht für die Ziffern Ersetzung verwenden und die bidirektionale Reihenfolge bekannt ist, z. b. aufgrund des zum Eingeben des Zeichens verwendeten Tastaturlayouts, nennen Sie **scriptitemize**. Geben Sie im-Befehl NULL-Zeiger für das [**Skript \_ Steuer**](/windows/win32/api/usp10/ns-usp10-script_control) Element und die [**Skript \_ Zustands**](/windows/win32/api/usp10/ns-usp10-script_state) Strukturen an. Bei dieser Methode werden Elemente nur mithilfe der Strukturierungs-Engine generiert, und die Elemente können mithilfe der Engine-Informationen neu angeordnet werden.
    > [!Note]  
    > Normalerweise sollten Anwendungen, die nur mit Skripts von links nach rechts und ohne Ziffern Ersetzung funktionieren, NULL-Zeiger für das [**Skript \_ Steuer**](/windows/win32/api/usp10/ns-usp10-script_control) Element und die [**Skript \_ Zustands**](/windows/win32/api/usp10/ns-usp10-script_state) Strukturen übergeben.

     

5.  Zusammenführen der Element Informationen mit den laufinformationen, um Bereiche zu liefern.
6.  Rufen Sie [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) auf, um Cluster zu identifizieren und Symbole zu generieren.
7.  Wenn [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) das Code-USP \_ E- \_ Skript \_ nicht \_ in \_ der Schriftart oder in \_ der Ausgabe mit den fehlenden Glyphen zurückgibt, wählen Sie Zeichen aus einer anderen Schriftart aus. Ersetzen Sie entweder eine andere Schriftart, oder deaktivieren Sie die Strukturierung, indem Sie den **Escript** -Member der [**Skript \_ Analyse**](/windows/win32/api/usp10/ns-usp10-script_analysis) Struktur festlegen, die an **scriptshape** übergeben wurde \_ Weitere Informationen finden Sie unter [using Font Fallback](using-font-fallback.md).
8.  Rufen Sie [**scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) auf, um die [voraus](uniscribe-glossary.md) setzungen und x-und y-Positionen für die Symbole in jedem aufeinander folgenden Bereich zu generieren. Dies ist der erste Schritt, bei dem die Textgröße berücksichtigt wird.
9.  Addieren Sie die Bereichs Größen, bis die Zeile überläuft.
10. Unterbrechen Sie den Bereich an einer Wort Grenze mithilfe der **fsoft Break** -und **fwhitespace** -Elemente in den logischen Attributen. Um einen einzelnen Zeichen Cluster während des Testlaufs zu unterbrechen, verwenden Sie die vom Aufruf von [**scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)zurückgegebenen Informationen.
    > [!Note]  
    > Entscheiden Sie, ob der erste Codepunkt eines Bereichs ein Wort Umbruch Punkt sein soll, da das letzte Zeichen des vorherigen Bereichs dies erfordert. Wenn z. b. ein Bereich mit einem Komma endet, sollten Sie das erste Zeichen des nächsten Bereichs als Wort Breakpoint in Erwägung gezogen.

     

11. Wiederholen Sie die Schritte 6 bis 10 für jede Zeile im Absatz. Wenn jedoch die letzte Run-Zeile in der Zeile unterbrochen wird, wird [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) aufgerufen, um den verbleibenden Teil der Laufzeit als ersten Testlauf in der nächsten Zeile neu zu strukturieren.

## <a name="display-text-using-uniscribe"></a>Anzeigen von Text mit uniwriter

Die Anwendung kann die folgenden Schritte ausführen, um einen Text Absatz anzuzeigen. Bei diesem Verfahren wird davon ausgegangen, dass die Anwendung den Text bereits angelegt hat und die Symbole und Positionen nicht aus dem Layoutprozess gespeichert hat. Wenn die Geschwindigkeit ein Problem ist, kann die Anwendung die Symbole und Positionen aus der layoutprozedur speichern und bei Schritt 2 in der Anzeige Prozedur beginnen.

> [!Note]  
> Die Anwendung kann Schritt 2 weglassen, wenn der Text keine Zeichen von von rechts nach links gerichteten Skripts enthält, keine bidirektionalen Steuerzeichen enthält und eine Basis Einbettungs Ebene von links nach rechts verwendet.

 

1.  Führen Sie für jede ausführen die folgenden Schritte aus:
    1.  Wenn sich der Stil seit der letzten Durchführung geändert hat, aktualisieren Sie das Handle für den Gerätekontext, indem Sie es freigeben und wiederholen.
    2.  Rufen Sie [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) auf, um Symbole für den Testlauf zu generieren.
    3.  Rufen Sie [**scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) auf, um für jedes Symbol eine Vorlauf Breite und einen x-, y-Offset zu generieren.
2.  Gehen Sie folgendermaßen vor, um die richtige visuelle Reihenfolge für die Ausführungen in der Zeile zu erstellen:
    1.  Extrahieren Sie ein Array von bidirektionalen [Einbettungs Ebenen](uniscribe-glossary.md), eine pro Bereich. Die Einbettungs Ebene wird durch (Skript \_ Element) Si () angegeben. ( Skript \_ Analyse) a. (Skript \_ State) s. ubidilevel.
    2.  Übergeben Sie dieses Array an [**scriptlayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) , um eine Zuordnung von visuellen Positionen zu logischen Positionen zu generieren.
3.  Optionale Um den Text zu rechtfertigen, nennen Sie entweder [**scriptrecht**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) , oder verwenden Sie spezielle Kenntnisse des Texts.
4.  Verwenden Sie die Visualisierung für die visuelle Darstellung, um die Ausführungen in der visuellen Reihenfolge anzuzeigen. Wenn Sie am linken Ende der Zeile beginnen, nennen Sie [**scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) , um die vom ersten Eintrag in der Zuordnung angegebene Testlauf anzuzeigen. Nennen Sie für jeden nachfolgenden Eintrag in der Zuordnung **scripttextout** , um die angezeigte Laufzeit rechts von der zuvor angezeigten Testlauf anzuzeigen.

    Wenn Sie Schritt 2 weglassen, beginnen Sie am linken Ende der Zeile, und nennen Sie [**scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) , um die erste logische Testlauf anzuzeigen, und dann die einzelnen logischen Testlauf auf der rechten Seite der vorherigen Testlauf anzuzeigen.

5.  Wiederholen Sie die obigen Schritte für alle Zeilen im Absatz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 
