---
description: Eine Anwendung kann den Inhalt eines Verzeichnisses und seiner Unterverzeichnisse mithilfe von Änderungsbenachrichtigungen überwachen.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Abrufen von Verzeichnisänderungsbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d94bd2b86aacaf7b32191fd68208bd1400a4b56cf4c55b13102210ffb50f7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048000"
---
# <a name="obtaining-directory-change-notifications"></a>Abrufen von Verzeichnisänderungsbenachrichtigungen

Eine Anwendung kann den Inhalt eines Verzeichnisses und seiner Unterverzeichnisse mithilfe von Änderungsbenachrichtigungen überwachen. Das Warten auf eine Änderungsbenachrichtigung ähnelt dem Warten auf einen ausstehenden Lesevorgang für ein Verzeichnis und bei Bedarf dessen Unterverzeichnisse. Wenn sich etwas innerhalb des verzeichnisses ändert, das beobachtet wird, wird der Lesevorgang abgeschlossen. Beispielsweise kann eine Anwendung diese Funktionen verwenden, um eine Verzeichnisauflistung zu aktualisieren, wenn sich ein Dateiname innerhalb des überwachten Verzeichnisses ändert.

Eine Anwendung kann mithilfe der [**FindFirstChangeNotification-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) eine Reihe von Bedingungen angeben, die eine Änderungsbenachrichtigung auslösen. Die Bedingungen umfassen Änderungen an Dateinamen, Verzeichnisnamen, Attributen, Dateigröße, Zeitpunkt des letzten Schreibzugriffs und Sicherheit. Diese Funktion gibt auch ein Handle zurück, auf das mithilfe der [Wartefunktionen gewartet werden kann.](/windows/desktop/Sync/wait-functions) Wenn die Wartebedingung erfüllt ist, [**kann FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) verwendet werden, um ein Benachrichtigungshand handle zum Warten auf nachfolgende Änderungen zur Verfügung zu stellen. Diese Funktionen geben jedoch nicht die tatsächliche Änderung an, die die Wartebedingung erfüllt hat.

Verwenden [**Sie FindCloseChangeNotification,**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) um das Benachrichtigungshand handle zu schließen.

Verwenden Sie die [**ReadDirectoryChangesW-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) um Informationen über die spezifische Änderung als Teil der Benachrichtigung abzurufen. Mit dieser Funktion können Sie auch eine Vervollständigungsroutine bereitstellen.

Informationen zum Nachverfolgen von Änderungen auf einem Volume finden Sie unter [Change Journal](change-journals.md).

Im folgenden Beispiel wird die Verzeichnisstruktur auf Verzeichnisnamenänderungen überwacht. Außerdem wird ein Verzeichnis auf Dateinamenänderungen überwacht. Im Beispiel wird die [**FindFirstChangeNotification-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) verwendet, um zwei Benachrichtigungshandles zu erstellen, und die [**WaitForMultipleObjects-Funktion,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) um auf die Handles zu warten. Wenn ein Verzeichnis in der Struktur erstellt oder gelöscht wird, sollte im Beispiel die gesamte Verzeichnisstruktur aktualisiert werden. Wenn eine Datei im Verzeichnis erstellt oder gelöscht wird, sollte das Verzeichnis im Beispiel aktualisiert werden.

> [!Note]
>
> In diesem einfachen Beispiel wird die [**ExitProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) zum Beenden und Bereinigten verwendet. Komplexere Anwendungen sollten jedoch immer eine ordnungsgemäße Ressourcenverwaltung wie [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) verwenden, wenn dies angemessen ist.

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
