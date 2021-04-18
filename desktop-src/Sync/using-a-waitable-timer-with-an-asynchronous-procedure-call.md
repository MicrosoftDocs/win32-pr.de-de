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
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a><span data-ttu-id="317b7-103">Verwenden von wanutzbaren Timern mit einem asynchronen Prozedur aufrutor</span><span class="sxs-lookup"><span data-stu-id="317b7-103">Using Waitable Timers with an Asynchronous Procedure Call</span></span>

<span data-ttu-id="317b7-104">Im folgenden Beispiel wird eine APC ( [asynchronen Procedure Call)](asynchronous-procedure-calls.md) -Funktion, die auch als Abschluss Routine bezeichnet wird, mit einem [aufnutzbaren Timer](waitable-timer-objects.md) verknüpft, wenn der Timer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="317b7-104">The following example associates an [asynchronous procedure call](asynchronous-procedure-calls.md) (APC) function, also known as a completion routine, with a [waitable timer](waitable-timer-objects.md) when the timer is set.</span></span> <span data-ttu-id="317b7-105">Die Adresse der Vervollständigungs Routine ist der vierte Parameter für die Funktion " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) ".</span><span class="sxs-lookup"><span data-stu-id="317b7-105">The address of the completion routine is the fourth parameter to the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function.</span></span> <span data-ttu-id="317b7-106">Der fünfte Parameter ist ein void-Zeiger, den Sie verwenden können, um Argumente an die Abschluss Routine zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="317b7-106">The fifth parameter is a void pointer that you can use to pass arguments to the completion routine.</span></span>

<span data-ttu-id="317b7-107">Die Abschluss Routine wird von dem Thread ausgeführt, der " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)" aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="317b7-107">The completion routine will be executed by the same thread that called [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span></span> <span data-ttu-id="317b7-108">Dieser Thread muss sich in einem Warn baren Zustand befinden, um die Abschluss Routine auszuführen.</span><span class="sxs-lookup"><span data-stu-id="317b7-108">This thread must be in an alertable state to execute the completion routine.</span></span> <span data-ttu-id="317b7-109">Dies erfolgt durch Aufrufen der Funktion " [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex) ", bei der es sich um eine mindestwarnzeit-Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="317b7-109">It accomplishes this by calling the [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) function, which is an alertable function.</span></span>

<span data-ttu-id="317b7-110">Jeder Thread verfügt über eine APC-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="317b7-110">Each thread has an APC queue.</span></span> <span data-ttu-id="317b7-111">Wenn in der APC-Warteschlange des Threads zu dem Zeitpunkt, zu dem eine der mindestwarnzeit-Funktionen aufgerufen wird, ein Eintrag vorhanden ist, wird der Thread nicht in den Standbymodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="317b7-111">If there is an entry in the thread's APC queue at the time that one of the alertable functions is called, the thread is not put to sleep.</span></span> <span data-ttu-id="317b7-112">Stattdessen wird der Eintrag aus der APC-Warteschlange entfernt, und die Abschluss Routine wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="317b7-112">Instead, the entry is removed from the APC queue and the completion routine is called.</span></span>

<span data-ttu-id="317b7-113">Wenn in der APC-Warteschlange kein Eintrag vorhanden ist, wird der Thread angehalten, bis der Warte Vorgang erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="317b7-113">If no entry exists in the APC queue, the thread is suspended until the wait is satisfied.</span></span> <span data-ttu-id="317b7-114">Der Warte Vorgang kann durch Hinzufügen eines Eintrags zur APC-Warteschlange, durch ein Timeout oder durch ein zu signalisierendes handle erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="317b7-114">The wait can be satisfied by adding an entry to the APC queue, by a timeout, or by a handle becoming signaled.</span></span> <span data-ttu-id="317b7-115">Wenn der Warte Vorgang durch einen Eintrag in der APC-Warteschlange erfüllt wird, wird der Thread aktiviert und die Abschluss Routine aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="317b7-115">If the wait is satisfied by an entry in the APC queue, the thread is awakened and the completion routine is called.</span></span> <span data-ttu-id="317b7-116">In diesem Fall ist der Rückgabewert der Funktion der e/a- **\_ \_ Abschluss**.</span><span class="sxs-lookup"><span data-stu-id="317b7-116">In this case, the return value of the function is **WAIT\_IO\_COMPLETION**.</span></span>

<span data-ttu-id="317b7-117">Nachdem die Abschluss Routine ausgeführt wurde, sucht das System nach einem weiteren Eintrag in der APC-Warteschlange, der verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="317b7-117">After the completion routine is executed, the system checks for another entry in the APC queue to process.</span></span> <span data-ttu-id="317b7-118">Eine mindestwarnzeit-Funktion gibt nur dann zurück, nachdem alle APC-Einträge verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="317b7-118">An alertable function will return only after all APC entries have been processed.</span></span> <span data-ttu-id="317b7-119">Daher ist es möglich, wenn der APC-Warteschlange Einträge schneller hinzugefügt werden, als Sie verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="317b7-119">Therefore, if entries are being added to the APC queue faster than they can be processed, it is possible that a call to an alertable function will never return.</span></span> <span data-ttu-id="317b7-120">Dies ist insbesondere bei ausnutzbaren Timern möglich, wenn der Zeitraum kürzer ist als die Zeit, die zum Ausführen der Abschluss Routine benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="317b7-120">This is especially possible with waitable timers, if the period is shorter than the amount of time required to execute the completion routine.</span></span>

<span data-ttu-id="317b7-121">Wenn Sie einen aufnutzbaren Timer mit einem APC verwenden, sollte der Thread, der den Timer festlegt, nicht auf das Handle des Timers warten.</span><span class="sxs-lookup"><span data-stu-id="317b7-121">When you are using a waitable timer with an APC, the thread that sets the timer should not wait on the handle of the timer.</span></span> <span data-ttu-id="317b7-122">Auf diese Weise können Sie bewirken, dass der Thread als Ergebnis des Zeit Gebers reaktiviert wird, anstatt als Ergebnis eines Eintrags, der der APC-Warteschlange hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="317b7-122">By doing so, you would cause the thread to wake up as a result of the timer becoming signaled rather than as the result of an entry being added to the APC queue.</span></span> <span data-ttu-id="317b7-123">Daher befindet sich der Thread nicht mehr in einem Warn baren Zustand, und die Abschluss Routine wird nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="317b7-123">As a result, the thread is no longer in an alertable state and the completion routine is not called.</span></span> <span data-ttu-id="317b7-124">Im folgenden Code wird der Thread durch den Aufrufen von [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex) ausgelöst, wenn der APC-Warteschlange des Threads ein Eintrag hinzugefügt wird, nachdem der Timer auf den signalisierten Zustand festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="317b7-124">In the following code, the call to [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) awakens the thread when an entry is added to the thread's APC queue after the timer is set to the signaled state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="317b7-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="317b7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="317b7-126">Verwenden von wanutzbaren Timer-Objekten</span><span class="sxs-lookup"><span data-stu-id="317b7-126">Using Waitable Timer Objects</span></span>](using-waitable-timer-objects.md)
</dt> </dl>

 

 
