---
description: Wenn möglich, ist die beste Möglichkeit, den Zielspeicherort für ein Verzeichnis anzugeben, das Erstellen der Verzeichnistabelle in Ihrem Installationspaket, um den richtigen Speicherort anzugeben. Weitere Informationen finden Sie unter Verwenden der Verzeichnistabelle.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Ändern des Zielspeicherorts für ein Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27adf952faeb4d37d5edb08a04bf25cc640d41e5d87732b30c80d25bba729705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145683"
---
# <a name="changing-the-target-location-for-a-directory"></a>Ändern des Zielspeicherorts für ein Verzeichnis

Wenn möglich, ist die beste Möglichkeit, den Zielspeicherort für ein Verzeichnis anzugeben, das Erstellen der [Verzeichnistabelle](directory-table.md) in Ihrem Installationspaket, um den richtigen Speicherort anzugeben. Weitere Informationen finden Sie unter [Verwenden der Verzeichnistabelle](using-the-directory-table.md).

Wenn Sie den Verzeichnisspeicherort zum Zeitpunkt der Installation ändern müssen, haben Sie die folgenden Optionen:

-   Geben Sie den Speicherort eines Verzeichnisses an, indem Sie den Wert einer [öffentlichen Eigenschaft](public-properties.md) in der Befehlszeile festlegen. Während der [CostFinalize-Aktion](costfinalize-action.md)werden die internen Verzeichnispfade, die vom Installationsprogramm verwendet werden, auf den Wert der Eigenschaften aktualisiert, die als Schlüssel in der [Verzeichnistabelle aufgeführt sind.](directory-table.md) Weitere Informationen finden Sie unter [Verwenden von Eigenschaften und](using-properties.md) Festlegen öffentlicher [Eigenschaftswerte in der Befehlszeile.](setting-public-property-values-on-the-command-line.md)
-   Geben Sie den Speicherort eines Verzeichnisses mithilfe einer benutzerdefinierten Aktion an. Wenn die benutzerdefinierte Aktion vor der [Aktion CostFinalize](costfinalize-action.md)ausgeführt werden soll, können Sie mit dem benutzerdefinierten Aktionstyp [51](custom-action-type-51.md) den Wert einer Eigenschaft aus einer formatierten Textzeichenfolge festlegen. Wenn die benutzerdefinierte Aktion nach der [Aktion CostFinalize](costfinalize-action.md)ausgeführt wird, können Sie den Wert des Verzeichnispfads mithilfe des benutzerdefinierten Aktionstyps [35](custom-action-type-35.md) aus einer formatierten Textzeichenfolge festlegen. Benutzerdefinierte Aktionen, die eine der [](b-gly.md) Eigenschaften des [Systemordners](property-reference.md) ändern, sollten sowohl in den Ausführungssequenztabellen ([InstallExecuteSequence Table](installexecutesequence-table.md) oder [AdminExecuteSequence Table](adminexecutesequence-table.md)) als auch [](f-gly.md) in den Sequenztabellen der Benutzeroberfläche ([InstallUISequence Table](installuisequence-table.md) und [AdminUISequence Table](adminuisequence-table.md)) enthalten sein, damit der Ordner sowohl während der vollständigen Installation der Benutzeroberfläche als auch bei grundlegenden Ui-Installationen geändert wird.
-   Wenn bei der Installation eine [*vollständige*](f-gly.md)Benutzeroberfläche ausgeführt wird, können Sie [**msiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) oder [SetTargetPath ControlEvent](settargetpath-controlevent.md) verwenden, um den Verzeichnispfad zu festlegen. Überprüfen Sie [**die ProductState-Eigenschaft,**](productstate.md) um zu ermitteln, ob das Produkt, das diese Komponente enthält, bereits installiert ist, bevor **Sie MsiSetTargetPath** oder SetTargetPath ControlEvent aufrufen. Versuchen Sie nicht, den Zielverzeichnispfad zu ändern, wenn einige Komponenten, die diesen Pfad verwenden, bereits für den aktuellen Benutzer oder einen anderen Benutzer installiert sind.

Die folgenden Einschränkungen gelten für alle oben genannten Optionen:

-   Versuchen Sie nicht, den Zielverzeichnispfad zu ändern, wenn einige Komponenten, die den Pfad verwenden, bereits für den aktuellen Benutzer oder für einen anderen Benutzer installiert sind.
-   Versuchen Sie nicht, den Zielverzeichnispfad während einer [Wartungsinstallation zu ändern.](maintenance-installation.md)

 

 



