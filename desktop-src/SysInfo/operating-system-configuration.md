---
description: Das Windows-Verzeichnis ist das Verzeichnis, das Windows-basierte Anwendungen, Initialisierungsdateien und Hilfedateien enthält. Die GetWindowsDirectory-Funktion Ruft den Pfad zu diesem Verzeichnis ab.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Konfiguration des Betriebssystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217146"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="c9d9a-104">Konfiguration des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="c9d9a-104">Operating System Configuration</span></span>

<span data-ttu-id="c9d9a-105">Das *Windows-Verzeichnis* ist das Verzeichnis, das Windows-basierte Anwendungen, Initialisierungsdateien und Hilfedateien enthält.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="c9d9a-106">Die [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion Ruft den Pfad zu diesem Verzeichnis ab.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="c9d9a-107">Das *System Verzeichnis* ist das Verzeichnis, das Dynamic Link Libraries, Treiber und Schriftart Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="c9d9a-108">Die [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion Ruft den Pfad zu diesem Verzeichnis ab.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="c9d9a-109">Die [**GetUsername**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) -Funktion Ruft den Namen des Benutzers ab, der derzeit beim System angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="c9d9a-110">Der Benutzername ist entweder der Anmelde Name oder der vollständige Name des Benutzers, sofern er in der Registrierung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="c9d9a-111">Eine *Umgebungsvariable* ist eine symbolische Variable, die ein Element des Systems darstellt, z. b. einen Pfad, einen Dateinamen oder andere Literaldaten.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="c9d9a-112">Der Umgebungsvariablen Pfad stellt z. b. die Verzeichnisse dar, in denen nach ausführbaren Dateien gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="c9d9a-113">Wenn sich ein Benutzer anmeldet, initialisiert das System Umgebungsvariablen basierend auf dem Umgebungs Abschnitt der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="c9d9a-114">Die [**expandenvironment Strings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) -Funktion Ruft die Werte der angegebenen Umgebungsvariablen ab.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="c9d9a-115">Weitere Informationen werden von der [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) -Schnittstelle bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
