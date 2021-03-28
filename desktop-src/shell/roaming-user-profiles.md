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
# <a name="roaming-user-profiles"></a><span data-ttu-id="dab76-104">Roamingbenutzerprofile</span><span class="sxs-lookup"><span data-stu-id="dab76-104">Roaming User Profiles</span></span>

<span data-ttu-id="dab76-105">Wenn auf einem Computer Windows 2000 Server oder höher in einem Netzwerk ausgeführt wird, können Benutzer ihre Profile auf dem Server speichern.</span><span class="sxs-lookup"><span data-stu-id="dab76-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="dab76-106">Diese Profile werden als *Roamingbenutzerprofile* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dab76-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="dab76-107">Roamingbenutzerprofile haben die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="dab76-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="dab76-108">Automatische Ressourcen Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="dab76-108">Automatic resource availability.</span></span> <span data-ttu-id="dab76-109">Das eindeutige Profil eines Benutzers ist automatisch verfügbar, wenn er sich auf einem beliebigen Computer im Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="dab76-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="dab76-110">Benutzer müssen nicht auf jedem Computer, den Sie in einem Netzwerk verwenden, ein Profil erstellen.</span><span class="sxs-lookup"><span data-stu-id="dab76-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="dab76-111">Vereinfachtes ersetzen und Sichern von Computern.</span><span class="sxs-lookup"><span data-stu-id="dab76-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="dab76-112">Wenn der Computer eines Benutzers ersetzt werden muss, kann er leicht ersetzt werden, da alle Profilinformationen des Benutzers unabhängig von einem einzelnen Computer separat im Netzwerk verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="dab76-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="dab76-113">Wenn sich der Benutzer zum ersten Mal beim neuen Computer anmeldet, wird die Server Kopie des Profils des Benutzers auf den neuen Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="dab76-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="dab76-114">Das Profil des Benutzers wird nicht automatisch geladen, wenn der Benutzer mit der [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) -Funktion angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="dab76-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="dab76-115">Verwenden Sie die [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) -Funktion, um ein Roamingbenutzerprofil Programm gesteuert zu laden.</span><span class="sxs-lookup"><span data-stu-id="dab76-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="dab76-116">Um ein von **LoadUserProfile** geladenes Roamingbenutzerprofil zu entladen, nennen Sie die [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dab76-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
