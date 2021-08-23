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
ms.openlocfilehash: 4b064eefae4916576cb8ccc6b3dfe058ea4e2e34f960315b74d384194f61ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967830"
---
# <a name="user-profiles-reference"></a>Referenz zu Benutzerprofilen

Die folgenden API-Elemente werden mit Benutzerprofilen verwendet.

## <a name="functions"></a>Functions



| Funktion                                                                   | BESCHREIBUNG                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Ruft die Umgebungsvariablen für den angegebenen Benutzer ab.                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Erstellt ein neues Benutzerprofil. (Windows Vista und höher.)                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Löscht das Benutzerprofil und alle benutzerbezogenen Einstellungen vom angegebenen Computer.                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Gibt von der [**CreateEnvironmentBlock-Funktion erstellte Umgebungsvariablen**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) frei. |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Erweitert die Quellzeichenfolge mithilfe des Umgebungsblocks, der für den angegebenen Benutzer eingerichtet wurde.                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Ruft den Pfad zum Stamm des Profils Alle Benutzer ab.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Ruft den Pfad zum Stamm des Standardbenutzerprofils ab.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Ruft den Pfad zum Stammverzeichnis ab, in dem alle Benutzerprofile gespeichert sind.                                  |
| [**GetProfileType**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Ruft den Typ des profils ab, das für den aktuellen Benutzer geladen wurde.                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Ruft den Pfad zum Stammverzeichnis des Profils des angegebenen Benutzers ab.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Lädt das Profil des angegebenen Benutzers.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Entlädt das Profil eines Benutzers, das von der [**LoadUserProfile-Funktion geladen**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) wurde.          |



 

Die [**CreateUserProfileEx-Funktion**](createuserprofileex.md) wird nicht unterstützt.

## <a name="structures"></a>Strukturen



| Struktur                          | BESCHREIBUNG                                |
|------------------------------------|--------------------------------------------|
| [**Profileinfo**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Enthält Informationen zu einem Benutzerprofil. |



 

 

 



