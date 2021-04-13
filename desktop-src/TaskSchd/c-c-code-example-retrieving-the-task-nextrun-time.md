---
title: C/C++-Code Beispiel Abrufen der Task-nextrun-Zeit
description: Dieses Beispiel ruft den Zeitpunkt ab, zu dem die Ausführung der Aufgabe geplant ist, und zeigt diese Uhrzeit auf dem Bildschirm an. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: 2134a188-2fd4-4b55-bd9e-3363772080c0
keywords:
- Abrufen der nächsten Aufgabe Taskplaner
- Abrufen von Arbeits Element Eigenschaften Taskplaner, Aufgabe Nächste Ausführungszeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57341db57debb0270668c1236e5b353c7f703a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388411"
---
# <a name="cc-code-example-retrieving-the-task-nextrun-time"></a><span data-ttu-id="d927c-106">C/C++-Code Beispiel: Abrufen der Task-nextrun-Zeit</span><span class="sxs-lookup"><span data-stu-id="d927c-106">C/C++ Code Example: Retrieving the Task NextRun Time</span></span>

<span data-ttu-id="d927c-107">Dieses Beispiel ruft den Zeitpunkt ab, zu dem die Ausführung der Aufgabe geplant ist, und zeigt diese Uhrzeit auf dem Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="d927c-107">This example retrieves the next time the task is scheduled to run and displays that time on the screen.</span></span> <span data-ttu-id="d927c-108">In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d927c-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <wchar.h>
#include <stdio.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      CoUninitialize();
      return 1;
    }
  }
  else
  {
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  // Release ITaskScheduler interface.
  pITS->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetNextRunTime and display next run time of 
  // this task.
  ///////////////////////////////////////////////////////////////////

  SYSTEMTIME pstNextRun;
    
  hr = pITask->GetNextRunTime(&pstNextRun);
  
  // Release the ITask interface.
  pITask->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetNextRunTime: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }

  wprintf(L"The next runtime for this task is: \n");
  wprintf(L"  %u/%u/%u \t %u:%02u\n", pstNextRun.wMonth,
                                      pstNextRun.wDay,
                                      pstNextRun.wYear,
                                      pstNextRun.wHour,
                                      pstNextRun.wMinute);
 

  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d927c-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d927c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d927c-110">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d927c-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




