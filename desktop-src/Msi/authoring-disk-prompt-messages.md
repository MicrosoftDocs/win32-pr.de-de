---
description: Verwenden Sie die folgenden Richtlinien, um eine Windows Installer Installation zu erstellen, die ein Meldungs Feld anzeigt, in dem der Benutzer zum Einfügen eines Datenträgers
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Erstellen von Datenträger Aufforderungs Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349169"
---
# <a name="authoring-disk-prompt-messages"></a>Erstellen von Datenträger Aufforderungs Meldungen

Verwenden Sie die folgenden Richtlinien, um eine Windows Installer Installation zu erstellen, die ein Meldungs Feld anzeigt, in dem der Benutzer zum Einfügen eines Datenträgers

**So zeigen Sie ein Meldungs Feld an, das den Benutzer auffordert, einen Datenträger einzufügen**

1.  Verwenden Sie die Erstellungs Funktionen des Installers, um die Zeichenfolge der [**diskprompt**](diskprompt.md) -Eigenschaft in der [Eigenschaften](property-table.md) Tabelle festzulegen. Dies sollte den Namen des installierten Produkts und einen Platzhalter Parameter innerhalb der Zeichenfolge für den auf dem Datenträger gedruckten Titel einschließen. Für Microsoft Publisher könnte die **diskprompt** -Eigenschaft z. b. "Microsoft Publisher: Disk \[ 1 \] " lauten, wobei " \[ 1" \] der Platzhalter für den Datenträger Titel ist.
2.  Geben Sie die Titel der einzelnen Datenträger ein, für die in separate Zeilen der Spalte "diskprompt" der [Medien](media-table.md) Tabelle aufgefordert werden. Der erste und einzige Eintrag in der Medien Tabelle könnte z. b. "1 – install" lauten.
3.  Während der [InstallFiles](installfiles-action.md) -Aktion wird der Wert aus der diskprompt-Spalte der [Medien](media-table.md) Tabelle durch den Platzhalter in der Zeichenfolge der [**diskprompt**](diskprompt.md) -Eigenschaft ersetzt.
4.  Die Meldung, die im Meldungs Feld angezeigt wird, wird aus einer integrierten Vorlagen Zeichenfolge in der [Fehler Tabelle](error-table.md)erstellt. Dies ist der Fehler 1302, und die Vorlagen Zeichenfolge lautet: "Bitte legen Sie den Datenträger \[ ein: 2 \] " und \[ 2 \] steht für einen Platzhalter für die [**diskprompt**](diskprompt.md) -Eigenschaft.

Im Beispiel wird dem Benutzer die folgende Meldung angezeigt: "legen Sie den Datenträger ein: Microsoft Publisher: Disk 1 – install".

Beachten Sie, dass Datenträger-prompt-Meldungen von allen [Benutzeroberflächen Ebenen](user-interface-levels.md) angezeigt werden, ausgenommen keine.

 

 



