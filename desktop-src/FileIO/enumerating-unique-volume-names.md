---
description: Informationen zum erhalten eines VolumeGuid-Pfads für jedes lokale Volume, das einem Laufwerksbuchstaben zugeordnet ist, der zurzeit auf dem Computer verwendet wird.
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: Auflisten von Volume-GUID-Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350297"
---
# <a name="enumerating-volume-guid-paths"></a>Auflisten von Volume-GUID-Pfaden

Das Codebeispiel in diesem Thema zeigt, wie Sie einen **VolumeGuid** -Pfad für jedes lokale Volume abrufen, das einem Laufwerksbuchstaben zugeordnet ist, der zurzeit auf dem Computer verwendet wird.

Im Codebeispiel wird die [**getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) -Funktion verwendet.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



Ein Beispiel für das Auflisten aller lokal angeschlossenen Volumes und das Anzeigen des Geräte Pfads, des Volume- **GUID** -Pfads und der bereitgestellten Pfade (einschließlich der Laufwerk Buchstaben) finden Sie unter [Anzeigen von volumepfaden](displaying-volume-paths.md).

 

 



