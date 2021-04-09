---
description: Die Bedingungs Tabelle kann verwendet werden, um den Auswahl Status eines beliebigen Eintrags in der Featuretabelle basierend auf einem bedingten Ausdruck zu ändern.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Bedingungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958739"
---
# <a name="condition-table"></a>Bedingungs Tabelle

Die Bedingungs Tabelle kann verwendet werden, um den Auswahl Status eines beliebigen Eintrags in der [Featuretabelle](feature-table.md) basierend auf einem bedingten Ausdruck zu ändern.

Die Bedingungs Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Funktion\_ | [Bezeichner](identifier.md) | J   | N        |
| Ebene     | [Integer](integer.md)       | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel in Spalte 1 der Featuretabelle.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Geringen
</dt> <dd>

Eine bedingte Installationsstufe für die Funktion in der \_ featurespalte der Tabelle. Der Installer legt die Installations Ebene dieses Features auf die in dieser Spalte angegebene Ebene fest, wenn der Ausdruck in der Spalte Bedingung als true ausgewertet wird.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Wenn dieser bedingte Ausdruck als true ausgewertet wird, wird die Spalte Ebene in der Featuretabelle auf die bedingte Installations Ebene festgelegt.

Der Ausdruck in der Spalte Bedingung sollte keinen Verweis auf den installierten Zustand eines Features oder einer Komponente enthalten. Dies liegt daran, dass die Ausdrücke in der Spalte Bedingung ausgewertet werden, bevor der Installer die installierten Status von Features und Komponenten auswertet. Jeder Ausdruck in der Bedingungs Tabelle, der versucht, den installierten Zustand eines Features oder einer Komponente zu überprüfen, wird immer auf "false" ausgewertet.

Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Funktion kann durch Festlegen der Ebene-Spalte auf 0 (null) dauerhaft deaktiviert werden.

Die Ebene kann basierend auf einer Bedingungs Anweisung festgelegt werden, z. b. ein Test für Plattform, Betriebssystem oder eine bestimmte Eigenschaften Einstellung.

Bedingungen sollten sorgfältig ausgewählt werden, damit eine Funktion bei der Deinstallation nicht aktiviert und dann deaktiviert wird. Dadurch wird das Feature verwaist, und das Produkt kann nicht deinstalliert werden.

Diese Tabelle wird beim Ausführen der [Aktion "costfinalize](costfinalize-action.md) " bezeichnet.

Wenn die [**vorab ausgewählte**](preselected.md) Eigenschaft auf 1 festgelegt wurde, wertet das Installationsprogramm die Bedingungs Tabelle nicht aus. Die Bedingungs Tabelle wirkt sich nur auf die Installation von-Funktionen aus, wenn keine der folgenden Eigenschaften festgelegt wurde:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**Aufgeh**](remove.md)  
[**Addsource**](addsource.md)  
[**Adddefault**](adddefault.md)  
[**Installieren Sie**](reinstall.md)  
[**Benen**](advertise.md)  
[**Compaddlocal**](compaddlocal.md)  
[**Compaddsource**](compaddsource.md)  
[**Compadddefault**](compadddefault.md)  
[**Fileaddlocal**](fileaddlocal.md)  
[**Fileaddsource**](fileaddsource.md)  
[**Fileadddefault**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



