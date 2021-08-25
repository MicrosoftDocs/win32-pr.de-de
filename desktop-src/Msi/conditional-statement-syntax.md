---
description: In diesem Abschnitt wird die Syntax von bedingten Anweisungen beschrieben, die von der MsiEvaluateCondition-Funktion und den Aktionssequenztabellen verwendet werden. Weitere Informationen finden Sie unter Beispiele für die Syntax bedingter Anweisungen.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Syntax für bedingte Anweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfea7ec31cecbe9c72dee9c660b0e6ee9d07cee2f1818941d036a781c104a93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077960"
---
# <a name="conditional-statement-syntax"></a>Syntax für bedingte Anweisungen

In diesem Abschnitt wird die Syntax von bedingten Anweisungen beschrieben, die von der [**MsiEvaluateCondition-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) und den Aktionssequenztabellen [verwendet werden.](using-a-sequence-table.md) Weitere Informationen finden Sie unter [Beispiele für die Syntax für bedingte Anweisungen.](examples-of-conditional-statement-syntax.md)

## <a name="summary-of-conditional-statement-syntax"></a>Zusammenfassung der Syntax für bedingte Anweisungen

In dieser Tabelle und der folgenden Liste wird die Syntax zusammengefasst, die in bedingten Ausdrücken verwendet werden soll.



| Element                | Syntax                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| Wert               | \|Symbolliteral \| ganze Zahl                                                                                    |
| comparison-operator | < \| > \| <= \| >= \| = \| <>                                                                 |
| Begriff                | value \| value comparison-operator value \| ( expression )\|                                                    |
| Boolescher Faktor      | Begriff \| **NOT-Begriff**                                                                                            |
| Boolescher Begriff        | Boolean-factor \| Boolean-factor **AND** term                                                                   |
| expression          | Boolean-term \| Boolean-term **OR** expression                                                                  |
| Symbol              | Eigenschaft \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state |



 

-   Bei Symbolnamen und -werten wird die Kleinschreibung beachtet.
-   Bei Umgebungsvariablennamen wird die Schreibung nicht beachtet.
-   Literaltext muss in Anführungszeichen ("Text") eingeschlossen werden.
    > [!Note]  
    > Literaltext, der Anführungszeichen enthält, kann nicht in bedingungsbedingten Anweisungen verwendet werden, da es kein Escapezeichen für Anführungszeichen im Literaltext gibt. Um einen Vergleich mit literalem Text mit Anführungszeichen zu erstellen, sollte der Literaltext in eine -Eigenschaft eingefügt werden. Um beispielsweise zu überprüfen, ob die SERVERNAME-Eigenschaft keine Anführungszeichen enthält, definieren Sie eine Eigenschaft namens QUOTES in der [Property](property-table.md) -Tabelle mit dem Wert " und ändern die Bedingung in NOT SERVERNAME><QUOTES.

     

-   Nicht vorhandene Eigenschaftswerte werden als leere Zeichenfolgen behandelt.
-   Numerische Gleitkommawerte werden nicht unterstützt.
-   Operatoren und Rangfolge sind identisch mit in den Sprachen BASIC und SQL Sprachen.
-   Arithmetische Operatoren werden nicht unterstützt.
-   Klammern können verwendet werden, um die Rangfolge von Operatoren zu überschreiben.
-   Bei Operatoren wird die Schreibung nicht beachtet.
-   Bei Zeichenfolgenvergleichen führt eine Tilde "~", die dem Operator vorangestellt ist, einen Vergleich durch, bei dem die Schreibung nicht beachtet wird.
-   Der Vergleich einer ganzen Zahl mit einer Zeichenfolge oder einem Eigenschaftswert, der nicht in eine ganze Zahl konvertiert werden kann, ist immer **msiEvaluateConditionFalse,** mit Ausnahme des Vergleichsoperator "<>", der **msiEvaluateConditionTrue zurückgibt.**

