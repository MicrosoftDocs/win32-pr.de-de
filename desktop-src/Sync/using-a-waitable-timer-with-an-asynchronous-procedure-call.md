---
description: Im folgenden Beispiel wird eine APC (asynchronen Procedure Call)-Funktion, die auch als Abschluss Routine bezeichnet wird, mit einem aufnutzbaren Timer verknüpft, wenn der Timer festgelegt wird.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Verwenden von wanutzbaren Timern mit einem asynchronen Prozedur aufrutor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628288b1c5e1ce7c83e104cf6daa9e6fdcc3eb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358489"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Verwenden von wanutzbaren Timern mit einem asynchronen Prozedur aufrutor

Im folgenden Beispiel wird eine APC ( [asynchronen Procedure Call)](asynchronous-procedure-calls.md) -Funktion, die auch als Abschluss Routine bezeichnet wird, mit einem [aufnutzbaren Timer](waitable-timer-objects.md) verknüpft, wenn der Timer festgelegt wird. Die Adresse der Vervollständigungs Routine ist der vierte Parameter für die Funktion " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) ". Der fünfte Parameter ist ein void-Zeiger, den Sie verwenden können, um Argumente an die Abschluss Routine zu übergeben.

Die Abschluss Routine wird von dem Thread ausgeführt, der " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)" aufgerufen hat. Dieser Thread muss sich in einem Warn baren Zustand befinden, um die Abschluss Routine auszuführen. Dies erfolgt durch Aufrufen der Funktion " [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex) ", bei der es sich um eine mindestwarnzeit-Funktion handelt.

Jeder Thread verfügt über eine APC-Warteschlange. Wenn in der APC-Warteschlange des Threads zu dem Zeitpunkt, zu dem eine der mindestwarnzeit-Funktionen aufgerufen wird, ein Eintrag vorhanden ist, wird der Thread nicht in den Standbymodus versetzt. Stattdessen wird der Eintrag aus der APC-Warteschlange entfernt, und die Abschluss Routine wird aufgerufen.

Wenn in der APC-Warteschlange kein Eintrag vorhanden ist, wird der Thread angehalten, bis der Warte Vorgang erfüllt ist. Der Warte Vorgang kann durch Hinzufügen eines Eintrags zur APC-Warteschlange, durch ein Timeout oder durch ein zu signalisierendes handle erreicht werden. Wenn der Warte Vorgang durch einen Eintrag in der APC-Warteschlange erfüllt wird, wird der Thread aktiviert und die Abschluss Routine aufgerufen. In diesem Fall ist der Rückgabewert der Funktion der e/a- **\_ \_ Abschluss**.

Nachdem die Abschluss Routine ausgeführt wurde, sucht das System nach einem weiteren Eintrag in der APC-Warteschlange, der verarbeitet werden soll. Eine mindestwarnzeit-Funktion gibt nur dann zurück, nachdem alle APC-Einträge verarbeitet wurden. Daher ist es möglich, wenn der APC-Warteschlange Einträge schneller hinzugefügt werden, als Sie verarbeitet werden können. Dies ist insbesondere bei ausnutzbaren Timern möglich, wenn der Zeitraum kürzer ist als die Zeit, die zum Ausführen der Abschluss Routine benötigt wird.

Wenn Sie einen aufnutzbaren Timer mit einem APC verwenden, sollte der Thread, der den Timer festlegt, nicht auf das Handle des Timers warten. Auf diese Weise können Sie bewirken, dass der Thread als Ergebnis des Zeit Gebers reaktiviert wird, anstatt als Ergebnis eines Eintrags, der der APC-Warteschlange hinzugefügt wird. Daher befindet sich der Thread nicht mehr in einem Warn baren Zustand, und die Abschluss Routine wird nicht aufgerufen. Im folgenden Code wird der Thread durch den Aufrufen von [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex) ausgelöst, wenn der APC-Warteschlange des Threads ein Eintrag hinzugefügt wird, nachdem der Timer auf den signalisierten Zustand festgelegt wurde.


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

[Verwenden von wanutzbaren Timer-Objekten](using-waitable-timer-objects.md)
</dt> </dl>

 

 
