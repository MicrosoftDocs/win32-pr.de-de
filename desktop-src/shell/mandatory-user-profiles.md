---
description: Bei einem obligatorischen Benutzerprofil handelt es sich um eine besondere Art von vorkonfiguriertem Roamingbenutzerprofil, mit dem Administratoren Einstellungen für Benutzer angeben können.
title: Verbindliche Benutzerprofile
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524424"
---
# <a name="mandatory-user-profiles"></a><span data-ttu-id="008f2-103">Verbindliche Benutzerprofile</span><span class="sxs-lookup"><span data-stu-id="008f2-103">Mandatory User Profiles</span></span>

<span data-ttu-id="008f2-104">Bei einem obligatorischen Benutzerprofil handelt es sich um eine besondere Art von vorkonfiguriertem [Roamingbenutzerprofil](roaming-user-profiles.md) , mit dem Administratoren Einstellungen für Benutzer angeben können.</span><span class="sxs-lookup"><span data-stu-id="008f2-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="008f2-105">Mit obligatorischen Benutzerprofilen kann ein Benutzer seinen Desktop ändern, die Änderungen werden jedoch nicht gespeichert, wenn sich der Benutzer abmeldet.</span><span class="sxs-lookup"><span data-stu-id="008f2-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="008f2-106">Wenn sich der Benutzer das nächste Mal anmeldet, wird das vom Administrator erstellte obligatorische Benutzerprofil heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="008f2-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="008f2-107">Es gibt zwei Arten von obligatorischen Profilen: *normale verbindliche* Profile und *Super verbindliche* Profile.</span><span class="sxs-lookup"><span data-stu-id="008f2-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="008f2-108">Benutzerprofile werden zu obligatorischen Profilen, wenn der Administrator die Datei "Ntuser. dat" (die Registrierungs Struktur) auf dem Server in "Ntuser. man" umbenennt.</span><span class="sxs-lookup"><span data-stu-id="008f2-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="008f2-109">Die. man-Erweiterung bewirkt, dass das Benutzerprofil ein Schreib geschütztes Profil ist.</span><span class="sxs-lookup"><span data-stu-id="008f2-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="008f2-110">Benutzerprofile werden äußerst *obligatorisch* , wenn der Ordnername des Profil Pfads in. man; Beispiel: \\ \\ Server \\ Freigabe \\ mandatoryprofile. man \\ .</span><span class="sxs-lookup"><span data-stu-id="008f2-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="008f2-111">Super verbindliche Benutzerprofile ähneln normalen obligatorischen Profilen, mit der Ausnahme, dass sich Benutzer, die über Super verbindliche Profile verfügen, nicht anmelden können, wenn der Server, auf dem das obligatorische Profil gespeichert ist, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="008f2-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="008f2-112">Benutzer mit normalen obligatorischen Profilen können sich mit der lokal zwischengespeicherten Kopie des obligatorischen Profils anmelden.</span><span class="sxs-lookup"><span data-stu-id="008f2-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="008f2-113">Nur Systemadministratoren können Änderungen an obligatorischen Benutzerprofilen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="008f2-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



