---
description: Die folgenden API-Elemente werden mit Benutzerprofilen verwendet.
title: Referenz zu Benutzerprofilen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980712"
---
# <a name="user-profiles-reference"></a>Referenz zu Benutzerprofilen

Die folgenden API-Elemente werden mit Benutzerprofilen verwendet.

## <a name="functions"></a>Functions



| Funktion                                                                   | BESCHREIBUNG                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**"Kreateumgebblock"**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Ruft die Umgebungsvariablen für den angegebenen Benutzer ab.                                                   |
| [**"Kreateprofile"**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Erstellt ein neues Benutzerprofil. (Nur Windows Vista und höher.)                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Löscht das Benutzerprofil und alle Benutzer bezogenen Einstellungen vom angegebenen Computer.                           |
| [**Destroyumgebblock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Gibt Umgebungsvariablen frei, die von der Funktion " [**kreateenvironment Block**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) " erstellt wurden. |
| [**Expandumgebstringsforuser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Erweitert die Quell Zeichenfolge mit dem Umgebungsblock, der für den angegebenen Benutzer eingerichtet wurde.                  |
| [**Getallusersprofiledirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Ruft den Pfad zum Stamm des Profils alle Benutzer ab.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Ruft den Pfad zum Stamm des Standardbenutzer Profils ab.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Ruft den Pfad zum Stammverzeichnis ab, in dem alle Benutzerprofile gespeichert werden.                                  |
| [**Getprofiletype**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Ruft den Typ des Profils ab, das für den aktuellen Benutzer geladen wurde.                                                    |
| [**Getuserprofiledirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Ruft den Pfad zum Stammverzeichnis des angegebenen Benutzerprofils ab.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Lädt das Profil des angegebenen Benutzers.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Entlädt das Profil eines Benutzers, das von der [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) -Funktion geladen wurde.          |



 

Die Funktion " [**samateuserprofileex**](createuserprofileex.md) " wird nicht unterstützt.

## <a name="structures"></a>Strukturen



| Struktur                          | BESCHREIBUNG                                |
|------------------------------------|--------------------------------------------|
| [**Profilinfo**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Enthält Informationen zu einem Benutzerprofil. |



 

 

 



