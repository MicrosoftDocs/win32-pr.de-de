---
description: Um ein Verzeichnis zusammen mit den darin enthaltenen Dateien und Unterverzeichnissen an einen anderen Speicherort zu verschieben, rufen Sie die Funktion MoveFileEx, MoveFileWithProgress oder MoveFileTransacted auf.
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: Verschieben von Verzeichnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da891e22c2840ad9460f5fb43c8cc1b130905b86de80a988be2eeeb9a4010ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951139"
---
# <a name="moving-directories"></a>Verschieben von Verzeichnissen

Um ein Verzeichnis zusammen mit den darin enthaltenen Dateien und Unterverzeichnissen an einen anderen Speicherort zu verschieben, rufen Sie die Funktion [**MoveFileEx,**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)oder [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) auf. Die [**MoveFileWithProgress-Funktion**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) verfügt über die gleiche Funktionalität wie [**MoveFileEx,**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)mit der Ausnahme, dass **Sie mit MoveFileWithProgress** eine Rückrufroutine angeben können, die Benachrichtigungen zum Status des Vorgangs empfängt. Mit der [**MoveFileTransacted-Funktion**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) können Sie den Vorgang als transaktiven Vorgang ausführen.

Im folgenden Beispiel wird die Verwendung der [**MoveFileEx-Funktion**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) mit einem Verzeichnis veranschaulicht.


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



 

 



