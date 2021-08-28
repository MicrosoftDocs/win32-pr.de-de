---
description: Im folgenden Beispiel wird eine APC-Funktion (Asynchronous Procedure Call, asynchroner Prozeduraufruf), die auch als Vervollständigungsroutine bezeichnet wird, einem wartebaren Timer zu, wenn der Timer festgelegt ist.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Verwenden von wartebaren Timern mit einem asynchronen Prozeduraufruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62436011a3da0ac17525a0ce977e7bcd25382c5c267b62b9c972381e0f28562d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661150"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Verwenden von wartebaren Timern mit einem asynchronen Prozeduraufruf

Im folgenden Beispiel wird eine APC-Funktion [(Asynchronous Procedure Call,](asynchronous-procedure-calls.md) asynchroner Prozeduraufruf), die auch als Vervollständigungsroutine bezeichnet wird, einem wartebaren [Timer](waitable-timer-objects.md) zu, wenn der Timer festgelegt ist. Die Adresse der Vervollständigungsroutine ist der vierte Parameter der [**SetWaitableTimer-Funktion.**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) Der fünfte Parameter ist ein void-Zeiger, mit dem Sie Argumente an die Vervollständigungsroutine übergeben können.

Die Vervollständigungsroutine wird von demselben Thread ausgeführt, der [**SetWaitableTimer aufgerufen hat.**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) Dieser Thread muss sich in einem warnbaren Zustand befindet, um die Abschlussroutine auszuführen. Dies erreichen Sie durch Aufrufen der [**SleepEx-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-sleepex) bei der es sich um eine warnbare Funktion handelt.

Jeder Thread verfügt über eine APC-Warteschlange. Wenn zum Zeitpunkt des Aufrufens einer der warnbaren Funktionen ein Eintrag in der APC-Warteschlange des Threads angezeigt wird, wird der Thread nicht in den Ruhezustand versetzt. Stattdessen wird der Eintrag aus der APC-Warteschlange entfernt und die Abschlussroutine aufgerufen.

Wenn kein Eintrag in der APC-Warteschlange vorhanden ist, wird der Thread angehalten, bis die Wartezeit erfüllt ist. Die Wartezeit kann durch Hinzufügen eines Eintrags zur APC-Warteschlange, durch ein Timeout oder durch ein Handle, das signalisiert wird, erfüllt werden. Wenn der Wartezustand durch einen Eintrag in der APC-Warteschlange erfüllt wird, wird der Thread erweckt, und die Abschlussroutine wird aufgerufen. In diesem Fall ist der Rückgabewert der Funktion **WAIT \_ IO \_ COMPLETION**.

Nachdem die Abschlussroutine ausgeführt wurde, überprüft das System, ob ein anderer Eintrag in der APC-Warteschlange zur Verarbeitung verwendet wird. Eine warnungsfähige Funktion gibt erst zurück, nachdem alle APC-Einträge verarbeitet wurden. Wenn Einträge daher schneller zur APC-Warteschlange hinzugefügt werden, als sie verarbeitet werden können, ist es möglich, dass ein Aufruf einer warnbaren Funktion niemals zurücksetzbar ist. Dies ist insbesondere bei wartebaren Timern möglich, wenn der Zeitraum kürzer als der Zeitraum ist, der zum Ausführen der Abschlussroutine erforderlich ist.

Wenn Sie einen wartebaren Timer mit einem APC verwenden, sollte der Thread, der den Timer fest legt, nicht auf das Handle des Timers warten. Dadurch würden Sie bewirken, dass der Thread reaktiviert wird, wenn der Timer signalisiert wird und nicht als Ergebnis eines Eintrags, der der APC-Warteschlange hinzugefügt wird. Daher befindet sich der Thread nicht mehr in einem warnbaren Zustand, und die Abschlussroutine wird nicht aufgerufen. Im folgenden Code weckt der Aufruf von [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) den Thread, wenn der APC-Warteschlange des Threads ein Eintrag hinzugefügt wird, nachdem der Timer auf den signalisierten Zustand festgelegt wurde.


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von wartebaren Timerobjekten](using-waitable-timer-objects.md)
</dt> </dl>

 

 
