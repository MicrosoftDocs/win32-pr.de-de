---
title: Informationen zu Atom-Tabellen
description: In diesem Abschnitt werden Atomtabellen erläutert.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- Atome
- Atom-Tabellen
- Atomnamen
- dynamischer Datenaustausch (DDE), Atome
- DDE (dynamischer Datenaustausch),atoms
- Globale Atomtabellen
- Lokale Atomtabellen
- Ganzzahlige Atome
- Zeichenfolgenatome
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 92a8304e1e96c7385ddb11ba6391258acbe62a26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549605"
---
# <a name="about-atom-tables"></a>Informationen zu Atom-Tabellen

Eine *Atom-Tabelle* ist eine systemdefinierte Tabelle, in der Zeichenfolgen und entsprechende Bezeichner gespeichert werden. Eine Anwendung platziert eine Zeichenfolge in einer Atomtabelle und empfängt eine 16-Bit-Ganzzahl, die als Atom bezeichnet wird und für den Zugriff auf die Zeichenfolge verwendet werden kann.  Eine Zeichenfolge, die in einer Atomtabelle platziert wurde, wird als *Atomname bezeichnet.*

Das System bietet eine Reihe von Atomtabellen. Jede Atomtabelle dient einem anderen Zweck. Beispielsweise verwenden dynamischer Datenaustausch -Anwendungen (DDE) [](#global-atom-table) die globale Atom-Tabelle, um Elementnamen- und Themennamenzeichenfolgen für andere Anwendungen gemeinsam zu verwenden. Anstatt tatsächliche Zeichenfolgen zu übergeben, übergibt eine DDE-Anwendung globale Atome an ihre Partneranwendung. Der Partner verwendet die Atome, um die Zeichenfolgen aus der Atomtabelle zu erhalten.

Anwendungen können lokale Atomtabellen verwenden, um eigene Elementnamenzuordnungen zu speichern.

Das System verwendet Atomtabellen, auf die Anwendungen nicht direkt zugriffen können. Die Anwendung verwendet diese Atome jedoch beim Aufrufen einer Vielzahl von Funktionen. Beispielsweise werden registrierte Zwischenablageformate in einer internen Atomtabelle gespeichert, die vom System verwendet wird. Eine Anwendung fügt dieser Atomtabelle mithilfe der [**RegisterClipboardFormat-Funktion Atome**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) hinzu. Außerdem werden registrierte Klassen in einer internen Atomtabelle gespeichert, die vom System verwendet wird. Eine Anwendung fügt dieser Atomtabelle mithilfe der [**RegisterClass-**](/windows/desktop/api/winuser/nf-winuser-registerclassa) oder [**RegisterClassEx-Funktion Atome**](/windows/desktop/api/winuser/nf-winuser-registerclassexa) hinzu.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Globale Atom-Tabelle](#global-atom-table)
-   [User Atom-Tabelle](#user-atom-table)
-   [Lokale Atom-Tabellen](#local-atom-tables)
-   [Atom-Typen](#atom-types)
    -   [Zeichenfolgenatome](#string-atoms)
    -   [Ganzzahlige Atome](#integer-atoms)
-   [Atomerstellung und Nutzungsanzahl](#atom-creation-and-usage-count)
-   [Atom-Table-Abfragen](#atom-table-queries)
-   [Atom-Zeichenfolgenformate](#atom-string-formats)

## <a name="global-atom-table"></a>Globale Atom-Tabelle

Die globale Atomtabelle ist für alle Anwendungen verfügbar. Wenn eine Anwendung eine Zeichenfolge in der globalen Atomtabelle platziert, generiert das System ein Atom, das im gesamten System eindeutig ist. Jede Anwendung mit dem Atom kann die identifizierte Zeichenfolge abrufen, indem sie die globale Atomtabelle abfragt.

Eine Anwendung, die ein privates DDE-Datenformat für die Freigabe von Daten für andere Anwendungen definiert, sollte den Formatnamen in der globalen Atomtabelle platzieren. Diese Technik verhindert Konflikte mit den Namen von Formaten, die vom System oder von anderen Anwendungen definiert werden, und macht die Bezeichner (Atome) für die Nachrichten oder Formate für die anderen Anwendungen verfügbar.

## <a name="user-atom-table"></a>User Atom-Tabelle

Zusätzlich zur globalen Atomtabelle ist die Benutzer-Atomtabelle eine weitere Atomtabelle des Systems, die auch für alle Prozesse freigegeben wird. Die Benutzer-Atomtabelle wird für eine kleine Anzahl von internen Szenarien für win32k verwendet. Beispielsweise Windows-Modulnamen, bekannte Zeichenfolgen in win32k, OLE-Formaten usw. Obwohl Anwendungen nicht direkt mit der Atomtabelle des Benutzers interagieren, rufen sie mehrere APIs wie [RegisterClass,](/windows/win32/api/winuser/nf-winuser-registerclassexa) [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)und [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)auf, die der Atomtabelle des Benutzers Einträge hinzufügen. Die von hinzugefügten Einträge `RegisterClass` können von gelöscht `UnregisterClass` werden. Die von und hinzugefügten Einträge werden jedoch `RegisterWindowMessage` `RegisterClipboardFormat` erst gelöscht, nachdem die Sitzung beendet wurde. Wenn die Benutzer-Atomtabelle keinen Speicherplatz mehr hat und die übergebene Zeichenfolge nicht bereits in der Tabelle enthalten ist, schlägt der Aufruf fehl. 

### <a name="atom-table-size"></a>Atom-Tabellengröße
 
Viele wichtige APIs, einschließlich [CreateWindow,](/windows/win32/api/winuser/nf-winuser-createwindowa)basieren auf Benutzer-Atomen. Aus diesem Grund führt die Speicherplatzerschöpfung in der Benutzer-Atomtabelle zu schwerwiegenden Problemen. Beispielsweise können alle Anwendungen möglicherweise nicht gestartet werden. Im Folgenden finden Sie einige Empfehlungen, um sicherzustellen, dass Ihre Anwendung Atomtabellen effizient nutzt und die Zuverlässigkeit und Leistung der Anwendung und des Systems bei behält:  

1. Sie sollten die Nutzung der Benutzer-Atomtabelle durch Ihre App einschränken. Das Speichern eindeutiger Zeichenfolgen mitHILFE von APIs wie `RegisterClass` , oder nimmt Speicherplatz in der `RegisterWindowMessage` `RegisterClipboardFormat` Atomtabelle des Benutzers ein, die global von anderen Apps verwendet wird, um Fensterklassen mithilfe von Zeichenfolgen zu registrieren. Wenn möglich, sollten Sie [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw)DeleteAtom verwenden, / [](/windows/desktop/api/Winbase/nf-winbase-deleteatom) um Zeichenfolgen in einer lokalen Atomtabelle zu speichern, oder [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom,](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) wenn die Atome prozessübergreifend benötigt werden.

1. Wenn bedenken, dass die Anwendung Probleme mit der Atomtabelle des Benutzers verursacht, können Sie die Grundursache untersuchen, indem Sie den Kerneldebugger verbinden und bei Aufrufen von ( ) in den Prozess `UserAddAtomEx` `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` einbrechen. Suchen Sie `user32!` in der Aufrufstapel nach , um zu sehen, welche API aufgerufen wird. Die Methodik ähnelt der Problemerkennung bei globalen Atomtabellen, die unter [Identifying Global Atom Table Leaks (Identifizieren von globalen Atomtabellenverlusten)](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks)erläutert wird. Eine weitere Möglichkeit, den Inhalt der Benutzer-Atomtabelle zu speichern, besteht [darin, GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) über den Bereich möglicher Atome von 0xC000 bis 0xFFFF aufzurufen. Wenn die Gesamtanzahl der Atome stetig steigt, während die Anwendung ausgeführt wird, oder nicht zur Baseline zurückkehrt, wenn die App geschlossen wird, liegt ein Problem vor.

## <a name="local-atom-tables"></a>Lokale Atomtabellen

Eine Anwendung kann eine lokale Atomtabelle verwenden, um eine große Anzahl von Zeichenfolgen effizient zu verwalten, die nur innerhalb der Anwendung verwendet werden. Diese Zeichenfolgen und die zugeordneten Atome sind nur für die Anwendung verfügbar, die die Tabelle erstellt hat.

Eine Anwendung, die dieselbe Zeichenfolge in einer Reihe von Strukturen erfordert, kann die Speicherauslastung mithilfe einer lokalen Atomtabelle reduzieren. Anstatt die Zeichenfolge in jede Struktur zu kopieren, kann die Anwendung die Zeichenfolge in der Atomtabelle platzieren und das resultierende Atom in die Strukturen einschließen. Auf diese Weise wird eine Zeichenfolge nur einmal im Arbeitsspeicher angezeigt, kann aber mehrmals in der Anwendung verwendet werden.

Anwendungen können auch lokale Atomtabellen verwenden, um Zeit bei der Suche nach einer bestimmten Zeichenfolge zu sparen. Um eine Suche durchzuführen, muss eine Anwendung nur die Suchzeichenfolge in der Atomtabelle platzieren und das resultierende Atom mit den Atomen in den relevanten Strukturen vergleichen. Der Vergleich von Atomen ist in der Regel schneller als das Vergleichen von Zeichenfolgen.

Atom-Tabellen werden als Hashtabellen implementiert. Standardmäßig verwendet eine lokale Atomtabelle 37 Buckets für ihre Hashtabelle. Sie können jedoch die Anzahl der verwendeten Buckets ändern, indem Sie die [**InitAtomTable-Funktion**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) aufrufen. Wenn die Anwendung **InitAtomTable** aufruft, muss sie dies jedoch tun, bevor andere Atomverwaltungsfunktionen aufgerufen werden.

## <a name="atom-types"></a>Atom-Typen

Anwendungen können zwei Typen von Atomen erstellen: Zeichenfolgen-Atome und ganzzahlige Atome. Die Werte von ganzzahligen Atomen und Zeichenfolgenatomen überlappen sich nicht, sodass beide Typen von Atomen im gleichen Codeblock verwendet werden können.

Mehrere Funktionen akzeptieren entweder Zeichenfolgen oder Atome als Parameter. Wenn ein Atom an diese Funktionen übergeben wird, kann eine Anwendung das [**MAKEINTATOM-Makro**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) verwenden, um das Atom in ein Formular zu konvertieren, das von der Funktion verwendet werden kann.

In den folgenden Abschnitten werden Atomtypen beschrieben.

-   [Zeichenfolgenatome](#string-atoms)
-   [Ganzzahlige Atome](#integer-atoms)

### <a name="string-atoms"></a>Zeichenfolgenatome

Wenn Anwendungen auf NULL terminierte Zeichenfolgen an die [**Funktionen GlobalAddAtom,**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) [**AddAtom,**](/windows/desktop/api/Winbase/nf-winbase-addatomw) [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)und [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) übergeben, erhalten sie Zeichenfolgenatome (16-Bit-Ganzzahlen) als Rückgabe.  Zeichenfolgenatome verfügen über die folgenden Eigenschaften:

-   Die Werte von Zeichenfolgenatomen liegen im Bereich 0xC000 (MAXINTATOM) bis 0xFFFF.
-   Der Fall ist bei der Suche nach einem Atomnamen in einer Atomtabelle nicht von Bedeutung. Außerdem muss die gesamte Zeichenfolge in einem Suchvorgang übereinstimmen. Es wird kein Abgleich von Teilzeichenfolgen ausgeführt.
-   Die einem Zeichenfolgenatom zugeordnete Zeichenfolge darf nicht mehr als 255 Byte groß sein. Diese Einschränkung gilt für alle Atomfunktionen.
-   Jedem *Atomnamen* ist eine Verweisanzahl zugeordnet. Die Anzahl wird jedes Mal erhöht, wenn der Atomname der Tabelle hinzugefügt und jedes Mal dekrementiert wird, wenn der Atomname daraus gelöscht wird. Dadurch wird verhindert, dass verschiedene Benutzer desselben Zeichenfolgenatoms die Atomnamen des jeweils anderen zerstören. Wenn der Verweiszähler für einen Atomnamen gleich 0 (null) ist, entfernt das System das Atom und den Atomnamen aus der Tabelle.

### <a name="integer-atoms"></a>Ganzzahlige Atome

Ganzzahlige Atome unterscheiden sich wie folgt von Zeichenfolgenatomen:

-   Die Werte ganzzahliger Atome liegen im Bereich 0x0001 bis 0xBFFF (**MAXINTATOM**– 1).
-   Die Zeichenfolgendarstellung eines ganzzahligen \# Atoms *ist dddd,* wobei die von *dddd dargestellten* Werte Dezimalziffern sind. Führende Nullen werden ignoriert.
-   Einem ganzzahligen Atom ist kein Verweiszähler oder Speicheraufwand zugeordnet.

## <a name="atom-creation-and-usage-count"></a>Atomerstellung und Nutzungsanzahl

Eine Anwendung erstellt ein lokales Atom durch Aufrufen der [**AddAtom-Funktion.**](/windows/desktop/api/Winbase/nf-winbase-addatomw) Er erstellt ein globales Atom durch Aufrufen der [**GlobalAddAtom-Funktion.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) Beide Funktionen erfordern einen Zeiger auf eine Zeichenfolge. Das System durchsucht die entsprechende Atomtabelle nach der Zeichenfolge und gibt das entsprechende Atom an die Anwendung zurück. Wenn sich die Zeichenfolge bereits in der Atomtabelle befindet, erhöht das System im Falle eines Zeichenfolgenatoms den Verweiszähler für die Zeichenfolge während dieses Prozesses.

Wiederholte Aufrufe zum Hinzufügen des gleichen Atomnamens geben dasselbe Atom zurück. Wenn der Atomname nicht in der Tabelle vorhanden ist, wenn [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) aufgerufen wird, wird der Atomname der Tabelle hinzugefügt, und ein neues Atom wird zurückgegeben. Wenn es sich um ein Zeichenfolgenatom handelt, wird die Verweisanzahl ebenfalls auf 1 festgelegt.

Eine Anwendung sollte die [**DeleteAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) aufrufen, wenn sie kein lokales Atom mehr verwenden muss. Sie sollte die [**GlobalDeleteAtom-Funktion aufrufen,**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) wenn sie kein globales Atom mehr benötigt. Im Fall eines Zeichenfolgenatoms reduziert eine dieser Funktionen die Verweisanzahl des entsprechenden Atoms um eins. Wenn die Verweisanzahl null erreicht, löscht das System den Atomnamen aus der Tabelle.

Der Atomname eines Zeichenfolgenatoms verbleibt in der globalen Atomtabelle, solange der Verweiszähler größer als 0 (null) ist, auch nachdem die Anwendung, die es in der Tabelle platziert hat, beendet wurde. Eine lokale Atomtabelle wird zerstört, wenn die zugeordnete Anwendung beendet wird, unabhängig von der Verweisanzahl der Atome in der Tabelle.

## <a name="atom-table-queries"></a>Atom-Table Abfragen

Eine Anwendung kann mithilfe der [**Funktion FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) oder [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) bestimmen, ob sich eine bestimmte Zeichenfolge bereits in einer Atomtabelle befindet. Diese Funktionen durchsuchen eine Atomtabelle nach der angegebenen Zeichenfolge und geben das entsprechende Atom zurück, wenn die Zeichenfolge vorhanden ist.

Eine Anwendung kann die Funktion [**GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) oder [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) verwenden, um eine Atomnamenzeichenfolge aus einer Atomtabelle abzurufen, vorausgesetzt, die Anwendung verfügt über das Atom, das der gesuchten Zeichenfolge entspricht. Beide Funktionen kopieren die Atomnamenzeichenfolge des angegebenen Atoms in einen Puffer und geben die Länge der kopierten Zeichenfolge zurück. **GetAtomName** ruft eine Atomnamenzeichenfolge aus einer lokalen Atomtabelle ab, und **GlobalGetAtomName** ruft eine Atomnamenzeichenfolge aus der globalen Atomtabelle ab.

## <a name="atom-string-formats"></a>Atom-Zeichenfolgenformate

Die Funktionen [**AddAtom,**](/windows/desktop/api/Winbase/nf-winbase-addatomw) [**GlobalAddAtom,**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)und [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) verwenden einen Zeiger auf eine auf NULL endende Zeichenfolge. Eine Anwendung kann diesen Zeiger auf eine der folgenden Arten angeben.



|     Zeichenfolgenformat               |    Beschreibung                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*Dddd*           | Eine ganze Zahl, die als Dezimalzeichenfolge angegeben ist. Wird zum Erstellen oder Suchen eines ganzzahligen Atoms verwendet.                  |
| *Zeichenfolgen-Atomname* | Ein Zeichenfolgen-Atomname. Wird verwendet, um einer Atomtabelle einen Zeichenfolgen-Atomnamen hinzuzufügen und als Rückgabe ein Atom zu empfangen. |



 

 

 
