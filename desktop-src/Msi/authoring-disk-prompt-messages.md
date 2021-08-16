---
description: Verwenden Sie die folgenden Richtlinien, um eine installation Windows Installer zu erstellen, die ein Meldungsfeld anzeigt, in dem der Benutzer aufgefordert wird, einen Datenträger einzufügen.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Erstellen von Datenträgereingabeaufforderungsmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a27b324600b7098c4b11dd94528ce0f3aa624e6859df8d02ef43ee90d632068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381375"
---
# <a name="authoring-disk-prompt-messages"></a>Erstellen von Datenträgereingabeaufforderungsmeldungen

Verwenden Sie die folgenden Richtlinien, um eine installation Windows Installer zu erstellen, die ein Meldungsfeld anzeigt, in dem der Benutzer aufgefordert wird, einen Datenträger einzufügen.

**So zeigen Sie ein Meldungsfeld an, in dem der Benutzer aufgefordert wird, einen Datenträger einzufügen**

1.  Verwenden Sie die Erstellungsfunktionen des Installationsprogramms, um die [**DiskPrompt-Eigenschaftenzeichenfolge**](diskprompt.md) in der [Property-Tabelle](property-table.md) festzulegen. Dies sollte den Namen des zu installierenden Produkts und einen Platzhalterparameter in der Zeichenfolge für den titel enthalten, der auf dem Datenträger ausgegeben wird. Für Microsoft Publisher könnte die **DiskPrompt-Eigenschaft** beispielsweise "Microsoft Publisher: Datenträger \[ \] 1" sein, wobei \[ 1 \] der Platzhalter für den Datenträgertitel ist.
2.  Geben Sie die Titel der einzelnen Datenträger, für die eine Eingabeaufforderung angezeigt wird, in separate Zeilen der DiskPrompt-Spalte der [Tabelle Media](media-table.md) ein. Beispielsweise könnte der erste und einzige Eintrag in der Media-Tabelle "1–Install" sein.
3.  Während der [InstallFiles-Aktion](installfiles-action.md) wird der Wert aus der DiskPrompt-Spalte der [Media-Tabelle](media-table.md) durch den Platzhalter in der Zeichenfolge der [**DiskPrompt-Eigenschaft**](diskprompt.md) ersetzt.
4.  Die im Meldungsfeld angezeigte Meldung wird aus einer integrierten Vorlagenzeichenfolge in der [Fehlertabelle](error-table.md)erstellt. Dies ist Fehler 1302, und die Vorlagenzeichenfolge lautet: "Please insert the disk: \[ 2 \] ", and the \[ 2 \] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.

Im Beispiel wird dem Benutzer die folgende Meldung angezeigt: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."

Beachten Sie, dass Datenträgereingabeaufforderungsmeldungen von allen [Benutzeroberfläche Ebenen](user-interface-levels.md) mit Ausnahme von "None" angezeigt werden.

 

 