## <a name="access-prefixes"></a>Zugriffspräfixe

Die folgende Tabelle zeigt die Präfixe, die für den Zugriff auf verschiedene System- und Installationsprogramminformationen für die Verwendung in bedingten Ausdrücken verwendet werden.



| Symboltyp          | Präfix | Wert                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Installer-Eigenschaft   | (none) | Der Wert der Property -Tabelle[(-Eigenschaft).](property-table.md) |
| Umgebungsvariable | %      | Der Wert der Umgebungsvariablen.                            |
| Komponententabellenschlüssel  | $      | Aktionszustand der Komponente.                            |
| Komponententabellenschlüssel  | ?      | Installierter Zustand der Komponente.                         |
| Schlüssel der Featuretabelle    | &      | Aktionsstatus des Features.                              |
| Schlüssel der Featuretabelle    | !      | Installierter Zustand des Features.                           |



 

## <a name="logical-operators"></a>Logische Operatoren

Die folgende Tabelle zeigt die logischen Operatoren in bedingten Ausdrücken in der Reihenfolge von hoher bis niedriger Rangfolge.



| Operator | Bedeutung                                                 |
|----------|---------------------------------------------------------|
| Not      | Unärer Präfixoperator; invertiert den Status des folgenden Begriffs. |
| Und      | TRUE, wenn beide Begriffe TRUE sind.                            |
| oder       | TRUE, wenn einer oder beide Begriffe TRUE sind.                  |
| Xor      | TRUE, wenn einer der beiden Begriffe TRUE ist.             |
| Eqv      | TRUE, wenn beide Begriffe TRUE oder beide Begriffe FALSE sind.    |
| Imp      | TRUE, wenn der linke Begriff FALSE oder der rechte Begriff TRUE ist.       |



 

## <a name="comparative-operators"></a>Vergleichsoperatoren

Die folgende Tabelle zeigt die Vergleichsoperatoren, die in bedingten Ausdrücken verwendet werden. Diese Vergleichsoperatoren können nur zwischen zwei Werten auftreten.



| Operator | Bedeutung                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE, wenn der linke Wert gleich dem rechten Wert ist.                 |
| <> | TRUE, wenn der linke Wert nicht gleich dem rechten Wert ist.             |
| >     | TRUE, wenn der linke Wert größer als der rechte Wert ist.             |
| >=    | TRUE, wenn der linke Wert größer oder gleich dem rechten Wert ist. |
| <     | TRUE, wenn der linke Wert kleiner als der rechte Wert ist.                |
| <=    | TRUE, wenn der linke Wert kleiner oder gleich dem rechten Wert ist.    |



 

## <a name="substring-operators"></a>Teilzeichenfolgenoperatoren

Die folgende Tabelle zeigt die in bedingten Ausdrücken verwendeten Teilzeichenfolgenoperatoren. Teilzeichenfolgenoperatoren können zwischen zwei Zeichenfolgenwerten auftreten.



| Operator | Bedeutung                                           |
|----------|---------------------------------------------------|
| >< | TRUE, wenn die linke Zeichenfolge die rechte Zeichenfolge enthält.    |
| << | TRUE, wenn die linke Zeichenfolge mit der rechten Zeichenfolge beginnt. |
| >> | TRUE, wenn die linke Zeichenfolge mit der rechten Zeichenfolge endet.   |



 

## <a name="bitwise-numeric-operators"></a>Bitweise numerische Operatoren

Die folgende Tabelle zeigt die bitweisen numerischen Operatoren in bedingten Ausdrücken. Diese Operatoren können zwischen zwei ganzzahligen Werten auftreten.



| Operator | Bedeutung                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | Bitweises AND, TRUE, wenn die linke und rechte ganze Zahl Bits gemeinsam haben.    |
| << | TRUE, wenn die hohen 16 Bits der linken ganzen Zahl gleich der rechten ganzen Zahl sind. |
| >> | TRUE, wenn die unteren 16 Bits der linken ganzen Zahl gleich der rechten ganzen Zahl sind.  |



 

