---
title: Informationen zu Atom-Tabellen
description: In diesem Abschnitt werden Atom-Tabellen erläutert.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- Atome
- Atom-Tabellen
- Atom-Namen
- Dynamischer Datenaustausch (DDE), Atome
- DDE (dynamischer Datenaustausch), Atome
- globale Atom-Tabellen
- lokale Atom-Tabellen
- ganzzahlige Atome
- Zeichen folgen Atome
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 27f7cdb4bb2dc2fd97b4dba6909022b297df1a1d
ms.sourcegitcommit: e985e0532f0f895ae418e8c2658dac819cdae3b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "104391099"
---
# <a name="about-atom-tables"></a>Informationen zu Atom-Tabellen

Eine *Atom-Tabelle* ist eine System definierte Tabelle, in der Zeichen folgen und entsprechende Bezeichner gespeichert werden. Eine Anwendung platziert eine Zeichenfolge in eine Atom-Tabelle und empfängt eine 16-Bit-Ganzzahl, die als *Atom* bezeichnet wird und für den Zugriff auf die Zeichenfolge verwendet werden kann. Eine Zeichenfolge, die in eine Atom-Tabelle eingefügt wurde, wird als *Atom-Name* bezeichnet.

Das System stellt eine Reihe von Atom-Tabellen bereit. Jede Atom-Tabelle dient einem anderen Zweck. Beispielsweise verwenden dynamischer Datenaustausch (DDE)-Anwendungen die [globale Atom-Tabelle](#global-atom-table) , um Elementname-und Topic-Name-Zeichen folgen für andere Anwendungen freizugeben. Anstatt tatsächliche Zeichen folgen zu übergeben, übergibt eine DDE-Anwendung globale Atome an die Partner Anwendung. Der Partner verwendet die Atome zum Abrufen der Zeichen folgen aus der Atom-Tabelle.

Anwendungen können lokale Atom-Tabellen verwenden, um Ihre eigenen Element namens Zuordnungen zu speichern.

Das System verwendet Atom-Tabellen, auf die Anwendungen nicht direkt zugreifen können. Die Anwendung verwendet diese Atome jedoch, wenn eine Vielzahl von Funktionen aufgerufen wird. Beispielsweise werden registrierte Zwischenablage Formate in einer internen Atom-Tabelle gespeichert, die vom System verwendet wird. Eine Anwendung fügt dieser Atom-Tabelle mithilfe der [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) -Funktion Atome hinzu. Außerdem werden registrierte Klassen in einer internen Atom-Tabelle gespeichert, die vom System verwendet wird. Eine Anwendung fügt dieser Atom-Tabelle mithilfe der [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion oder der [**RegisterClassEx**](/windows/desktop/api/winuser/nf-winuser-registerclassexa) -Funktion Atome hinzu.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Globale Atom-Tabelle](#global-atom-table)
-   [Benutzer-Atom-Tabelle](#user-atom-table)
-   [Lokale Atom-Tabellen](#local-atom-tables)
-   [Atom-Typen](#atom-types)
    -   [Zeichen folgen Atome](#string-atoms)
    -   [Ganzzahlige Atome](#integer-atoms)
-   [Atom-Erstellung und Verwendungs Anzahl](#atom-creation-and-usage-count)
-   [Atom-Tabellen Abfragen](#atom-table-queries)
-   [Atom-Zeichen folgen Formate](#atom-string-formats)

## <a name="global-atom-table"></a>Globale Atom-Tabelle

Die globale Atom-Tabelle ist für alle Anwendungen verfügbar. Wenn eine Anwendung eine Zeichenfolge in der globalen Atom-Tabelle platziert, generiert das System ein Atom, das im gesamten System eindeutig ist. Jede Anwendung, die über das Atom-Atom verfügt, kann die von ihr identifizierte Zeichenfolge durch Abfragen der globalen Atom-Tabelle abrufen.

Eine Anwendung, die ein privates DDE-Datenformat für die gemeinsame Nutzung von Daten mit anderen Anwendungen definiert, sollte den Format Namen in der globalen Atom-Tabelle platzieren. Diese Methode verhindert Konflikte mit den Namen von Formaten, die vom System oder von anderen Anwendungen definiert werden, und macht die Bezeichner (Atome) für die Nachrichten oder Formate verfügbar, die für die anderen Anwendungen verfügbar sind.

## <a name="user-atom-table"></a>Benutzer-Atom-Tabelle

Zusätzlich zur globalen Atom-Tabelle ist die Benutzer-Atom-Tabelle eine weitere System-Atom-Tabelle, die auch für alle Prozesse freigegeben wird. Die Benutzer-Atom-Tabelle wird für eine kleine Anzahl von Szenarios verwendet, die intern für Win32k verwendet werden. beispielsweise Windows-Modulnamen, bekannte Zeichen folgen in Win32k, OLE-Formaten usw. Obwohl Anwendungen nicht direkt mit der Benutzer-Atom-Tabelle interagieren, werden mehrere APIs – z. b. [registerClass](/windows/win32/api/winuser/nf-winuser-registerclassexa), [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)und [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)– aufgerufen, die der Benutzer-Atom-Tabelle Einträge hinzufügen. Die von hinzugefügten Einträge `RegisterClass` können von gelöscht werden `UnregisterClass` . Die von hinzugefügten Einträge `RegisterWindowMessage` `RegisterClipboardFormat` werden jedoch erst gelöscht, wenn die Sitzung beendet wird. Wenn die Benutzer-Atom-Tabelle keinen Speicherplatz mehr aufweist und die Zeichenfolge, die Sie weitergibt, nicht bereits in der Tabelle vorhanden ist, tritt ein Fehler auf. 

### <a name="atom-table-size"></a>Atom-Tabellengröße
 
Viele wichtige APIs, einschließlich " [kreatewindow](/windows/win32/api/winuser/nf-winuser-createwindowa)", basieren auf Benutzer Atomen. Aus diesem Grund führt die Speicherauslastung in der Benutzer-Atom-Tabelle zu schwerwiegenden Problemen. Beispielsweise können alle Anwendungen nicht gestartet werden. Im folgenden finden Sie einige Empfehlungen, um sicherzustellen, dass Ihre Anwendung Atom-Tabellen effizient nutzt und die Zuverlässigkeit und Leistung der Anwendung und des Systems beibehält:  

1. Sie sollten die Verwendung der Benutzer-Atom-Tabelle für Ihre APP einschränken. Das Speichern von eindeutigen Zeichen folgen mithilfe von APIs wie `RegisterClass` , `RegisterWindowMessage` oder `RegisterClipboardFormat` nimmt Platz in der Benutzer-Atom-Tabelle, die von anderen apps Global zum Registrieren von Fenster Klassen mithilfe von Zeichen folgen verwendet wird. Wenn möglich, sollten Sie [addatom](/windows/desktop/api/Winbase/nf-winbase-addatomw) / [deleteatom](/windows/desktop/api/Winbase/nf-winbase-deleteatom) verwenden, um Zeichen folgen in einer lokalen Atom-Tabelle zu speichern, oder [globaladdatom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [globaldeleteatom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) , wenn die Atome Prozess übergreifend benötigt werden.

1. Wenn Sie Bedenken bezüglich der Anwendung haben, die Probleme mit der Atom-Tabelle der Benutzer verursacht, können Sie die Ursache untersuchen, indem Sie den Kernel Debugger verbinden und den Prozess bei Aufrufen von `UserAddAtomEx` () unterbrechen `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` . Suchen `user32!` Sie nach in der Aufruf Liste, um festzustellen, welche API aufgerufen wird. Die Methodik ähnelt der globalen Atom-Tabellen Problemerkennung, die unter [identifizieren globaler Atom-Tabellen Lecks](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks)erläutert wird. Eine andere Möglichkeit, den Inhalt der Atom-Benutzertabelle zu speichern, besteht darin, [getclipboardformatname](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) über den Bereich möglicher Atome zwischen 0xc000 und 0xFFFF aufzurufenden. Wenn die Gesamtanzahl der Atom-Anwendungen ständig steigt, während die Anwendung ausgeführt wird oder nicht an die Baseline zurückkehrt, wenn die app geschlossen wird, liegt ein Problem vor.

## <a name="local-atom-tables"></a>Lokale Atom-Tabellen

Eine Anwendung kann eine lokale Atom-Tabelle verwenden, um eine große Anzahl von Zeichen folgen, die nur innerhalb der Anwendung verwendet werden, effizient zu verwalten. Diese Zeichen folgen und die zugeordneten Atome sind nur für die Anwendung verfügbar, die die Tabelle erstellt hat.

Eine Anwendung, die dieselbe Zeichenfolge in einer Reihe von Strukturen benötigt, kann die Speicherauslastung mithilfe einer lokalen Atom-Tabelle verringern. Anstatt die Zeichenfolge in jede Struktur zu kopieren, kann die Anwendung die Zeichenfolge in der Atom-Tabelle platzieren und das resultierende Atom in die Strukturen einschließen. Auf diese Weise wird eine Zeichenfolge nur einmal im Arbeitsspeicher angezeigt, kann aber mehrmals in der Anwendung verwendet werden.

Anwendungen können auch lokale Atom-Tabellen verwenden, um Zeit zu sparen, wenn Sie nach einer bestimmten Zeichenfolge suchen. Zum Durchführen einer Suche muss eine Anwendung nur die Such Zeichenfolge in der Atom-Tabelle platzieren und das resultierende Atom mit den Atomen in den relevanten Strukturen vergleichen. Das Vergleichen von Atomen ist in der Regel schneller als das Vergleichen von Zeichen

Atom-Tabellen werden als Hash Tabellen implementiert. Standardmäßig verwendet eine lokale Atom-Tabelle 37-Bucket für die Hash Tabelle. Sie können jedoch die Anzahl der verwendeten Bucket ändern, indem Sie die [**initatomtable**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) -Funktion aufrufen. Wenn die Anwendung jedoch **initatomtable** aufruft, muss Sie dies tun, bevor andere Atom-Verwaltungsfunktionen aufgerufen werden.

## <a name="atom-types"></a>Atom-Typen

Anwendungen können zwei Arten von Atomen erstellen: Zeichen folgen Atome und ganzzahlige Atome. Die Werte ganzzahliger Atome und Zeichen folgen Atome überlappen sich nicht, daher können beide Typen von Atomen im gleichen Codeblock verwendet werden.

Mehrere Funktionen akzeptieren entweder Zeichen folgen oder Atome als Parameter. Wenn ein Atom an diese Funktionen übergeben wird, kann eine Anwendung das [**makeintatom**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) -Makro verwenden, um das Atom in ein Formular zu konvertieren, das von der Funktion verwendet werden kann.

In den folgenden Abschnitten werden Atom-Typen beschrieben.

-   [Zeichen folgen Atome](#string-atoms)
-   [Ganzzahlige Atome](#integer-atoms)

### <a name="string-atoms"></a>Zeichen folgen Atome

Wenn Anwendungen NULL-terminierte Zeichen folgen an die Funktionen [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**globalfindatom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)und [**findatom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) übergeben, erhalten Sie *Zeichen folgen Atome* (16-Bit-Ganzzahlen) im Rückgabewert. Zeichen folgen Atome verfügen über die folgenden Eigenschaften:

-   Die Werte von Zeichen folgen Atomen liegen im Bereich von 0xc000 (maxintatom) bis 0xFFFF.
-   Die Groß-/Kleinschreibung ist bei Suchen nach einem Atom-Namen in einer Atom-Tabelle nicht signifikant. Außerdem muss die gesamte Zeichenfolge in einem Suchvorgang entsprechen. Es wird keine Teil Zeichenfolgen-Übereinstimmung ausgeführt.
-   Die Zeichenfolge, die einem Zeichen folgen-Atom zugeordnet ist, darf nicht mehr als 255 Bytes groß sein. Diese Einschränkung gilt für alle Atom-Funktionen.
-   Jedem Atom-Namen ist ein *Verweis Zähler* zugeordnet. Die Anzahl wird jedes Mal erhöht, wenn der Atom-Name der Tabelle hinzugefügt und bei jedem Löschen des Atom-namens dekrementiert wird. Dadurch wird verhindert, dass unterschiedliche Benutzer desselben Zeichen folgen Atom die Atom-Namen der anderen zerstören. Wenn der Verweis Zähler für einen Atom-Namen gleich NULL ist, entfernt das System das Atom und den Atom-Namen aus der Tabelle.

### <a name="integer-atoms"></a>Ganzzahlige Atome

Ganzzahlige Atome unterscheiden sich folgendermaßen von Zeichen folgen Atomen:

-   Die Werte ganzzahliger Atome liegen im Bereich 0x0001 bis 0xbfff (**maxintatom**– 1).
-   Die Zeichen folgen Darstellung eines ganzzahligen Atom ist \# *dddd*, wobei die durch *dddd* dargestellten Werte Dezimalstellen sind. Führende Nullen werden ignoriert.
-   Einem ganzzahligen Atom ist kein Verweis Zähler oder Speicher Aufwand zugeordnet.

## <a name="atom-creation-and-usage-count"></a>Atom-Erstellung und Verwendungs Anzahl

Eine Anwendung erstellt ein lokales Atom durch Aufrufen der [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) -Funktion. Es wird ein globales Atom erstellt, indem die [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion aufgerufen wird. Beide Funktionen erfordern einen Zeiger auf eine Zeichenfolge. Das System durchsucht die entsprechende Atom-Tabelle nach der Zeichenfolge und gibt das entsprechende Atom an die Anwendung zurück. Wenn die Zeichenfolge in der Atom-Tabelle bereits vorhanden ist, erhöht das System bei einem Zeichen folgen Atom den Verweis Zähler für die Zeichenfolge während dieses Vorgangs.

Bei wiederholten Aufrufen zum Hinzufügen desselben Atom-namens wird dasselbe Atom zurückgegeben. Wenn der Atom-Name in der Tabelle nicht vorhanden ist, wenn [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) aufgerufen wird, wird der Atom-Name der Tabelle hinzugefügt, und ein neues Atom wird zurückgegeben. Wenn es sich um ein Zeichen folgen Atom handelt, wird sein Verweis Zähler ebenfalls auf einen Wert festgelegt.

Eine Anwendung sollte die [**deleteatom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) -Funktion aufrufen, wenn Sie kein lokales Atom mehr verwenden muss. die Funktion " [**globaldeleteatom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) " sollte aufgerufen werden, wenn ein globales Atom nicht mehr benötigt wird. Bei einem Zeichen folgen Atom reduziert eine dieser Funktionen den Verweis Zähler des entsprechenden Atom um 1. Wenn der Verweis Zähler Null erreicht, löscht das System den Atom-Namen aus der Tabelle.

Der Atom-Name einer Zeichen folgen-Atom verbleibt in der globalen Atom-Tabelle, solange der Verweis Zähler größer als 0 (null) ist, auch nachdem die Anwendung, die Sie in die Tabelle eingefügt hat, beendet wird. Eine lokale Atom-Tabelle wird zerstört, wenn die zugehörige Anwendung beendet wird, unabhängig von der Verweis Anzahl der Atome in der Tabelle.

## <a name="atom-table-queries"></a>Atom-Table Abfragen

Eine Anwendung kann mithilfe der Funktion [**findatom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) oder [**globalfindatom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) ermitteln, ob eine bestimmte Zeichenfolge bereits in einer Atom-Tabelle vorhanden ist. Diese Funktionen durchsuchen eine Atom-Tabelle nach der angegebenen Zeichenfolge und geben, wenn die Zeichenfolge vorhanden ist, das entsprechende Atom zurück.

Eine Anwendung kann die Funktion " [**getatomname**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) " oder " [**globalgetatomname**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) " verwenden, um eine Atom-Name-Zeichenfolge aus einer Atom-Tabelle abzurufen, vorausgesetzt, die Anwendung verfügt über das Atom, das der gesuchten Zeichenfolge entspricht. Beide Funktionen kopieren die Atom-Name-Zeichenfolge des angegebenen Atom in einen Puffer und geben die Länge der kopierten Zeichenfolge zurück. **Getatomname** Ruft eine Atom-Name-Zeichenfolge aus einer lokalen Atom-Tabelle ab, und **globalgetatomname** Ruft eine Atom-Name-Zeichenfolge aus der globalen Atom-Tabelle ab.

## <a name="atom-string-formats"></a>Atom-Zeichen folgen Formate

Die Funktionen " [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw)", " [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)", " [**findatom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)" und " [**globalfindatom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) " nehmen einen Zeiger auf eine mit NULL endenden Zeichenfolge an. Eine Anwendung kann diesen Zeiger auf eine der folgenden Weisen angeben.



|                    |                                                                                                    |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*dddd*           | Eine als Dezimal Zeichenfolge angegebene Ganzzahl. Wird verwendet, um ein ganz Zahl Atom zu erstellen oder zu suchen.                  |
| *Name der Zeichenfolge Atom* | Ein Zeichen folgen-Atom-Name. Wird verwendet, um einer Atom-Tabelle einen Atom-Zeichen folgen Namen hinzuzufügen und in Return ein Atom zu empfangen. |



 

 

 
