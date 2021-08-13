---
title: Durchlaufen der Modulliste
description: Im folgenden Beispiel wird eine Liste von Modulen für den angegebenen Prozess erhalten.
ms.assetid: 8efe1e13-6222-496a-bff3-90f53b03c750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f84907cfeba5a9106616d68a3039dd1555e0f4c238ae111df4c886f7664f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419190"
---
# <a name="traversing-the-module-list"></a>Durchlaufen der Modulliste

Im folgenden Beispiel wird eine Liste von Modulen für den angegebenen Prozess erhalten. Die `ListProcessModules` Funktion erstellt mithilfe der [**CreateToolhelp32Snapshot-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) eine Momentaufnahme der Module, die einem bestimmten Prozess zugeordnet sind, und führt dann mithilfe der Funktionen [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) und [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) durch die Liste. Der `dwPID` -Parameter von `ListProcessModules` identifiziert den Prozess, für den Module aufzählt werden sollen, und wird in der Regel durch Aufrufen von **CreateToolhelp32Snapshot** abgerufen, um die auf dem System ausgeführten Prozesse aufzuzählen. Eine einfache Konsolenanwendung, die diese Funktion verwendet, finden Sie unter [Erstellen einer Momentaufnahme und Anzeigen](taking-a-snapshot-and-viewing-processes.md) von Prozessen.

Eine einfache Fehlerberichterstattungsfunktion ( `printError` ) zeigt die Ursache für alle Fehler an, die in der Regel auf Sicherheitseinschränkungen zurückzuführen sind.


```C++
#include <windows.h> 
#include <tlhelp32.h> 
#include <tchar.h> 
 
//  Forward declarations: 
BOOL ListProcessModules( DWORD dwPID ); 
void printError( TCHAR* msg ); 
 
int main( void )
{
  ListProcessModules(GetCurrentProcessId() );
  return 0;
}

BOOL ListProcessModules( DWORD dwPID ) 
{ 
  HANDLE hModuleSnap = INVALID_HANDLE_VALUE; 
  MODULEENTRY32 me32; 
 
//  Take a snapshot of all modules in the specified process. 
  hModuleSnap = CreateToolhelp32Snapshot( TH32CS_SNAPMODULE, dwPID ); 
  if( hModuleSnap == INVALID_HANDLE_VALUE ) 
  { 
    printError( TEXT("CreateToolhelp32Snapshot (of modules)") ); 
    return( FALSE ); 
  } 
 
//  Set the size of the structure before using it. 
  me32.dwSize = sizeof( MODULEENTRY32 ); 
 
//  Retrieve information about the first module, 
//  and exit if unsuccessful 
  if( !Module32First( hModuleSnap, &me32 ) ) 
  { 
    printError( TEXT("Module32First") );  // Show cause of failure 
    CloseHandle( hModuleSnap );     // Must clean up the snapshot object! 
    return( FALSE ); 
  } 
 
//  Now walk the module list of the process, 
//  and display information about each module 
  do 
  { 
    _tprintf( TEXT("\n\n     MODULE NAME:     %s"),             me32.szModule ); 
    _tprintf( TEXT("\n     executable     = %s"),             me32.szExePath ); 
    _tprintf( TEXT("\n     process ID     = 0x%08X"),         me32.th32ProcessID ); 
    _tprintf( TEXT("\n     ref count (g)  =     0x%04X"),     me32.GlblcntUsage ); 
    _tprintf( TEXT("\n     ref count (p)  =     0x%04X"),     me32.ProccntUsage ); 
    _tprintf( TEXT("\n     base address   = 0x%08X"), (DWORD) me32.modBaseAddr ); 
    _tprintf( TEXT("\n     base size      = %d"),             me32.modBaseSize ); 
 
  } while( Module32Next( hModuleSnap, &me32 ) ); 

    _tprintf( TEXT("\n"));
 
//  Do not forget to clean up the snapshot object. 
  CloseHandle( hModuleSnap ); 
  return( TRUE ); 
} 
 
 
void printError( TCHAR* msg )
{
  DWORD eNum;
  TCHAR sysMsg[256];
  TCHAR* p;

  eNum = GetLastError( );
  FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS,
         NULL, eNum,
         MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
         sysMsg, 256, NULL );

  // Trim the end of the line and terminate it with a null
  p = sysMsg;
  while( ( *p > 31 ) || ( *p == 9 ) )
    ++p;
  do { *p-- = 0; } while( ( p >= sysMsg ) &&
                          ( ( *p == '.' ) || ( *p < 33 ) ) );

  // Display the message
  _tprintf( TEXT("\n  WARNING: %s failed with error %d (%s)"), msg, eNum, sysMsg );
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Modullauf](module-walking.md)
</dt> </dl>

 

 