## <a name="feature-and-component-state-values"></a>Feature- und Komponentenzustandswerte

Die folgende Tabelle zeigt, wo die Verwendung der Funktions- und Komponentenoperatorsymbole gültig ist.



| Operator <state> | Wo diese Syntax gültig ist                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $component Aktion      | In der [Tabelle Bedingung](condition-table.md) und in den [Sequenztabellen](using-a-sequence-table.md) nach der [Aktion CostFinalize.](costfinalize-action.md) |
| &feature-action        | In der [Tabelle Bedingung](condition-table.md) und in den [Sequenztabellen](using-a-sequence-table.md) nach der [Aktion CostFinalize.](costfinalize-action.md) |
| !feature-state         | In der [Tabelle Bedingung](condition-table.md) und in den [Sequenztabellen](using-a-sequence-table.md) nach der [Aktion CostFinalize.](costfinalize-action.md) |
| ?Komponentenzustand       | In der [Tabelle Bedingung](condition-table.md) und in den [Sequenztabellen](using-a-sequence-table.md) nach der [Aktion CostFinalize.](costfinalize-action.md) |



 

Die folgende Tabelle zeigt die in bedingten Ausdrücken verwendeten Feature- und Komponentenzustandswerte. Diese Zustände werden erst festgelegt, wenn [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) entweder direkt oder durch die [Aktion CostFinalize aufgerufen](costfinalize-action.md) wird.



| State                    | Wert | Bedeutung                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ UNKNOWN    | –1    | Es ist keine Aktion für das Feature oder die Komponente zu ergreifen.              |
| INSTALLSTATE \_ ADVERTISED | 1     | Angekündigtes Feature. Dieser Zustand ist für Komponenten nicht verfügbar. |
| INSTALLSTATE \_ ABSENT     | 2     | Das Feature oder die Komponente ist nicht vorhanden.                            |
| INSTALLSTATE \_ LOCAL      | 3     | Feature oder Komponente auf dem lokalen Computer.                     |
| INSTALLSTATE \_ SOURCE     | 4     | Das Feature oder die Komponente wird aus der Quelle ausgeführt.                       |



 

Beispielsweise wird der bedingte Ausdruck "&MyFeature=3" nur dann als True ausgewertet, wenn MyFeature von seinem aktuellen Zustand in den Zustand der Installation auf dem lokalen Computer INSTALLSTATE LOCAL geändert \_ wird.

Beachten Sie, dass Sie nicht von der Bedingung $Component 1=3 abhängen sollten, um zu überprüfen, ob Component1 lokal auf dem Computer installiert ist. Dies kann fehlschlagen, wenn Component1 von mehr als einem Produkt installiert wird. Nachdem Component1 lokal von Product1 installiert wurde, wertet das Installationsprogramm die Bedingung $Component 1=3 während der Installation von Product2 als False aus. Dies liegt daran, dass das Installationsprogramm die Version der Komponente anhand des Schlüsselpfads der Komponente bestimmt und die Komponente für die Installation markiert, wenn ihre Version größer oder gleich der installierten Komponente ist.

Beachten Sie, dass das Installationsprogramm [](version.md) keine direkten Vergleiche des Versionsdatentyps in bedingungsbedingten Anweisungen vor nimmt. Sie können beispielsweise keine Vergleichsoperatoren verwenden, um Versionen wie "01.10" und "1.010" in einer bedingungsbedingten Anweisung zu vergleichen. Verwenden Sie stattdessen eine gültige -Methode, um nach einer Version zu suchen, wie unter Suchen nach vorhandenen [Anwendungen, Dateien,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)Registrierungseinträgen oder .ini-Dateieinträgen beschrieben, und legen Sie dann eine Eigenschaft fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften in bedingten Anweisungen](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



