---
description: Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Benutzer Umgebungsvariablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4f898c7a9135c0421fdd67a7bed1d97655556f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994782"
---
# <a name="user-environment-variables"></a>Benutzer Umgebungsvariablen

Umgebungsvariablen geben Suchpfade für Dateien, Verzeichnisse für temporäre Dateien, anwendungsspezifische Optionen und andere ähnliche Informationen an. Das System verwaltet einen Umgebungsblock für jeden Benutzer und einen für den Computer. Der System Umgebungsblock stellt Umgebungsvariablen für alle Benutzer des jeweiligen Computers dar. Der Umgebungsblock eines Benutzers stellt die Umgebungsvariablen dar, die das System für diesen bestimmten Benutzer verwaltet, einschließlich der Gruppe von System Umgebungsvariablen.

Standardmäßig erhält jeder Prozess eine Kopie des Umgebungs Blocks für seinen übergeordneten Prozess. In der Regel handelt es sich hierbei um den Umgebungsblock für den angemeldeten Benutzer. Von einem Prozess können unterschiedliche Umgebungs Blöcke für die untergeordneten Prozesse mithilfe der Funktion "- [**Prozess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " oder " [**kreateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " angegeben werden.

Um Umgebungsvariablen hinzuzufügen oder zu ändern, wählt der Benutzer in der System **Steuerung** **System** aus und wählt dann die Registerkarte **Umgebung** aus. Der Benutzer kann mithilfe des **Set** -Befehls auch Umgebungsvariablen an der Eingabeaufforderung hinzufügen oder ändern. Umgebungsvariablen, die mit dem **Set** -Befehl erstellt werden, gelten nur für das Befehlsfenster, in dem Sie festgelegt sind, und für die untergeordneten Prozesse. Weitere Informationen erhalten Sie, wenn Sie **Set/?** eingeben. an einer Eingabeaufforderung.

Verwenden Sie die Funktion " [**kreateenvironment Block**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) ", um eine Kopie des Umgebungs Blocks für einen bestimmten Benutzer abzurufen. Verwenden Sie die [**destroyenvironment Block**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) -Funktion, um einen von " **kreateenvironment Block**" erstellten Umgebungsblock freizugeben. Diese Funktionen verweisen auf einen Zeiger auf einen Umgebungsblock. Der Umgebungsblock ist ein Array von Unicode-Zeichen folgen, die auf Null enden. Die Liste endet mit zwei Nullen ( \\ 0 \\ 0).

Um eine Zeichenfolge zu erweitern, die Umgebungsvariablen enthält, indem Sie den Umgebungsblock für einen angegebenen Benutzer verwenden, verwenden Sie die [**expandumgebstringsforuser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) -Funktion.

 

 
