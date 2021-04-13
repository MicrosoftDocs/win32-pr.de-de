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
# <a name="assigning-a-drive-to-a-share"></a><span data-ttu-id="e8b56-104">Zuweisen eines Laufwerks zu einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="e8b56-104">Assigning a Drive to a Share</span></span>

<span data-ttu-id="e8b56-105">Im folgenden Beispiel wird veranschaulicht, wie Sie einen Laufwerk Buchstaben mit einer Remote Server Freigabe verbinden, indem Sie die [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8b56-105">The following example demonstrates how to connect a drive letter to a remote server share with a call to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function.</span></span> <span data-ttu-id="e8b56-106">Im Beispiel wird der Benutzer informiert, ob der-Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e8b56-106">The sample informs the user whether or not the call was successful.</span></span>

<span data-ttu-id="e8b56-107">Um das folgende Codebeispiel zu testen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e8b56-107">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="e8b56-108">Ändern Sie die folgenden Zeilen in gültige Zeichen folgen:</span><span class="sxs-lookup"><span data-stu-id="e8b56-108">Change the following lines to valid strings:</span></span>

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  <span data-ttu-id="e8b56-109">Fügen Sie die Datei einer Konsolenanwendung mit dem Namen AddConn2 hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8b56-109">Add the file to a console application called AddConn2.</span></span>
3.  <span data-ttu-id="e8b56-110">Verknüpfen Sie die MPR der Bibliothek. LIB zur compilerliste der Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="e8b56-110">Link the library MPR.LIB to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="e8b56-111">Kompilieren Sie das Programm AddConn2.EXE, und führen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="e8b56-111">Compile and run the program AddConn2.EXE.</span></span>


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



 

 