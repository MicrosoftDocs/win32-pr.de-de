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
# <a name="detecting-resource-replacement"></a>Erkennen von Ressourcenaustausch

Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil von Windows Vista oder Windows Server 2008 installiert werden.

WRP schützt Dateien, Ordner und Registrierungsschlüssel unter Windows Vista oder Windows Server 2008 durch erkennen und verhindern von versuchen, geschützte Ressourcen zu ersetzen. Dieser Schutz basiert auf einer Windows-Zugriffs Steuerungs Liste (DACL) und einer Zugriffs Steuerungs Liste (ACL), die für geschützte Ressourcen definiert ist. Die Berechtigung für den Vollzugriff zum Ändern von durch WRP geschützten Ressourcen ist auf Treuhänder beschränkt. Durch WRP geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenaustausch Mechanismen](supported-file-replacement-mechanisms.md) mit dem Windows-Modul Installations Dienst geändert werden. Anwendungen, die versuchen, eine durch WRP geschützte Ressource zu ändern, ändern niemals die Ressource und erhalten möglicherweise eine Fehlermeldung, die besagt, dass der Zugriff auf die Ressource verweigert wurde.

Anwendungen und Installationsprogramme können die Funktionen [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) und [**sfciskeyprotected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) verwenden, um zu bestimmen, ob eine Datei oder ein Registrierungsschlüssel geschützt ist.

* * Windows Server 2003 und Windows XP: * *

Der Windows-Datei Schutz (WFP) schützt Systemdateien durch das Erkennen von versuchen, geschützte Systemdateien zu ersetzen. Dieser Schutz wird ausgelöst, nachdem WFP eine Verzeichnis Änderungs Benachrichtigung für eine Datei in einem geschützten Verzeichnis erhalten hat. Wenn WFP diese Benachrichtigung empfängt, wird ermittelt, welche Datei geändert wurde. Wenn die Datei geschützt ist, sucht WFP in einer Katalog Datei nach der Datei Signatur, um zu bestimmen, ob die neue Datei die richtige Version hat. Wenn die Dateiversion nicht korrekt ist, ersetzt das System die Datei durch die richtige Version aus dem Cache oder den Verteilungs Medien, je nachdem, ob sich die Datei im Cache befindet. WFP sucht in der folgenden Reihenfolge nach der richtigen Datei:

1.  Durchsuchen Sie das Cache Verzeichnis.
2.  Durchsuchen Sie den Netzwerk Installationspfad, wenn das System mithilfe der Netzwerk Installation installiert wurde.
3.  Suchen Sie auf einer Windows-CD-ROM, wenn das System von CD-ROM installiert wurde.

Wenn die Datei an den ersten beiden Speicherorten von WFP nicht automatisch gefunden werden kann, wird die folgende Meldung angezeigt:

![WFP-Meldung angezeigt, wenn die Datei nicht im Cache Verzeichnis oder im Netzwerk Installationspfad gefunden wurde](images/wfp-1.png)

Wenn das System mit einer CD-ROM installiert wurde, zeigt WFP die folgende Meldung an:

![WFP-Meldung, die den Benutzer zum Einfügen der Windows-CD-ROM auffordert](images/wfp-2.png)

Wenn ein Administrator nicht angemeldet ist, kann WFP keines dieser Dialogfelder anzeigen. WFP zeigt das Dialogfeld an, nachdem sich ein Administrator anmeldet.

WFP protokolliert auch den Datei Ersetzungs Versuch im System Ereignisprotokoll. Wenn der Administrator die Wiederherstellung der richtigen Datei abgebrochen hat, protokolliert WFP den Abbruch.

## <a name="retrieving-the-list-of-protected-files"></a>Abrufen der Liste der geschützten Dateien

Im folgenden Beispiel wird gezeigt, wie Anwendungen und Installer die [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) -Funktion verwenden können, um die komplette Liste der geschützten Dateien zu erhalten.


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



 

 



