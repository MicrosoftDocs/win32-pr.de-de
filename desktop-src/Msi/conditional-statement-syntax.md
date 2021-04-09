---
description: In diesem Abschnitt wird die Syntax von bedingten Anweisungen beschrieben, die von der msievaluatecondition-Funktion und den Aktions Sequenz Tabellen verwendet werden. Weitere Informationen finden Sie unter Beispiele für bedingte Anweisungs Syntax.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Syntax der bedingten Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864408"
---
# <a name="conditional-statement-syntax"></a>Syntax der bedingten Anweisung

In diesem Abschnitt wird die Syntax von bedingten Anweisungen beschrieben, die von der [**msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) -Funktion und den Aktions [Sequenz Tabellen](using-a-sequence-table.md)verwendet werden. Weitere Informationen finden Sie unter [Beispiele für bedingte Anweisungs Syntax](examples-of-conditional-statement-syntax.md).

## <a name="summary-of-conditional-statement-syntax"></a>Zusammenfassung der Syntax der bedingten Anweisung

In dieser Tabelle und in der folgenden Liste wird die Syntax zusammengefasst, die in bedingten Ausdrücken verwendet werden soll.



| Element                | Syntax                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| value               | Symbol \| Literale \| Ganzzahl                                                                                    |
| Vergleichs Operator | < \| > \| <= \| >= \| = \| <>                                                                 |
| Begriff                | Wert \| Vergleichswert-Operator Wert \| (Ausdruck)\|                                                    |
| Boolescher Faktor      | Begriff " \| **nicht** Begriff"                                                                                            |
| Boolescher Ausdruck        | Boolescher Faktor \| **und** Begriff "boolescher Faktor"                                                                   |
| expression          | Boolescher Ausdruck ( \| boolescher Ausdruck **oder** Ausdruck)                                                                  |
| Symbol              | Eigenschaft " \| % Environment-Variable \| $Component-Action \| ? Component-State \| &Feature-Action \| ! Feature-State" |



 

-   Bei Symbol Namen und Werten wird Groß-/Kleinschreibung beachtet
-   Bei Umgebungsvariablen Namen wird Groß-/Kleinschreibung nicht beachtet
-   LiteralText muss in Anführungszeichen ("Text") eingeschlossen werden.
    > [!Note]  
    > LiteralText mit Anführungszeichen kann nicht in Bedingungs Anweisungen verwendet werden, da es kein Escapezeichen für Anführungszeichen innerhalb von Literaltext gibt. Um einen Vergleich mit Literaltext mit Anführungszeichen durchzuführen, sollte der Literaltext in eine Eigenschaft eingefügt werden. Um z. b. zu überprüfen, ob die ServerName-Eigenschaft keine Anführungszeichen enthält, definieren Sie eine Eigenschaft mit dem Namen Anführungszeichen in der [Eigenschaften Tabelle](property-table.md) mit dem Wert "", und ändern Sie die Bedingung in Not Servername><Anführungszeichen.

     

-   Nicht vorhandene Eigenschaftswerte werden als leere Zeichen folgen behandelt.
-   Numerische Gleit Komma Werte werden nicht unterstützt.
-   Operatoren und Rangfolge sind identisch mit denen in den Sprachen "Basic" und "SQL".
-   Arithmetische Operatoren werden nicht unterstützt.
-   Klammern können zum Überschreiben der Operator Rangfolge verwendet werden.
-   Bei Operatoren wird die Groß-/Kleinschreibung
-   Bei Zeichen folgen vergleichen führt eine Tilde, die dem Operator vorangestellt ist, einen Vergleich durch, bei dem die Groß-/Kleinschreibung nicht beachtet wird.
-   Der Vergleich einer Ganzzahl mit einer Zeichenfolge oder einem Eigenschafts Wert, der nicht in eine ganze Zahl konvertiert werden kann, ist immer **msievaluateconditionfalse**, mit Ausnahme des Vergleichs Operators "<>", der " **msievaluateconditiontrue**" zurückgibt.

## <a name="access-prefixes"></a>Zugriffs Präfixe

In der folgenden Tabelle sind die Präfixe aufgeführt, die für den Zugriff auf verschiedene System-und Installerinformationen zur Verwendung in bedingten Ausdrücken verwendet werden.



| Symboltyp          | Präfix | Wert                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Installereigenschaft   | (none) | Der Wert der Eigenschaften Tabelle ([Property](property-table.md)). |
| Umgebungsvariable | %      | Wert der Umgebungsvariablen.                            |
| Komponenten Tabellenschlüssel  | $      | Der Aktionszustand der Komponente.                            |
| Komponenten Tabellenschlüssel  | ?      | Installierter Status der Komponente.                         |
| Funktionstabellen Schlüssel    | &      | Der Aktionszustand des Features.                              |
| Funktionstabellen Schlüssel    | !      | Installierter Status des Features.                           |



 

## <a name="logical-operators"></a>Logische Operatoren

In der folgenden Tabelle werden die logischen Operatoren in bedingten Ausdrücken in der Reihenfolge, in der die Rangfolge hoch zu niedrig ist, angezeigt.



| Operator | Bedeutung                                                 |
|----------|---------------------------------------------------------|
| Not      | Unärer Präfix Operator; kehrt den Status des folgenden Begriffs um. |
| Und      | True, wenn beide Begriffe true sind.                            |
| oder       | True, wenn eine oder beide Begriffe den Wert true haben.                  |
| Xor      | True, wenn beide Bedingungen nicht erfüllt sind.             |
| Eqv      | True, wenn beide Begriffe true sind oder beide Begriffe false sind.    |
| IMP      | True, wenn der linke Begriff false ist oder der Rechte Begriff true ist.       |



 

