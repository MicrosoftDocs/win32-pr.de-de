---
description: Schreiben in ein E-Mail-Lot Das Schreiben in ein E-Mail-Lot ähnelt dem Schreiben in eine Standarddatenträgerdatei.
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: Schreiben in ein Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13c31fd6b24217267b394f80c2dcdf551b6949f8692811173021fb78326f2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359309"
---
# <a name="writing-to-a-mailslot"></a>Schreiben in ein Mailslot

Das Schreiben in ein E-Mail-Lot ähnelt dem Schreiben in eine Standarddatenträgerdatei. Im folgenden Code werden die [**Funktionen CreateFile,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)und [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) verwendet, um eine kurze Nachricht in einem Mailslot zu speichern. Die Nachricht wird an den Maillotserver mit dem Namen "sample \_ mailslot" auf dem lokalen Computer übertragen. Der Code wird unter der Annahme ausgeführt, dass der Maillotserver bereits erstellt wurde.


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



Im Folgenden finden Sie die Ausgabe, die angezeigt wird, wenn dieses Beispiel mit dem in Lesen aus einem Mailslot gezeigten [Mailslotserver ausgeführt wird.](reading-from-a-mailslot.md)

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
