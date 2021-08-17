---
description: Bevor Sie mit einer Datenbank arbeiten, müssen Sie zunächst ein Handle dafür abrufen.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Abrufen eines Datenbankhandpunkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a325c7c69bed4141de8f553a344b20b5f3c61bfe28a1594105c0a853b7075744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145563"
---
# <a name="obtaining-a-database-handle"></a>Abrufen eines Datenbankhandpunkts

Bevor Sie mit einer Datenbank arbeiten, müssen Sie zunächst ein Handle dafür abrufen.

**So greifen Sie auf Informationen zu einer Installationsdatenbank zu**

1.  Es gibt zwei Möglichkeiten, ein Handle für die Datenbank zu erhalten:
    -   Wenn eine Installation ausgeführt wird, rufen Sie ein Handle für die aktive Datenbank ab, indem Sie die [**MsiGetActiveDatabase-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) aufrufen.
    -   Wenn keine Installation ausgeführt wird, öffnen Sie eine angegebene Datenbank, indem Sie die [**MsiOpenDatabase-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) aufrufen.
2.  Nachdem die Datenbank geöffnet wurde, können Sie Funktionen aufrufen, um Informationen zur Datenbank zu erhalten oder die Datenbank zu bearbeiten.
    -   Erstellen Sie ein **View-Objekt,** und geben Sie SQL Abfrage der geöffneten Datenbank an, indem Sie die [**MsiDatabaseOpenView-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) aufrufen.
    -   Rufen Sie einen Datensatz ab, der alle Primärschlüssel einer angegebenen Tabelle in der geöffneten Datenbank enthält, indem Sie die [**MsiDatabaseGetPrimaryKeys-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) aufrufen.
    -   Überprüfen Sie den aktuellen Status einer geöffneten Datenbank, indem Sie die [**MsiGetDatabaseState-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) aufrufen. Mit der **MsiGetDatabaseState-Funktion** können Sie den Lese-/Schreibstatus für eine Datenbank oder ermitteln, ob das Handle gültig ist.

 

 



