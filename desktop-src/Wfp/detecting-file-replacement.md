---
description: Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil von Windows Vista oder Windows Server 2008 installiert werden.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Erkennen von Ressourcenaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759012"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="ac8e1-103">Erkennen von Ressourcenaustausch</span><span class="sxs-lookup"><span data-stu-id="ac8e1-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="ac8e1-104">Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil von Windows Vista oder Windows Server 2008 installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="ac8e1-105">WRP schützt Dateien, Ordner und Registrierungsschlüssel unter Windows Vista oder Windows Server 2008 durch erkennen und verhindern von versuchen, geschützte Ressourcen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="ac8e1-106">Dieser Schutz basiert auf einer Windows-Zugriffs Steuerungs Liste (DACL) und einer Zugriffs Steuerungs Liste (ACL), die für geschützte Ressourcen definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="ac8e1-107">Die Berechtigung für den Vollzugriff zum Ändern von durch WRP geschützten Ressourcen ist auf Treuhänder beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="ac8e1-108">Durch WRP geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenaustausch Mechanismen](supported-file-replacement-mechanisms.md) mit dem Windows-Modul Installations Dienst geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="ac8e1-109">Anwendungen, die versuchen, eine durch WRP geschützte Ressource zu ändern, ändern niemals die Ressource und erhalten möglicherweise eine Fehlermeldung, die besagt, dass der Zugriff auf die Ressource verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="ac8e1-110">Anwendungen und Installationsprogramme können die Funktionen [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) und [**sfciskeyprotected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) verwenden, um zu bestimmen, ob eine Datei oder ein Registrierungsschlüssel geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="ac8e1-111">\* \* Windows Server 2003 und Windows XP: \* \*</span><span class="sxs-lookup"><span data-stu-id="ac8e1-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="ac8e1-112">Der Windows-Datei Schutz (WFP) schützt Systemdateien durch das Erkennen von versuchen, geschützte Systemdateien zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="ac8e1-113">Dieser Schutz wird ausgelöst, nachdem WFP eine Verzeichnis Änderungs Benachrichtigung für eine Datei in einem geschützten Verzeichnis erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="ac8e1-114">Wenn WFP diese Benachrichtigung empfängt, wird ermittelt, welche Datei geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="ac8e1-115">Wenn die Datei geschützt ist, sucht WFP in einer Katalog Datei nach der Datei Signatur, um zu bestimmen, ob die neue Datei die richtige Version hat.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="ac8e1-116">Wenn die Dateiversion nicht korrekt ist, ersetzt das System die Datei durch die richtige Version aus dem Cache oder den Verteilungs Medien, je nachdem, ob sich die Datei im Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="ac8e1-117">WFP sucht in der folgenden Reihenfolge nach der richtigen Datei:</span><span class="sxs-lookup"><span data-stu-id="ac8e1-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="ac8e1-118">Durchsuchen Sie das Cache Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="ac8e1-119">Durchsuchen Sie den Netzwerk Installationspfad, wenn das System mithilfe der Netzwerk Installation installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="ac8e1-120">Suchen Sie auf einer Windows-CD-ROM, wenn das System von CD-ROM installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="ac8e1-121">Wenn die Datei an den ersten beiden Speicherorten von WFP nicht automatisch gefunden werden kann, wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ac8e1-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![WFP-Meldung angezeigt, wenn die Datei nicht im Cache Verzeichnis oder im Netzwerk Installationspfad gefunden wurde](images/wfp-1.png)

<span data-ttu-id="ac8e1-123">Wenn das System mit einer CD-ROM installiert wurde, zeigt WFP die folgende Meldung an:</span><span class="sxs-lookup"><span data-stu-id="ac8e1-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![WFP-Meldung, die den Benutzer zum Einfügen der Windows-CD-ROM auffordert](images/wfp-2.png)

<span data-ttu-id="ac8e1-125">Wenn ein Administrator nicht angemeldet ist, kann WFP keines dieser Dialogfelder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="ac8e1-126">WFP zeigt das Dialogfeld an, nachdem sich ein Administrator anmeldet.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="ac8e1-127">WFP protokolliert auch den Datei Ersetzungs Versuch im System Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="ac8e1-128">Wenn der Administrator die Wiederherstellung der richtigen Datei abgebrochen hat, protokolliert WFP den Abbruch.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="ac8e1-129">Abrufen der Liste der geschützten Dateien</span><span class="sxs-lookup"><span data-stu-id="ac8e1-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="ac8e1-130">Im folgenden Beispiel wird gezeigt, wie Anwendungen und Installer die [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) -Funktion verwenden können, um die komplette Liste der geschützten Dateien zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ac8e1-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



