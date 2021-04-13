---
title: Zuweisen eines Laufwerks zu einer Freigabe
description: Im folgenden Beispiel wird veranschaulicht, wie Sie einen Laufwerk Buchstaben mit einer Remote Server Freigabe verbinden, indem Sie die WNetAddConnection2-Funktion verwenden. Im Beispiel wird der Benutzer informiert, ob der-Befehl erfolgreich war.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cb4c930250f74cc549d9b5a31f121b92abad0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390660"
---
# <a name="assigning-a-drive-to-a-share"></a>Zuweisen eines Laufwerks zu einer Freigabe

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Laufwerk Buchstaben mit einer Remote Server Freigabe verbinden, indem Sie die [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) -Funktion verwenden. Im Beispiel wird der Benutzer informiert, ob der-Befehl erfolgreich war.

Um das folgende Codebeispiel zu testen, führen Sie die folgenden Schritte aus:

1.  Ändern Sie die folgenden Zeilen in gültige Zeichen folgen:

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Fügen Sie die Datei einer Konsolenanwendung mit dem Namen AddConn2 hinzu.
3.  Verknüpfen Sie die MPR der Bibliothek. LIB zur compilerliste der Bibliotheken.
4.  Kompilieren Sie das Programm AddConn2.EXE, und führen Sie es aus.


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 