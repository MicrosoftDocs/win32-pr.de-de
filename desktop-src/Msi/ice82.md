---
description: ICE82 überprüft, ob die RegisterProduct Action, RegisterUser Action, PublishProduct Action und PublishFeatures Action alle in der InstallExecuteSequence-Tabelle vorhanden sind. Das Paket wird überprüft, wenn alle Aktionen vorhanden sind.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf620bd58ca59315796941c6e8d9d3e4c12cdca9064d2be79058c89201a91bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105230"
---
# <a name="ice82"></a>ICE82

ICE82 überprüft, ob die [Aktion RegisterProduct,](registerproduct-action.md) [RegisterUser Action,](registeruser-action.md) [PublishProduct Action](publishproduct-action.md)und [PublishFeatures](publishfeatures-action.md) in der [InstallExecuteSequence-Tabelle vorhanden sind.](installexecutesequence-table.md) Das Paket wird überprüft, wenn alle Aktionen vorhanden sind.

ICE82 gibt eine Warnung aus, wenn zwei Aktionen mit der gleichen Sequenznummer in den Tabellen InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence oder AdvtExecuteSequence aufgeführt sind.

## <a name="result"></a>Ergebnis

ICE82 gibt die folgenden Warnungen aus.



| ICE82-Warnung                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Tabelle InstallExecuteSequence enthält nicht die unten genannten Aktionen: Aktionen fehlen:<br/> Veröffentlichen von Features<br/> Produkt veröffentlichen<br/> Registrieren des Produkts<br/> Registrieren eines Benutzers<br/> | Die benutzerdefinierte ICE82-Aktion gibt eine Warnung aus, wenn alle vier Aktionen nicht vorhanden sind.                                                                                                                                         |
| Diese Aktion \[ 1 \] enthält die doppelte \[ Sequenznummer 2 \] in Tabelle \[ \] 3.                                                                                                                                                     | ICE82 gibt eine Warnung aus, wenn zwei Aktionen mit der gleichen Sequenznummer in den Tabellen InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence oder AdvtExecuteSequence aufgeführt sind. |



 

ICE82 gibt die folgenden Fehler aus.



| ICE82-Fehler                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence sollte entweder alle unten genannten Aktionen oder keine der aktionen vorhanden enthalten.<br/> <List of actions present> <br/> Fehlende Aktionen:<br/> <List of actions missing> <br/> | ICE82 gibt einen Fehler aus, wenn einige der vier Aktionen vorhanden sind und andere nicht vorhanden sind. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




