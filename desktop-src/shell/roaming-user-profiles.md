---
description: Wenn auf einem Computer Windows 2000 Server oder höher in einem Netzwerk ausgeführt wird, können Benutzer ihre Profile auf dem Server speichern. Diese Profile werden als Roamingbenutzerprofile bezeichnet.
title: Roamingbenutzerprofile
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979937"
---
# <a name="roaming-user-profiles"></a>Roamingbenutzerprofile

Wenn auf einem Computer Windows 2000 Server oder höher in einem Netzwerk ausgeführt wird, können Benutzer ihre Profile auf dem Server speichern. Diese Profile werden als *Roamingbenutzerprofile* bezeichnet.

Roamingbenutzerprofile haben die folgenden Vorteile:

-   Automatische Ressourcen Verfügbarkeit. Das eindeutige Profil eines Benutzers ist automatisch verfügbar, wenn er sich auf einem beliebigen Computer im Netzwerk anmeldet. Benutzer müssen nicht auf jedem Computer, den Sie in einem Netzwerk verwenden, ein Profil erstellen.
-   Vereinfachtes ersetzen und Sichern von Computern. Wenn der Computer eines Benutzers ersetzt werden muss, kann er leicht ersetzt werden, da alle Profilinformationen des Benutzers unabhängig von einem einzelnen Computer separat im Netzwerk verwaltet werden. Wenn sich der Benutzer zum ersten Mal beim neuen Computer anmeldet, wird die Server Kopie des Profils des Benutzers auf den neuen Computer kopiert.

Das Profil des Benutzers wird nicht automatisch geladen, wenn der Benutzer mit der [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) -Funktion angemeldet ist. Verwenden Sie die [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) -Funktion, um ein Roamingbenutzerprofil Programm gesteuert zu laden. Um ein von **LoadUserProfile** geladenes Roamingbenutzerprofil zu entladen, nennen Sie die [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) -Funktion.

 

 
