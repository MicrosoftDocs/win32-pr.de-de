---
description: Das System erstellt automatisch ein lokales Benutzerprofil für jeden Benutzer, wenn sich der Benutzer zum ersten Mal am Computer anmeldet. Das System verwaltet automatisch die Einstellungen für die Arbeitsbereiche jedes Benutzers in einem Benutzerprofil auf dem lokalen Computer.
title: Lokale Benutzerprofile
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 713adc7db522ff473de42a3ecaa2a1a0671f95ee5f4039f0039a196304c7aa4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220155"
---
# <a name="local-user-profiles"></a>Lokale Benutzerprofile

Windows Sicherheit erfordert ein Benutzerprofil für jedes Benutzerkonto auf einem Computer. Das System erstellt automatisch ein *lokales Benutzerprofil* für jeden Benutzer, wenn sich der Benutzer zum ersten Mal am Computer anmeldet. Das System verwaltet automatisch die Einstellungen für die Arbeitsbereiche jedes Benutzers in einem Benutzerprofil auf dem lokalen Computer.

Windows Vista und höher: Benutzerprofile werden über das Systemsteuerungselement **Benutzerkonten** verwaltet.

Windows 2000 und Windows XP: Um ein Benutzerprofil zu kopieren oder zu löschen, wählen Sie auf der Systemsteuerung die Option **System** und dann im Bereich **Benutzerprofil** die Schaltfläche **Erweitert** und dann die Schaltfläche **Einstellungen** aus.

Das Profil des Benutzers wird nicht automatisch geladen, wenn der Benutzer mit der [**LogonUser-Funktion**](/windows/win32/api/winbase/nf-winbase-logonusera) angemeldet ist. Verwenden Sie die [**LoadUserProfile-Funktion,**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) um ein Benutzerprofil programmgesteuert zu laden. Um ein von **LoadUserProfile** geladenes Benutzerprofil zu entladen, rufen Sie die [**Funktion UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) auf.

 

 
