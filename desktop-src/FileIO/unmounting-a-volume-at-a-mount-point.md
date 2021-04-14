---
description: Löschen eines eingebundenen Ordners mit der DeleteVolumeMountPoint-Funktion
ms.assetid: 33049110-acf8-4db5-a9c4-bd4a884c8590
title: Löschen eines eingebundenen Ordners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b177aa2010d33b84aa98993d66952c50acb014e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527269"
---
# <a name="deleting-a-mounted-folder"></a>Löschen eines eingebundenen Ordners

Das Codebeispiel in diesem Thema zeigt, wie ein bereitgestellter Ordner mit der [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) -Funktion gelöscht wird. Weitere Informationen finden Sie unter [Erstellen eingebundenes Ordner](mounting-and-dismounting-a-volume.md).


```C++
#define _WIN32_WINNT 0x0501

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void
Syntax (TCHAR *argv)
{
   _tprintf(TEXT("%s unmounts a volume from a volume mount point\n"), 
          argv);
   _tprintf(TEXT("For example: \"%s c:\\mnt\\fdrive\\\"\n"), argv);
}

int _tmain(int argc, TCHAR *argv[])
{
   BOOL bFlag;

   if (argc != 2)
   {
      Syntax (argv[0]);
      return (-1);
   }

// We should do some error checking on the path argument, such as
// ensuring that there is a trailing backslash.

   bFlag = DeleteVolumeMountPoint(
              argv[1] // Path of the volume mount point
           );

   _tprintf(TEXT("\n%s %s in unmounting the volume at %s\n"), argv[0],
           bFlag ? TEXT("succeeded") : TEXT("failed"), argv[1]);

   return (bFlag);
}
```



 

 



