---
description: ICE82 überprüft, ob die Aktion registerproduct Action, RegisterUser Action, publishproduct Action und publishfeatures in der Tabelle InstallExecuteSequence vorhanden sind. Das Paket wird überprüft, wenn alle Aktionen vorhanden sind.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758413"
---
# <a name="ice82"></a>ICE82

ICE82 überprüft, ob die [Aktion registerproduct](registerproduct-action.md)Action, [RegisterUser Action](registeruser-action.md), [publishproduct Action](publishproduct-action.md)und [publishfeatures](publishfeatures-action.md) in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)vorhanden sind. Das Paket wird überprüft, wenn alle Aktionen vorhanden sind.

ICE82 gibt eine Warnung aus, wenn zwei Aktionen mit der gleichen Sequenznummer in den Tabellen InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence oder AdvtExecuteSequence aufgeführt sind.

## <a name="result"></a>Ergebnis

ICE82 gibt die folgenden Warnungen aus.



| ICE82-Warnung                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die InstallExecuteSequence-Tabelle enthält nicht die unten erwähnten Aktionen: Aktionen fehlen:<br/> Features veröffentlichen<br/> Produkt veröffentlichen<br/> Produkt registrieren<br/> Benutzer registrieren<br/> | ICE82 Custom Action gibt eine Warnung aus, wenn alle vier Aktionen fehlen.                                                                                                                                         |
| Diese Aktion \[ 1 \] weist die doppelte Sequenznummer \[ 2 \] in der Tabelle \[ 3 auf \] .                                                                                                                                                     | ICE82 gibt eine Warnung aus, wenn zwei Aktionen mit der gleichen Sequenznummer in den Tabellen InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence oder AdvtExecuteSequence aufgeführt sind. |



 

ICE82 gibt die folgenden Fehler aus.



| ICE82-Fehler                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence muss entweder alle unten erwähnten Aktionen enthalten, oder es sind keine Aktionen vorhanden.<br/> <List of actions present> <br/> Fehlende Aktionen:<br/> <List of actions missing> <br/> | ICE82 gibt einen Fehler aus, wenn einige der vier Aktionen vorhanden sind und andere nicht vorhanden sind. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




