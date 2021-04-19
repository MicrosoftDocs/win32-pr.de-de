---
description: Die Hardware Konfigurationsfunktionen rufen Informationen wie Prozessor, Hardwareprofil und Tastatur Informationen ab.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350891"
---
# <a name="hardware-configuration"></a><span data-ttu-id="f0a4d-103">Hardware Configuration</span><span class="sxs-lookup"><span data-stu-id="f0a4d-103">Hardware Configuration</span></span>

<span data-ttu-id="f0a4d-104">Die Hardware Konfigurationsfunktionen rufen Informationen wie Prozessor, Hardwareprofil und Tastatur Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="f0a4d-104">The hardware configuration functions retrieve information such as processor, hardware profile, and keyboard information.</span></span>

<span data-ttu-id="f0a4d-105">Die Funktion " [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) " ruft Prozessor-und Arbeitsspeicher Informationen ab, wie z. b. die Seitengröße, den OEM-Bezeichner (Original Equipment Manufacturer), die Anzahl und den Typ der Prozessoren, den Adressbereich der Anwendung usw.</span><span class="sxs-lookup"><span data-stu-id="f0a4d-105">The [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function retrieves processor and memory information, such as the page size, original equipment manufacturer (OEM) identifier, number and type of processors, application address range, and so on.</span></span> <span data-ttu-id="f0a4d-106">Die [**isprocessorfeaturepräsentiert**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) -Funktion Ruft Informationen zu den Gleit Komma Vorgängen und Anweisungs Sätzen ab, die vom Prozessor unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f0a4d-106">The [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) function retrieves information about the floating-point operations and instruction sets supported by the processor.</span></span>

<span data-ttu-id="f0a4d-107">Die Funktion " [**gethappthwprofile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) " Ruft Informationen über das Hardwareprofil ab.</span><span class="sxs-lookup"><span data-stu-id="f0a4d-107">The [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) function retrieves information about the hardware profile.</span></span> <span data-ttu-id="f0a4d-108">Das Hardwareprofil enthält Informationen wie den Andock Zustand, Globally Unique Identifier (GUID) und den anzeigen Amen für das Profil.</span><span class="sxs-lookup"><span data-stu-id="f0a4d-108">The hardware profile includes information such as the docking state, globally unique identifier (GUID), and display name for the profile.</span></span> <span data-ttu-id="f0a4d-109">Die [**getkeyboardtype**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) -Funktion ruft solche Informationen als den Typ der Tastatur und die Anzahl der Funktionstasten auf der aktuellen Tastatur ab.</span><span class="sxs-lookup"><span data-stu-id="f0a4d-109">The [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) function retrieves such information as the type of keyboard and the number of function keys on the current keyboard.</span></span>

 

 
