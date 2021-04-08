---
description: Eine Anwendung kann den Inhalt eines Verzeichnisses und seiner Unterverzeichnisse mithilfe von Änderungs Benachrichtigungen überwachen.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Abrufen von Benachrichtigungen über Verzeichnisänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753561"
---
# <a name="obtaining-directory-change-notifications"></a>Abrufen von Benachrichtigungen über Verzeichnisänderungen

Eine Anwendung kann den Inhalt eines Verzeichnisses und seiner Unterverzeichnisse mithilfe von Änderungs Benachrichtigungen überwachen. Das warten auf eine Änderungs Benachrichtigung ähnelt dem Ausführen eines Lesevorgangs für ein Verzeichnis und ggf. seiner Unterverzeichnisse. Wenn sich im zu überwachenden Verzeichnis etwas ändert, wird der Lesevorgang abgeschlossen. Beispielsweise kann eine Anwendung diese Funktionen verwenden, um ein Verzeichnis aufzulisten, wenn ein Dateiname im überwachten Verzeichnis geändert wird.

Eine Anwendung kann eine Reihe von Bedingungen angeben, die eine Änderungs Benachrichtigung mithilfe der [**findfirstchangenotifi-**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) Funktion auslöst. Zu den Bedingungen zählen Änderungen an Dateinamen, Verzeichnisnamen, Attributen, Dateigröße, Zeitpunkt des letzten Schreibzugriffs und Sicherheit. Diese Funktion gibt auch ein Handle zurück, auf das mithilfe der Wait- [Funktionen](/windows/desktop/Sync/wait-functions)gewartet werden kann. Wenn die Warte Bedingung erfüllt ist, kann [**findnextchangenotifiverwendet**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) werden, um ein Benachrichtigungs handle bereitzustellen, das auf nachfolgende Änderungen gewartet werden soll. Diese Funktionen geben jedoch nicht die tatsächliche Änderung an, die die Warte Bedingung erfüllt hat.

Verwenden Sie [**findclosechangenotifi,**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) um das Benachrichtigungs Handle zu schließen.

Um Informationen über die jeweilige Änderung im Rahmen der Benachrichtigung abzurufen, verwenden Sie die Funktion "read [**directorychangesw**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) ". Mit dieser Funktion können Sie auch eine Vervollständigungs Routine bereitstellen.

Informationen zum Nachverfolgen von Änderungen auf einem Volume finden Sie unter [Change Journals](change-journals.md).

Im folgenden Beispiel wird die Verzeichnisstruktur auf Änderungen des Verzeichnis namens überwacht. Außerdem wird ein Verzeichnis für Dateinamen Änderungen überwacht. Im Beispiel wird die [**findfirstchangenotifi-**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) Funktion verwendet, um zwei Benachrichtigungs Handles zu erstellen, und die [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) -Funktion, die auf die Handles gewartet werden soll. Wenn ein Verzeichnis in der Struktur erstellt oder gelöscht wird, sollte im Beispiel die gesamte Verzeichnisstruktur aktualisiert werden. Wenn eine Datei im Verzeichnis erstellt oder gelöscht wird, sollte im Beispiel das Verzeichnis aktualisiert werden.

> [!Note]
>
> Dieses vereinfachte Beispiel verwendet die [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion für das Beenden und bereinigen. komplexere Anwendungen sollten jedoch immer eine geeignete Ressourcenverwaltung wie z. b. " [**findclosechangenotifi"**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) verwenden.

 


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



 

 
