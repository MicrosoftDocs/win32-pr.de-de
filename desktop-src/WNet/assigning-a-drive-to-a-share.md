---
title: Zuweisen eines Laufwerks zu einer Freigabe
description: Im folgenden Beispiel wird veranschaulicht, wie ein Laufwerkbuchstabe mit einer Remoteserverfreigabe mit einem Aufruf der WNetAddConnection2-Funktion verbunden wird. Im Beispiel wird der Benutzer darüber informiert, ob der Aufruf erfolgreich war.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37095f085b3124cfaa049de4bf61ae830c94191c94c5993f7532920b122b63d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053378"
---
# <a name="assigning-a-drive-to-a-share"></a>Zuweisen eines Laufwerks zu einer Freigabe

Im folgenden Beispiel wird veranschaulicht, wie ein Laufwerkbuchstabe mit einer Remoteserverfreigabe mit einem Aufruf der [**WNetAddConnection2-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) verbunden wird. Im Beispiel wird der Benutzer darüber informiert, ob der Aufruf erfolgreich war.

Führen Sie die folgenden Schritte aus, um das folgende Codebeispiel zu testen:

1.  Ändern Sie die folgenden Zeilen in gültige Zeichenfolgen:

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Fügen Sie die Datei einer Konsolenanwendung namens AddConn2 hinzu.
3.  Verknüpfen Sie die Bibliotheks-MPR. LIB zur Compilerliste der Bibliotheken.
4.  Kompilieren Sie das Programm, und führen Sie es AddConn2.EXE aus.


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



 

 