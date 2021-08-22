---
description: Die Tabelle Bedingung kann verwendet werden, um den Auswahlzustand eines beliebigen Eintrags in der Feature-Tabelle basierend auf einem bedingten Ausdruck zu ändern.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Bedingungstabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d9ccb265d69f99a58e155657a0e9d058ba61a920088184ec2b67c3e4506a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926960"
---
# <a name="condition-table"></a>Bedingungstabelle

Die Tabelle Bedingung kann verwendet werden, um den Auswahlzustand eines beliebigen Eintrags in der [Feature-Tabelle](feature-table.md) basierend auf einem bedingten Ausdruck zu ändern.

Die Tabelle Bedingung enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Komponente\_ | [Identifier](identifier.md) | J   | N        |
| Ebene     | [Integer](integer.md)       | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Externer Schlüssel in Spalte 1 der Feature-Tabelle.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Ebene
</dt> <dd>

Eine bedingte Installationsebene für das Feature in der Spalte Feature \_ dieser Tabelle. Das Installationsprogramm legt die Installationsebene dieses Features auf die in dieser Spalte angegebene Ebene fest, wenn der Ausdruck in der Spalte Bedingung zu TRUE ausgewertet wird.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Wenn dieser bedingte Ausdruck zu TRUE ausgewertet wird, wird die Spalte Level in der Tabelle Feature auf die bedingte Installationsebene festgelegt.

Der Ausdruck in der Spalte Bedingung darf keinen Verweis auf den installierten Zustand eines Features oder einer Komponente enthalten. Dies liegt daran, dass die Ausdrücke in der Spalte Bedingung ausgewertet werden, bevor das Installationsprogramm die installierten Zustände von Features und Komponenten auswertet. Jeder Ausdruck in der Bedingungstabelle, der versucht, den installierten Zustand eines Features oder einer Komponente zu überprüfen, wird immer als FALSE ausgewertet.

Informationen zur Syntax von bedingten Anweisungen finden Sie unter [Conditional Statement Syntax](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Feature kann dauerhaft deaktiviert werden, indem die Spalte Ebene auf 0 festgelegt wird.

Die Ebene kann basierend auf einer beliebigen bedingungsbasierten Anweisung festgelegt werden, z. B. einem Test für die Plattform, dem Betriebssystem oder einer bestimmten Eigenschafteneinstellung.

Bedingungen sollten sorgfältig ausgewählt werden, damit ein Feature bei der Installation nicht aktiviert und dann bei der Deinstallation deaktiviert wird. Dadurch wird das Feature verwaist, und das Produkt kann nicht deinstalliert werden.

Auf diese Tabelle wird verwiesen, wenn die [Aktion CostFinalize](costfinalize-action.md) ausgeführt wird.

Wenn die [**Preselected-Eigenschaft**](preselected.md) auf 1 festgelegt wurde, wertet das Installationsprogramm die Tabelle Bedingung nicht aus. Die Tabelle Bedingung wirkt sich nur auf die Installation von Features aus, wenn keine der folgenden Eigenschaften festgelegt wurde:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**Entfernen**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**Installieren**](reinstall.md)  
[**Werben**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



