---
description: Schreiben in einen Mailslot Das Schreiben in einen Mailslot ähnelt dem Schreiben in eine Standard Datenträger-Datei.
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: Schreiben in einen postslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568727f7a83d46925f3e681f3dec4906903ca8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350879"
---
# <a name="writing-to-a-mailslot"></a><span data-ttu-id="af71e-104">Schreiben in einen postslot</span><span class="sxs-lookup"><span data-stu-id="af71e-104">Writing to a Mailslot</span></span>

<span data-ttu-id="af71e-105">Das Schreiben in einen Mailslot ähnelt dem Schreiben in eine Standard Datenträger-Datei.</span><span class="sxs-lookup"><span data-stu-id="af71e-105">Writing to a mailslot is similar to writing to a standard disk file.</span></span> <span data-ttu-id="af71e-106">Der folgende Code verwendet die Funktionen "up [**", "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" und " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) ", um eine kurze Nachricht in einem postslot zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="af71e-106">The following code uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) functions to put a short message in a mailslot.</span></span> <span data-ttu-id="af71e-107">Die Nachricht wird an den Mailslot-Server mit dem Namen "Sample \_ Mailslot" auf dem lokalen Computer übertragen.</span><span class="sxs-lookup"><span data-stu-id="af71e-107">The message is broadcast to the mailslot server named "sample\_mailslot" on the local computer.</span></span> <span data-ttu-id="af71e-108">Der Code unter der Annahme, dass der Mailslot-Server bereits erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="af71e-108">The code operates under the assumption that the mailslot server was already created.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WriteSlot(HANDLE hSlot, LPCTSTR lpszMessage)
{
   BOOL fResult; 
   DWORD cbWritten; 
 
   fResult = WriteFile(hSlot, 
     lpszMessage, 
     (DWORD) (lstrlen(lpszMessage)+1)*sizeof(TCHAR),  
     &cbWritten, 
     (LPOVERLAPPED) NULL); 
 
   if (!fResult) 
   { 
      printf("WriteFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   printf("Slot written to successfully.\n"); 

   return TRUE;
}

int main()
{ 
   HANDLE hFile; 

   hFile = CreateFile(SlotName, 
     GENERIC_WRITE, 
     FILE_SHARE_READ,
     (LPSECURITY_ATTRIBUTES) NULL, 
     OPEN_EXISTING, 
     FILE_ATTRIBUTE_NORMAL, 
     (HANDLE) NULL); 
 
   if (hFile == INVALID_HANDLE_VALUE) 
   { 
      printf("CreateFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   WriteSlot(hFile, TEXT("Message one for mailslot."));
   WriteSlot(hFile, TEXT("Message two for mailslot."));

   Sleep(5000);

   WriteSlot(hFile, TEXT("Message three for mailslot."));
 
   CloseHandle(hFile); 
 
   return TRUE;
}
```



<span data-ttu-id="af71e-109">Im folgenden wird die Ausgabe angezeigt, die angezeigt wird, wenn dieses Beispiel mit dem Mailslot-Server ausgeführt wird, der beim [Lesen aus einem postslot](reading-from-a-mailslot.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="af71e-109">The following is the output that is displayed when this example is run with the mailslot server shown in [Reading from a Mailslot](reading-from-a-mailslot.md).</span></span>

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
