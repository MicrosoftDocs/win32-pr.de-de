---
description: Bevor Sie mit einer Datenbank arbeiten, müssen Sie zunächst ein Handle dafür abrufen.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Abrufen eines Daten Bank Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130440"
---
# <a name="obtaining-a-database-handle"></a>Abrufen eines Daten Bank Handles

Bevor Sie mit einer Datenbank arbeiten, müssen Sie zunächst ein Handle dafür abrufen.

**So greifen Sie auf Informationen zu einer Installer-Datenbank zu**

1.  Abrufen eines Handles für die Datenbank auf eine von zwei Arten:
    -   Wenn eine Installation ausgeführt wird, rufen Sie ein Handle für die aktive Datenbank ab, indem Sie die [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) -Funktion aufrufen.
    -   Wenn eine Installation nicht ausgeführt wird, öffnen Sie eine beliebige Datenbank, indem Sie die [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) -Funktion aufrufen.
2.  Nachdem die Datenbank geöffnet wurde, können Sie Funktionen zum Abrufen von Informationen über die Datenbank oder zum Bearbeiten der Datenbank abrufen.
    -   Erstellen Sie ein **View** -Objekt, und geben Sie eine SQL-Abfrage der geöffneten Datenbank an, indem Sie die [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) -Funktion aufrufen.
    -   Rufen Sie einen Datensatz ab, der alle Primärschlüssel einer angegebenen Tabelle in der geöffneten Datenbank enthält, indem Sie die [**msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) -Funktion aufrufen.
    -   Überprüfen Sie den aktuellen Status einer geöffneten Datenbank, indem Sie die [**msigetdatabasestate**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) -Funktion aufrufen. Mit der **msigetdatabasestate** -Funktion können Sie den Lese-/Schreibstatus für eine Datenbank festlegen oder, wenn das Handle gültig ist.

 

 



