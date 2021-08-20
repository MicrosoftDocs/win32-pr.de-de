---
description: Windows Resource Protection (WRP) verhindert den Austausch wichtiger Systemdateien, Ordner und Registrierungsschlüssel, die als Teil von Windows Vista oder Windows Server 2008 installiert werden.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Erkennen des Ressourcenaustauschs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e452b9fba0a8002e13d7fc309ff3c8a12ec114a6a33b1bd7d8d253d710ffa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053218"
---
# <a name="detecting-resource-replacement"></a>Erkennen des Ressourcenaustauschs

Windows Resource Protection (WRP) verhindert den Austausch wichtiger Systemdateien, Ordner und Registrierungsschlüssel, die als Teil von Windows Vista oder Windows Server 2008 installiert werden.

WRP schützt Dateien, Ordner und Registrierungsschlüssel auf Windows Vista oder Windows Server 2008, indem versuche erkannt und verhindert werden, geschützte Ressourcen zu ersetzen. Dieser Schutz basiert auf einer Windows DACL (Discretionary Access Control List) und Zugriffssteuerungslisten (ACL), die für geschützte Ressourcen definiert sind. Die Berechtigung für vollzugriff zum Ändern von WRP-geschützten Ressourcen ist auf TrustedInstaller beschränkt. WRP-geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenersetzungsmechanismen](supported-file-replacement-mechanisms.md) mit dem Installerdienst für Windows Module geändert werden. Anwendungen, die versuchen, eine DURCH WRP geschützte Ressource zu ändern, ändern die Ressource nie und erhalten möglicherweise eine Fehlermeldung mit dem Hinweis, dass der Zugriff auf die Ressource verweigert wurde.

Anwendungen und Installationsprogramme können die Funktionen [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) und [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) verwenden, um zu bestimmen, ob eine Datei oder ein Registrierungsschlüssel geschützt ist.

**Windows Server 2003 und Windows XP: **

Windows File Protection (WFP) schützt Systemdateien, indem versucht wird, geschützte Systemdateien zu ersetzen. Dieser Schutz wird ausgelöst, nachdem WFP eine Verzeichnisänderungsbenachrichtigung für eine Datei in einem geschützten Verzeichnis empfängt. Wenn WFP diese Benachrichtigung empfängt, wird ermittelt, welche Datei geändert wurde. Wenn die Datei geschützt ist, sucht WFP die Dateisignatur in einer Katalogdatei, um zu ermitteln, ob die neue Datei die richtige Version ist. Wenn die Dateiversion nicht korrekt ist, ersetzt das System die Datei durch die richtige Version aus dem Cache oder dem Verteilungsmedium, je nachdem, ob sich die Datei im Cache befindet. WFP sucht in der folgenden Reihenfolge nach der richtigen Datei:

1.  Durchsuchen Sie das Cacheverzeichnis.
2.  Suchen Sie den Netzwerkinstallationspfad, wenn das System mithilfe der Netzwerkinstallation installiert wurde.
3.  Suchen Sie nach einer Windows CD-ROM, wenn das System von CD-ROM installiert wurde.

Wenn WFP die Datei an den ersten beiden Speicherorten nicht automatisch finden kann, wird die folgende Meldung angezeigt:

![WFP-Meldung, die angezeigt wird, wenn die Datei nicht im Cacheverzeichnis oder im Netzwerkinstallationspfad gefunden wurde](images/wfp-1.png)

Wenn das System mithilfe einer CD-ROM installiert wurde, zeigt WFP die folgende Meldung an:

![WFP-Meldung, die angezeigt wird, um den Benutzer zum Einfügen von Windows-CD-ROM aufzufordern](images/wfp-2.png)

Wenn kein Administrator angemeldet ist, kann WFP keines dieser Dialogfelder anzeigen. WFP zeigt das Dialogfeld an, nachdem sich ein Administrator angemeldet hat.

WFP protokolliert auch den Dateiersetzungsversuch im Systemereignisprotokoll. Wenn der Administrator die Wiederherstellung der richtigen Datei abgebrochen hat, protokolliert WFP den Abbruch.

## <a name="retrieving-the-list-of-protected-files"></a>Abrufen der Liste der geschützten Dateien

Das folgende Beispiel zeigt, wie Anwendungen und Installationsprogramme die [**SfcGetNextProtectedFile-Funktion**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) verwenden können, um die vollständige Liste der geschützten Dateien abzurufen.


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



 

 



