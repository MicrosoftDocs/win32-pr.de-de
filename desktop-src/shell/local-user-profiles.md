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
# <a name="local-user-profiles"></a><span data-ttu-id="b287b-104">Lokale Benutzerprofile</span><span class="sxs-lookup"><span data-stu-id="b287b-104">Local User Profiles</span></span>

<span data-ttu-id="b287b-105">Für die Windows-Sicherheit ist ein Benutzerprofil für jedes Benutzerkonto auf einem Computer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b287b-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="b287b-106">Das System erstellt automatisch ein *Lokales Benutzerprofil* für jeden Benutzer, wenn sich der Benutzer zum ersten Mal beim Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b287b-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="b287b-107">Das System verwaltet automatisch die Einstellungen für die Arbeitsumgebung der einzelnen Benutzer in einem Benutzerprofil auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="b287b-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="b287b-108">Windows Vista und höher: Benutzerprofile werden über das System Steuerungselement **Benutzerkonten** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b287b-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="b287b-109">Windows 2000 und Windows XP: um ein Benutzerprofil zu kopieren oder zu löschen, wählen Sie in der Systemsteuerung die Option **System** , dann die Registerkarte **erweitert** und dann im Bereich **Benutzerprofil** die Schaltfläche **Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="b287b-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="b287b-110">Das Profil des Benutzers wird nicht automatisch geladen, wenn der Benutzer mit der [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) -Funktion angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b287b-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="b287b-111">Wenn Sie ein Benutzerprofil Programm gesteuert laden möchten, verwenden Sie die [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b287b-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="b287b-112">Um ein von **LoadUserProfile** geladenes Benutzerprofil zu entladen, nennen Sie die [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b287b-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
