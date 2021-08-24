---
title: C/C++-Codebeispiel zum Abrufen der Aufgabe NextRun Time
description: In diesem Beispiel wird das nächste Mal abgerufen, wenn die Ausführung der Aufgabe geplant ist, und diese Uhrzeit auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: 2134a188-2fd4-4b55-bd9e-3363772080c0
keywords:
- Abrufen der nächsten Laufzeit der Aufgabe Taskplaner
- Abrufen von Arbeitselementeigenschaften Taskplaner , nächste Ausführungszeit der Aufgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0472f867aea83457bbb4cb77a5a092b8c302f793b0df052e4addb0422adedb5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738500"
---
# <a name="cc-code-example-retrieving-the-task-nextrun-time"></a>C/C++-Codebeispiel: Abrufen der Aufgabe NextRun Time

In diesem Beispiel wird das nächste Mal abgerufen, wenn die Ausführung der Aufgabe geplant ist, und diese Uhrzeit auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1.0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




