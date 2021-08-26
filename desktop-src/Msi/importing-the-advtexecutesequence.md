---
description: Die Tabelle AdvtExecuteSequence listet Aktionen auf, die das Installationsprogramm aufruft, wenn die AKTION "ADVERTISE" der obersten Ebene ausgeführt wird. Weitere Informationen finden Sie unter Tabellengruppe für Installationsprozedur, Verwenden einer Sequenztabelle und ausführliches Beispiel für die Sequenztabelle.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importieren der AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518adfa315b5705806ba65caf09691316894ab664c32485dd3f4b6ce894be1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043670"
---
# <a name="importing-the-advtexecutesequence"></a>Importieren der AdvtExecuteSequence

Die [Tabelle AdvtExecuteSequence listet](advtexecutesequence-table.md) Aktionen auf, die das Installationsprogramm aufruft, wenn die [ADVERTISE-Aktion](advertise-action.md)der obersten Ebene ausgeführt wird. Weitere Informationen finden Sie unter [Installationsprozedurtabellengruppe](installation-procedure-tables-group.md), [Verwenden einer Sequenztabelle](using-a-sequence-table.md)und ausführliches Beispiel für [die Sequenztabelle.](sequence-table-detailed-example.md)

Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) uisample.msi aus dem Windows Installer SDK verwendet haben, enthalten die Sequenztabellen in Ihrer Kopie von MNP2000.msi bereits die unter Verwenden einer [Sequenztabelle](using-a-sequence-table.md)beschriebenen vorgeschlagenen Aktionssequenzen. Es sollten keine Änderungen an diesen Sequenzen erforderlich sein, um das Editor Beispielinstallationspaket zu erstellen.

Verwenden Sie den Datenbank-Editor, um MNP2000.msi zu öffnen und die folgenden Daten in die [Tabelle AdvtExecuteSequence](advtexecutesequence-table.md)einzugeben.

[Tabelle "AdvtExecuteSequence"](advtexecutesequence-table.md)



| Aktion                | Bedingung | Sequenz |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1000     |
| CostInitialize        |           | 800      |
| CreateShortcuts       |           | 4500     |
| InstallFinalize       |           | 6600     |
| InstallInitialize     |           | 1500     |
| InstallValidate       |           | 1400     |
| PublishComponents     |           | 6200     |
| PublishFeatures       |           | 6300     |
| PublishProduct        |           | 6400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| RegisterMIMEInfo      |           | 4900     |
| RegisterProgIdInfo    |           | 4800     |



 

Die [Tabelle AdvtUISequence](advtuisequence-table.md) wird vom Installationsprogramm nicht verwendet. Diese Tabelle darf nicht vorhanden sein oder in der Installationsdatenbank leer gelassen werden.

[Fortsetzen](adding-summary-information.md)

 

 



