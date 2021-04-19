---
description: In Windows Vista und Windows Server 2008 haben sich die Standard Speicherorte für Benutzerdaten und Systemdaten geändert.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Verknüpfungs Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360204"
---
# <a name="junction-points"></a><span data-ttu-id="1d848-103">Verknüpfungs Punkte</span><span class="sxs-lookup"><span data-stu-id="1d848-103">Junction Points</span></span>

<span data-ttu-id="1d848-104">In Windows Vista und Windows Server 2008 haben sich die Standard Speicherorte für Benutzerdaten und Systemdaten geändert.</span><span class="sxs-lookup"><span data-stu-id="1d848-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="1d848-105">Beispielsweise werden Benutzerdaten, die zuvor im Verzeichnis "% System Drive% \\ Documents and Settings" gespeichert waren, jetzt im Verzeichnis "% System Drive% Users" gespeichert \\ .</span><span class="sxs-lookup"><span data-stu-id="1d848-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="1d848-106">Aus Gründen der Abwärtskompatibilität haben die alten Standorte Verbindungspunkte, die auf die neuen Speicherorte verweisen.</span><span class="sxs-lookup"><span data-stu-id="1d848-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="1d848-107">Beispiel: "c: \\ Dokumente und Einstellungen" ist jetzt ein Verknüpfungs Punkt, der auf "c: Users" zeigt \\ .</span><span class="sxs-lookup"><span data-stu-id="1d848-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="1d848-108">Sicherungs Anwendungen müssen in der Lage sein, Verknüpfungs Punkte zu sichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d848-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="1d848-109">Diese Verknüpfungs Punkte können wie folgt identifiziert werden:</span><span class="sxs-lookup"><span data-stu-id="1d848-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="1d848-110">Die Attribute "File Attribute Analyse \_ \_ Point", " \_ file \_ Attribute Hidden" und "File Attribute \_ System File" sind \_ \_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1d848-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="1d848-111">Außerdem haben Sie Zugriffs Steuerungs Listen (ACLs) festgelegt, um allen Benutzern den Lesezugriff zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="1d848-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="1d848-112">Anwendungen, die einen bestimmten Pfad aufzurufen, können diese Verknüpfungs Punkte durchlaufen, wenn Sie über die erforderlichen Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="1d848-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="1d848-113">Allerdings führt der Versuch, den Inhalt der Verknüpfungs Punkte aufzulisten, zu Fehlern.</span><span class="sxs-lookup"><span data-stu-id="1d848-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="1d848-114">Aus zwei Gründen ist es wichtig, dass Sicherungs Anwendungen diese Verknüpfungs Punkte nicht durchlaufen oder versuchen, Daten darunter zu sichern:</span><span class="sxs-lookup"><span data-stu-id="1d848-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="1d848-115">Dies kann dazu führen, dass die Sicherungs Anwendung die gleichen Daten mehrmals sichert.</span><span class="sxs-lookup"><span data-stu-id="1d848-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="1d848-116">Sie kann auch zu Zyklen (Zirkel Verweise) führen.</span><span class="sxs-lookup"><span data-stu-id="1d848-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="1d848-117">Per-User-und System Anschlüsse</span><span class="sxs-lookup"><span data-stu-id="1d848-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="1d848-118">Die Verknüpfungs Punkte, die zur Bereitstellung von Datei-und Registrierungsvirtualisierung in Windows Vista und Windows Server 2008 verwendet werden, können in zwei Klassen unterteilt werden: pro Benutzer-und System Anschlüsse.</span><span class="sxs-lookup"><span data-stu-id="1d848-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="1d848-119">Pro-Benutzer-Verbindungen werden im Profil jedes einzelnen Benutzers erstellt, um die Abwärtskompatibilität für Benutzer Anwendungen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1d848-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="1d848-120">Der Verknüpfungs Punkt bei c: \\ Benutzer \\ *Benutzername* \\ meine Dokumente, die auf c: \\ Benutzer \\ *Benutzername* \\ Dokumente zeigt, ist ein Beispiel für eine benutzerspezifische Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="1d848-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="1d848-121">Benutzerspezifische Verbindungen werden vom Profil Dienst erstellt, wenn das Profil des Benutzers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d848-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="1d848-122">Die anderen Verbindungen sind System Knotenpunkte, die sich nicht unter dem Benutzer \\ *Namen* Verzeichnis des Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="1d848-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="1d848-123">Zu den System Knotenpunkten zählen beispielsweise folgende:</span><span class="sxs-lookup"><span data-stu-id="1d848-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="1d848-124">Dokumente und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1d848-124">Documents and Settings</span></span>
-   <span data-ttu-id="1d848-125">Verbindungen in den Benutzerprofilen "alle Benutzer", "öffentlich" und "Standard"</span><span class="sxs-lookup"><span data-stu-id="1d848-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="1d848-126">System Anschlüsse werden von userenv.dll erstellt, wenn Sie von der Windows-Willkommensseite aufgerufen wird (auch als "Machine out-of-Box-do" bezeichnet oder "MOOBE" bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="1d848-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="1d848-127">Wenn der Benutzer die Systemsprache in eine andere Sprache als Englisch ändert, werden die Verknüpfungs Punkte pro Benutzer und System mit lokalisierten Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d848-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 



