---
description: Zum Verschieben eines Verzeichnisses an einen anderen Speicherort, zusammen mit den darin enthaltenen Dateien und Unterverzeichnissen, wird die Funktion MoveFileEx, movefilewithprogress oder movefiletransktive aufgerufen.
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: Verschieben von Verzeichnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56167f0831894350a044104bce1f41ef3c5770ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366476"
---
# <a name="moving-directories"></a>Verschieben von Verzeichnissen

Zum Verschieben eines Verzeichnisses an einen anderen Speicherort, zusammen mit den darin enthaltenen Dateien und Unterverzeichnissen, wird die Funktion [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), [**movefilewithprogress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)oder [**movefiletransktive**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) aufgerufen. Die Funktion " [**fivefilewithprogress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) " verfügt über die gleiche Funktionalität wie " [**muvefileex**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)", **mit dem Unterschied, dass "** " mit "" "mit" "" "mit" "" "mit" ". Die Funktion " [**fivefiletransktive**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) " ermöglicht es Ihnen, den Vorgang als transaktiven Vorgang auszuführen.

Das folgende Beispiel veranschaulicht die Verwendung der Funktion " [**fivefileex**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) " mit einem Verzeichnis.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    printf("\n");
    if( argc != 3 )
    {
        printf("ERROR:  Incorrect number of arguments\n\n");
        printf("Description:\n");
        printf("  Moves a directory and its contents\n\n");
        printf("Usage:\n");
        _tprintf(TEXT("  %s [source_dir] [target_dir]\n\n"), argv[0]);
        printf("  The target directory cannot exist already.\n\n");
        return;
    }

    // Move the source directory to the target directory location.
    // The target directory must be on the same drive as the source.
    // The target directory cannot already exist.

    if (!MoveFileEx(argv[1], argv[2], MOVEFILE_WRITE_THROUGH))
    { 
        printf ("MoveFileEx failed with error %d\n", GetLastError());
        return;
    }
    else _tprintf(TEXT("%s has been moved to %s\n"), argv[1], argv[2]);
}
```



 

 



