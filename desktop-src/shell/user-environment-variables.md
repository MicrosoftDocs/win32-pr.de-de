---
description: Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Benutzerumgebungsvariablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bbe37cdbe7dd82268b2166ed625a9baf1d2502df4c26208bca51a89cd782df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857042"
---
# <a name="user-environment-variables"></a>Benutzerumgebungsvariablen

Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an. Das System verwaltet einen Umgebungsblock für jeden Benutzer und einen für den Computer. Der Systemumgebungsblock stellt Umgebungsvariablen für alle Benutzer des jeweiligen Computers dar. Der Umgebungsblock eines Benutzers stellt die Umgebungsvariablen dar, die das System für diesen bestimmten Benutzer verwaltet, einschließlich der Systemumgebungsvariablen.

Standardmäßig erhält jeder Prozess eine Kopie des Umgebungsblocks für seinen übergeordneten Prozess. In der Regel ist dies der Umgebungsblock für den angemeldeten Benutzer. Ein Prozess kann mithilfe der [**CreateProcess-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) oder [**CreateProcessAsUser-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) verschiedene Umgebungsblöcke für seine untergeordneten Prozesse angeben.

Um Umgebungsvariablen hinzuzufügen oder zu ändern, wählt der Benutzer **system** aus der Systemsteuerung **und** dann die Registerkarte **Umgebung** aus. Der Benutzer kann umgebungsvariablen auch über eine Eingabeaufforderung mithilfe des Befehls **set hinzufügen oder** ändern. Umgebungsvariablen, die mit dem **Set-Befehl** erstellt werden, gelten nur für das Befehlsfenster, in dem sie festgelegt sind, und für die untergeordneten Prozesse. Geben Sie für weitere Informationen set **/? ein.** an einer Eingabeaufforderung.

Verwenden Sie die [**CreateEnvironmentBlock-Funktion,**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) um eine Kopie des Umgebungsblocks für einen bestimmten Benutzer abzurufen. Um einen von **CreateEnvironmentBlock erstellten Umgebungsblock** frei zu geben, verwenden Sie die [**DestroyEnvironmentBlock-Funktion.**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) Diese Funktionen verweisen auf einen Zeiger auf einen Umgebungsblock. Der Umgebungsblock ist ein Array von Unicode-Zeichenfolgen mit NULL-Terminierung. Die Liste endet mit zwei NULL-Werten ( \\ 0 \\ 0).

Verwenden Sie die [**ExpandEnvironmentStringsForUser-Funktion,**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) um eine Zeichenfolge zu erweitern, die Umgebungsvariablen enthält, indem Sie den Umgebungsblock für einen angegebenen Benutzer verwenden.

 

 
