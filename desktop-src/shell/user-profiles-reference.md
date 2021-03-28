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
# <a name="user-profiles-reference"></a><span data-ttu-id="1a112-103">Referenz zu Benutzerprofilen</span><span class="sxs-lookup"><span data-stu-id="1a112-103">User Profiles Reference</span></span>

<span data-ttu-id="1a112-104">Die folgenden API-Elemente werden mit Benutzerprofilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a112-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="1a112-105">Functions</span><span class="sxs-lookup"><span data-stu-id="1a112-105">Functions</span></span>



| <span data-ttu-id="1a112-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="1a112-106">Function</span></span>                                                                   | <span data-ttu-id="1a112-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a112-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a112-108">**"Kreateumgebblock"**</span><span class="sxs-lookup"><span data-stu-id="1a112-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="1a112-109">Ruft die Umgebungsvariablen für den angegebenen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="1a112-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="1a112-110">**"Kreateprofile"**</span><span class="sxs-lookup"><span data-stu-id="1a112-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="1a112-111">Erstellt ein neues Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="1a112-111">Creates a new user profile.</span></span> <span data-ttu-id="1a112-112">(Nur Windows Vista und höher.)</span><span class="sxs-lookup"><span data-stu-id="1a112-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="1a112-113">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="1a112-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="1a112-114">Löscht das Benutzerprofil und alle Benutzer bezogenen Einstellungen vom angegebenen Computer.</span><span class="sxs-lookup"><span data-stu-id="1a112-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="1a112-115">**Destroyumgebblock**</span><span class="sxs-lookup"><span data-stu-id="1a112-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="1a112-116">Gibt Umgebungsvariablen frei, die von der Funktion " [**kreateenvironment Block**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) " erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1a112-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="1a112-117">**Expandumgebstringsforuser**</span><span class="sxs-lookup"><span data-stu-id="1a112-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="1a112-118">Erweitert die Quell Zeichenfolge mit dem Umgebungsblock, der für den angegebenen Benutzer eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="1a112-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="1a112-119">**Getallusersprofiledirectory**</span><span class="sxs-lookup"><span data-stu-id="1a112-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="1a112-120">Ruft den Pfad zum Stamm des Profils alle Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="1a112-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="1a112-121">**GetDefaultUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="1a112-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="1a112-122">Ruft den Pfad zum Stamm des Standardbenutzer Profils ab.</span><span class="sxs-lookup"><span data-stu-id="1a112-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="1a112-123">**GetProfilesDirectory**</span><span class="sxs-lookup"><span data-stu-id="1a112-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="1a112-124">Ruft den Pfad zum Stammverzeichnis ab, in dem alle Benutzerprofile gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1a112-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="1a112-125">**Getprofiletype**</span><span class="sxs-lookup"><span data-stu-id="1a112-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="1a112-126">Ruft den Typ des Profils ab, das für den aktuellen Benutzer geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1a112-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="1a112-127">**Getuserprofiledirectory**</span><span class="sxs-lookup"><span data-stu-id="1a112-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="1a112-128">Ruft den Pfad zum Stammverzeichnis des angegebenen Benutzerprofils ab.</span><span class="sxs-lookup"><span data-stu-id="1a112-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="1a112-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="1a112-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="1a112-130">Lädt das Profil des angegebenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1a112-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="1a112-131">**UnloadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="1a112-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="1a112-132">Entlädt das Profil eines Benutzers, das von der [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) -Funktion geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1a112-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="1a112-133">Die Funktion " [**samateuserprofileex**](createuserprofileex.md) " wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a112-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="1a112-134">Strukturen</span><span class="sxs-lookup"><span data-stu-id="1a112-134">Structures</span></span>



| <span data-ttu-id="1a112-135">Struktur</span><span class="sxs-lookup"><span data-stu-id="1a112-135">Structure</span></span>                          | <span data-ttu-id="1a112-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a112-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="1a112-137">**Profilinfo**</span><span class="sxs-lookup"><span data-stu-id="1a112-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="1a112-138">Enthält Informationen zu einem Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="1a112-138">Contains information about a user profile.</span></span> |



 

 

 



