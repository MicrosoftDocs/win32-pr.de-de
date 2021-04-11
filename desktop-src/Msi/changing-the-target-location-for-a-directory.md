---
description: Wenn möglich, ist die beste Möglichkeit zum Angeben des Zielspeicher Orts für ein Verzeichnis das Erstellen der Verzeichnis Tabelle in Ihrem Installationspaket, um den richtigen Speicherort bereitzustellen. Weitere Informationen finden Sie unter Verwenden der Verzeichnis Tabelle.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Ändern des Zielspeicher Orts für ein Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818c4e9d555244dd1637e19eb249478f13ea2d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215705"
---
# <a name="changing-the-target-location-for-a-directory"></a>Ändern des Zielspeicher Orts für ein Verzeichnis

Wenn möglich, ist die beste Möglichkeit zum Angeben des Zielspeicher Orts für ein Verzeichnis das Erstellen der [Verzeichnis Tabelle](directory-table.md) in Ihrem Installationspaket, um den richtigen Speicherort bereitzustellen. Weitere Informationen finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).

Wenn Sie den Speicherort des Verzeichnisses zum Zeitpunkt der Installation ändern müssen, haben Sie folgende Möglichkeiten:

-   Geben Sie den Speicherort eines Verzeichnisses an, indem Sie den Wert einer [öffentlichen Eigenschaft](public-properties.md) in der Befehlszeile festlegen. Während der [costfinalize-Aktion](costfinalize-action.md)werden die vom Installationsprogramm verwendeten internen Verzeichnispfade auf den Wert der Eigenschaften aktualisiert, die in der [Verzeichnis Tabelle](directory-table.md)als Schlüssel aufgeführt sind. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften](using-properties.md) und [Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile](setting-public-property-values-on-the-command-line.md).
-   Geben Sie den Speicherort eines Verzeichnisses mithilfe einer benutzerdefinierten Aktion an. Wenn die benutzerdefinierte Aktion vor der [costfinalize-Aktion](costfinalize-action.md)ausgeführt werden soll, können Sie einen [benutzerdefinierten Aktionstyp 51](custom-action-type-51.md) verwenden, um den Wert einer Eigenschaft aus einer formatierten Text Zeichenfolge festzulegen. Wenn die benutzerdefinierte Aktion nach der [costfinalize-Aktion](costfinalize-action.md)ausgeführt wird, können Sie einen [benutzerdefinierten Aktionstyp 35](custom-action-type-35.md) verwenden, um den Wert des Verzeichnis Pfads aus einer formatierten Text Zeichenfolge festzulegen. Benutzerdefinierte Aktionen, die eine der [System Ordnereigenschaften](property-reference.md) ändern, sollten sowohl in den Ausführungssequenz Tabellen ([InstallExecuteSequence-Tabelle](installexecutesequence-table.md) [*als auch*](f-gly.md) in der [AdminExecuteSequence](adminexecutesequence-table.md)-Tabelle) und in den Sequenz Tabellen der Benutzeroberfläche ("[InstallUISequence](installuisequence-table.md) [*" und "*](b-gly.md) [AdminUISequence](adminuisequence-table.md)") enthalten sein
-   Wenn bei der Installation eine [*vollständige Benutzeroberfläche*](f-gly.md)ausgeführt wird, können Sie den Verzeichnispfad mithilfe von " [**msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) " oder " [settargetpath ControlEvent](settargetpath-controlevent.md) " festlegen. Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) , um zu bestimmen, ob das Produkt, das diese Komponente enthält, bereits installiert ist, bevor Sie **msisettargetpath** oder settargetpath ControlEvent aufrufen. Versuchen Sie nicht, den Zielverzeichnis Pfad zu ändern, wenn einige Komponenten, die diesen Pfad verwenden, für den aktuellen Benutzer oder einen anderen Benutzer bereits installiert sind.

Für alle oben genannten Optionen gelten die folgenden Einschränkungen:

-   Versuchen Sie nicht, den Zielverzeichnis Pfad zu ändern, wenn einige Komponenten, die den Pfad verwenden, für den aktuellen Benutzer oder für einen anderen Benutzer bereits installiert sind.
-   Versuchen Sie nicht, den Zielverzeichnis Pfad während einer [Wartungs Installation](maintenance-installation.md)zu ändern.

 

 



