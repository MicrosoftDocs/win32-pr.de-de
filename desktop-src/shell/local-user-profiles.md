---
description: Das System erstellt automatisch ein lokales Benutzerprofil für jeden Benutzer, wenn sich der Benutzer zum ersten Mal beim Computer anmeldet. Das System verwaltet automatisch die Einstellungen für die Arbeitsumgebung der einzelnen Benutzer in einem Benutzerprofil auf dem lokalen Computer.
title: Lokale Benutzerprofile
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980016"
---
# <a name="local-user-profiles"></a>Lokale Benutzerprofile

Für die Windows-Sicherheit ist ein Benutzerprofil für jedes Benutzerkonto auf einem Computer erforderlich. Das System erstellt automatisch ein *Lokales Benutzerprofil* für jeden Benutzer, wenn sich der Benutzer zum ersten Mal beim Computer anmeldet. Das System verwaltet automatisch die Einstellungen für die Arbeitsumgebung der einzelnen Benutzer in einem Benutzerprofil auf dem lokalen Computer.

Windows Vista und höher: Benutzerprofile werden über das System Steuerungselement **Benutzerkonten** verwaltet.

Windows 2000 und Windows XP: um ein Benutzerprofil zu kopieren oder zu löschen, wählen Sie in der Systemsteuerung die Option **System** , dann die Registerkarte **erweitert** und dann im Bereich **Benutzerprofil** die Schaltfläche **Einstellungen** .

Das Profil des Benutzers wird nicht automatisch geladen, wenn der Benutzer mit der [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) -Funktion angemeldet ist. Wenn Sie ein Benutzerprofil Programm gesteuert laden möchten, verwenden Sie die [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) -Funktion. Um ein von **LoadUserProfile** geladenes Benutzerprofil zu entladen, nennen Sie die [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) -Funktion.

 

 
