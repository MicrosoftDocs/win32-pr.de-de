---
description: ICE23 überprüft die Reihenfolge der Steuerregisterkarten für jedes Dialogfeld.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbab2d50c07fce208edc845e64cff0061f513c102a55da2d56b49c4a4c17e867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529000"
---
# <a name="ice23"></a>ICE23

ICE23 überprüft die Reihenfolge der Steuerregisterkarten für jedes Dialogfeld.

ICE23 überprüft Folgendes in der [Tabelle Dialog](dialog-table.md) und in der [Tabelle Control](control-table.md):

-   Jeder Datensatz in der Tabelle Dialog gibt ein Steuerelement in der Spalte Control \_ First an, das in dem von der Spalte Dialog angegebenen Dialogfeld vorhanden ist.
-   Dass jeder Datensatz in der Control-Tabelle ein Steuerelement in der Control Next -Spalte angibt, das sich \_ im selben Dialogfeld wie das in der Control -Spalte aufgeführte Steuerelement befindet, oder Control \_ Next den NULL-Wert enthält.
-   Dadurch, dass nach den \_ Control Next-Einträgen von Steuerelement zu Steuerelement in der Control-Tabelle eine einzelne, geschlossene Schleife entsteht, die zum ursprünglichen Steuerelement zurückkommt. Nicht jedes Steuerelement muss sich in der Schleife befinden, aber die Schleife muss jedes Steuerelement durchlaufen, das über einen Eintrag in der Spalte Nächstes Steuerelement \_ verfügt.

## <a name="result"></a>Ergebnis

ICE23 sendet eine Fehlermeldung, wenn die Registerkartenreihenfolge von Steuerelementen keine einzelne geschlossene Schleife im Dialogfeld bildet.

## <a name="example"></a>Beispiel

ICE23 gibt die folgenden Fehlermeldungen für das gezeigte Beispiel aus.

-   Dialog1 verfügt über kein Control \_ First-Steuerelement.
-   Control \_ First of dialog Dialog2 bezieht sich auf ein nicht vorhandenes Steuerelement ControlX.
-   Dialog3 verfügt über die Tabstoppreihenfolge für das ungeordnete Ende des Steuerelements ControlB.
-   Dialog4 verfügt über eine falsch formatierte Registerkartenreihenfolge im ControlC-Steuerelement.
-   Dialog5 verfügt über eine falsch formatierte Registerkartenreihenfolge im ControlC-Steuerelement.
-   Steuerelement \_ Next of control Dialog6.ControlClinks to unknown control (Steuerelement Weiter des Steuerelements Dialog6.ControlC) ist mit einem unbekannten Steuerelement verknüpft.

[Dialogtabelle](dialog-table.md) (partiell)



| Dialog  | Zuerst \_ steuern |
|---------|----------------|
| Dialogfeld1 |                |
| Dialog2 | ControlX       |
| Dialogfeld3 | Controla       |
| Dialog4 | Controla       |
| Dialogfeld5 | Controla       |



 

[Steuertabelle](control-table.md) (partiell)



| Dialog  | Control  | Nächste \_ Steuerung |
|---------|----------|---------------|
| Dialogfeld1 | Controla |               |
| Dialogfeld1 | ControlB | Controla      |
| Dialog2 | Controla | ControlB      |
| Dialog2 | ControlB | Controla      |
| Dialogfeld3 | Controla | ControlB      |
| Dialogfeld3 | ControlB |               |
| Dialog4 | Controla | ControlB      |
| Dialog4 | ControlB | ControlC      |
| Dialog4 | ControlC | ControlB      |
| Dialogfeld5 | Controla | ControlB      |
| Dialogfeld5 | ControlB | ControlC      |
| Dialogfeld5 | ControlC | Controla      |
| Dialogfeld5 | ControlD | Controla      |
| Dialog6 | Controla | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | ControlD | Controla      |



 

Um diese Fehler zu beheben, beachten Sie Folgendes in den obigen Tabellen, und nehmen Sie die angegebenen Änderungen vor.

Nicht jede Zeile in der Dialogtabelle verfügt über ein Steuerelement, das in der Spalte Control First angegeben \_ ist. Ändern Sie die Spalte Control \_ First des Dialog1-Datensatzes in der Tabelle Dialog in ein Steuerelement, das in Dialog1 vorhanden ist.

Nicht jede Zeile in der Dialogtabelle verfügt über ein Steuerelement, das in der Spalte Control First angegeben \_ ist, die im Dialogfeld vorhanden ist. Ändern Sie die Spalte Control \_ First von Dialog2 in ein Steuerelement, das in Dialog2 vorhanden ist.

Das Befolgen der Einträge Control \_ Next in der Control-Tabelle von Steuerelement zu Steuerelement führt nicht in jedem Fall zu einer geschlossenen Schleife. Ändern Sie die Spalte Control \_ Next für ControlB in Dialog3 in ControlA.

Das Befolgen der Einträge Control \_ Next in der Control-Tabelle von Steuerelement zu Steuerelement führt nicht in jedem Fall zurück zum anfänglichen Steuerelement. Ändern Sie die Spalte Control \_ Next für ControlC in Dialog4, um auf ControlA zu verweisen.

Wenn Sie den Einträgen Control \_ Next in der Control-Tabelle von Steuerelement zu Steuerelement folgen, wird nicht jedes Steuerelement im Dialogfeld mit einem Eintrag in der Spalte Control \_ Next durchlaufen. Ändern Sie die Spalte Control \_ Next für ControlC in Dialog5 in ControlD.

Steuerelement \_ Weiter verweist nicht auf ein gültiges Steuerelement, das sich im selben Dialogfeld wie das in der Spalte Steuerelement aufgeführte Steuerelement befindet. Ändern Sie die Spalte Control \_ Next für ControlC in Dialog6, um auf ControlD zu verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