## <a name="comparative-operators"></a>Vergleichs Operatoren

Die folgende Tabelle zeigt die Vergleichs Operatoren, die in bedingten Ausdrücken verwendet werden. Diese Vergleichs Operatoren können nur zwischen zwei Werten auftreten.



| Operator | Bedeutung                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE, wenn der linke Wert gleich dem richtigen Wert ist.                 |
| <> | TRUE, wenn der linke Wert nicht gleich dem richtigen Wert ist.             |
| >     | TRUE, wenn der linke Wert größer als der Rechte Wert ist.             |
| >=    | TRUE, wenn der linke Wert größer oder gleich dem rechten Wert ist. |
| <     | TRUE, wenn der linke Wert kleiner als der Rechte Wert ist.                |
| <=    | TRUE, wenn der linke Wert kleiner oder gleich dem rechten Wert ist.    |



 

## <a name="substring-operators"></a>Substring-Operatoren

In der folgenden Tabelle sind die Teil Zeichenfolge-Operatoren aufgeführt, die in bedingten Ausdrücken verwendet werden Substring-Operatoren können zwischen zwei Zeichen folgen Werten auftreten.



| Operator | Bedeutung                                           |
|----------|---------------------------------------------------|
| >< | TRUE, wenn die linke Zeichenfolge die Rechte Zeichenfolge enthält.    |
| << | TRUE, wenn die linke Zeichenfolge mit der rechten Zeichenfolge beginnt. |
| >> | TRUE, wenn die linke Zeichenfolge mit der rechten Zeichenfolge endet.   |



 

## <a name="bitwise-numeric-operators"></a>Bitweise numerische Operatoren

In der folgenden Tabelle werden die bitweisen numerischen Operatoren in bedingten Ausdrücken angezeigt. Diese Operatoren können zwischen zwei ganzzahligen Werten auftreten.



| Operator | Bedeutung                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | Bitweises and, true, wenn die linke und die Rechte Ganzzahl allgemeine Bits aufweisen.    |
| << | True, wenn die hohen 16 Bits der linken Ganzzahl gleich der rechten ganzen Zahl sind. |
| >> | True, wenn die unteren 16 Bits der linken Ganzzahl gleich der rechten ganzen Zahl sind.  |



 

## <a name="feature-and-component-state-values"></a>Funktions-und Komponenten Zustands Werte

In der folgenden Tabelle wird gezeigt, wo die Verwendung der Symbol-und Komponenten Operator Symbole gültig ist.



| KOM <state> | Wenn diese Syntax gültig ist                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $Component Aktion      | In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion. |
| &Feature-Aktion        | In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion. |
| ! Feature-State         | In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion. |
| ? Component-State       | In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion. |



 

In der folgenden Tabelle werden die Funktions-und Komponenten Zustands Werte aufgeführt, die in bedingten Ausdrücken verwendet werden. Diese Zustände werden erst festgelegt, wenn [**msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) entweder direkt oder durch die [costfinalize](costfinalize-action.md) -Aktion aufgerufen wird.



| State                    | Wert | Bedeutung                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| InstallState \_ unbekannt    | -1    | Es ist keine Aktion für das Feature oder die Komponente erforderlich.              |
| InstallState \_ angekündigt | 1     | Angekündigte Funktion. Dieser Status ist für Komponenten nicht verfügbar. |
| InstallState \_ fehlt.     | 2     | Die Funktion oder Komponente ist nicht vorhanden.                            |
| InstallState \_ lokal      | 3     | Feature oder Komponente auf dem lokalen Computer.                     |
| InstallState- \_ Quelle     | 4     | Funktion oder Komponente, die von der Quelle ausgeführt wird.                       |



 

Beispielsweise wird der bedingte Ausdruck "&myfeature = 3" nur dann zu "true" ausgewertet, wenn die Funktion "myfeature" von Ihrem aktuellen Zustand in den Zustand "", der auf dem lokalen Computer installiert ist, "InstallState local" geändert wird \_ .

Beachten Sie, dass Sie nicht auf die Bedingung $Component 1 = 3 angewiesen sind, um zu überprüfen, ob Component1 lokal auf dem Computer installiert ist. Dies kann fehlschlagen, wenn Component1 von mehr als einem Produkt installiert wird. Nachdem Component1 lokal von product1 installiert wurde, wertet das Installationsprogramm während der Installation von product2 die Bedingung $Component 1 = 3 als false aus. Dies liegt daran, dass das Installationsprogramm die Version der Komponente mithilfe des Schlüssel Pfads der Komponente bestimmt und die Komponente für die Installation markiert, wenn deren Version größer oder gleich der installierten Komponente ist.

Beachten Sie, dass das Installationsprogramm keine direkten Vergleiche des Datentyps [Version](version.md) in Bedingungs Anweisungen durchführt. Beispielsweise können Sie keine Vergleichs Operatoren verwenden, um Versionen wie "01,10" und "1,010" in einer Bedingungs Anweisung zu vergleichen. Verwenden Sie stattdessen eine gültige Methode für die Suche nach einer Version, z. b. in [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), und legen Sie dann eine Eigenschaft fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



