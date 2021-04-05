---
title: C/C++-Code Beispiel Abrufen des Task Status
description: In diesem Beispiel wird der aktuelle Status der Aufgabe abgerufen und auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: 7ad40ac7-2363-481a-87fa-18dcf2d749b3
keywords:
- Abrufen von Task Status Taskplaner
- Abrufen von Arbeits Element Eigenschaften Taskplaner, Task Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068e2be84750ac8fead97eac146400139dee85fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947683"
---
# <a name="cc-code-example-retrieving-task-status"></a>C/C++-Code Beispiel: Abrufen des Task Status

In diesem Beispiel wird der aktuelle Status der Aufgabe abgerufen und auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

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
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
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
  // Call ITask::GetStatus. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HRESULT phrStatus;
  
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetStatus: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The status of Test Task is: ");
  
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;
  case SCHED_S_TASK_DISABLED:
       wprintf(L"  SCHED_S_TASK_DISABLED\n");
       break;
  case SCHED_S_TASK_HAS_NOT_RUN:
       wprintf(L"  SCHED_S_TASK_HAS_NOT_RUN\n");
       break;
  case SCHED_S_TASK_NOT_SCHEDULED:
       wprintf(L"  SCHED_S_TASK_NOT_SCHEDULED\n");
       break;
  case SCHED_S_TASK_NO_MORE_RUNS:
       wprintf(L"  SCHED_S_TASK_NO_MORE_RUNS\n");
       break;
  case SCHED_S_TASK_NO_VALID_TRIGGERS:
       wprintf(L"  SCHED_S_TASK_NO_VALID_TRIGGERS\n");
       break;
  default:
       wprintf(L"  unknown status flag!\n"); 
  }
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




