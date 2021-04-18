---
description: ICE23 überprüft die Aktivier Reihenfolge der Steuerelemente für jedes Dialogfeld.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368025"
---
# <a name="ice23"></a>ICE23

ICE23 überprüft die Aktivier Reihenfolge der Steuerelemente für jedes Dialogfeld.

ICE23 überprüft Folgendes in der Dialog Feld [Tabelle](dialog-table.md) und der [Steuerelement Tabelle](control-table.md):

-   Jeder Datensatz in der Dialogfeld Tabelle gibt ein Steuerelement in der ersten Spalte des Steuer Elements an \_ , das im Dialogfeld vorhanden ist, das in der Dialogfeld Spalte angegeben ist.
-   Jeder Datensatz in der Steuerelement Tabelle gibt ein Steuerelement in der \_ nächsten Spalte des Steuer Elements an, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das in der Steuerelement Spalte aufgelistet ist, oder \_ das nächste Steuerelement enthält den Nullwert
-   Nach den nachfolgendes Steuerelementen des Steuer Elements in der Steuerelement \_ Tabelle wird eine einzelne, geschlossene Schleife erstellt, die zum ursprünglichen Steuerelement zurückkehrt. Nicht jedes Steuerelement muss sich in der Schleife befinden, aber die Schleife muss jedes Steuerelement durchlaufen, das über einen Eintrag in der nächsten Spalte des Steuer Elements verfügt \_ .

## <a name="result"></a>Ergebnis

ICE23 gibt eine Fehlermeldung aus, wenn die Aktivier Reihenfolge der Steuerelemente im Dialogfeld keine einzelne geschlossene Schleife bildet.

## <a name="example"></a>Beispiel

ICE23 gibt die folgenden Fehlermeldungen für das gezeigte Beispiel an.

-   Dialog1 hat nicht zuerst das Steuerelement \_ .
-   Control \_ First von Dialog Dialog2 bezieht sich auf das nicht vorhandene Steuerelement controlx.
-   Dialog3 hat die Reihenfolge der aktivierbaren Registerkarten bei Steuerungs kontrolllb.
-   Dialog4 hat eine falsch formatierte Aktivier Reihenfolge bei Steuerungs kontrolllc
-   Dialog5 hat eine falsch formatierte Aktivier Reihenfolge bei Steuerungs kontrolllc.
-   Das Steuerelement \_ neben Control Dialog6. controlc ist mit einem unbekannten Steuerelement verknüpft.

[Dialog Feld Tabelle](dialog-table.md) (teilweise)



| Dialog  | \_Zuerst Steuern |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | Controlx       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[Control-Tabelle](control-table.md) (partiell)



| Dialog  | Control  | Nächstes Steuerelement \_ |
|---------|----------|---------------|
| Dialog1 | ControlA |               |
| Dialog1 | Controlb | ControlA      |
| Dialog2 | ControlA | Controlb      |
| Dialog2 | Controlb | ControlA      |
| Dialog3 | ControlA | Controlb      |
| Dialog3 | Controlb |               |
| Dialog4 | ControlA | Controlb      |
| Dialog4 | Controlb | Controlc      |
| Dialog4 | Controlc | Controlb      |
| Dialog5 | ControlA | Controlb      |
| Dialog5 | Controlb | Controlc      |
| Dialog5 | Controlc | ControlA      |
| Dialog5 | ControlD | ControlA      |
| Dialog6 | ControlA | Controlb      |
| Dialog6 | Controlb | Controlc      |
| Dialog6 | Controlc | Controlx      |
| Dialog6 | ControlD | ControlA      |



 

Beachten Sie die folgenden Tabellen, um diese Fehler zu beheben, und nehmen Sie die angezeigten Änderungen vor.

Nicht jede Zeile in der Dialog Tabelle verfügt über ein Steuerelement, das in der ersten Spalte des Steuer Elements angegeben ist \_ . Ändern Sie die Control \_ First-Spalte des Dialog1-Datensatzes in der Dialog Feld Tabelle in ein Steuerelement, das in Dialog1 vorhanden ist.

Nicht jede Zeile in der Dialogfeld Tabelle verfügt über ein Steuerelement, das in der ersten Spalte des Steuer Elements angegeben ist \_ , die im Dialog Feld vorhanden ist. Ändern Sie die Control \_ First-Spalte des Dialog2 in ein Steuerelement, das in Dialog2 vorhanden ist.

Nach dem Steuern der \_ nächsten Einträge in der Steuerelement Tabelle von Steuerelement zu Steuerelement wird in jedem Fall keine geschlossene Schleife durchlaufen. Ändern Sie das Steuerelement \_ Next column for controlb in Dialog3 to ControlA.

Nach dem Steuern der Steuerelemente \_ in der Steuerelement Tabelle von Steuerelement zu Steuerelement wird in jedem Fall nicht mehr auf das ursprüngliche Steuerelement zurückgeführt. Ändern Sie das Steuerelement \_ Next column for controlc in Dialog4, um auf ControlA zu verweisen.

Wenn Sie das Steuerelement \_ Nächste Einträge in der Steuerelement Tabelle von Steuerelement zu Steuerung befolgen, werden nicht alle Steuerelemente im Dialogfeld durch einen Eintrag in der nächsten Spalte des-Steuer Elements weitergeleitet \_ . Ändern Sie das Steuerelement \_ Next column for controlc in Dialog5 to ControlD.

Das \_ nächste Steuerelement verweist nicht auf ein gültiges Steuerelement, das sich im gleichen Dialogfeld wie das Steuerelement befindet, das in der Steuerelement Spalte aufgelistet ist. Ändern Sie das Steuerelement \_ Next column for controlc in Dialog6, um auf ControlD zu verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



