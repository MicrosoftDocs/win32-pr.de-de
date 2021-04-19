---
title: C/C++-Code Beispiel Abrufen der Aufgaben Priorität
description: Dieses Beispiel ruft die Prioritäts Ebene einer Aufgabe ab und zeigt den Pfad zum Arbeitsverzeichnis auf dem Bildschirm an. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: 6e7eccce-406a-4827-8fe2-abe93251668a
keywords:
- Abrufen der Aufgaben Prioritäts Taskplaner
- Abrufen von Task Eigenschaften Taskplaner, Priorität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9b32b5b4a6e66539ce1a65ab41488f96418d29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338586"
---
# <a name="cc-code-example-retrieving-task-priority"></a><span data-ttu-id="aae89-106">C/C++-Code Beispiel: Abrufen der Aufgaben Priorität</span><span class="sxs-lookup"><span data-stu-id="aae89-106">C/C++ Code Example: Retrieving Task Priority</span></span>

<span data-ttu-id="aae89-107">Dieses Beispiel ruft die Prioritäts Ebene einer Aufgabe ab und zeigt den Pfad zum Arbeitsverzeichnis auf dem Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="aae89-107">This example retrieves the priority level of a task and displays the path to the working directory on the screen.</span></span> <span data-ttu-id="aae89-108">In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="aae89-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate: error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetPriority to retrieve the priority level 
  // of Test Task.
  ///////////////////////////////////////////////////////////////////
  
  DWORD pdwPriority;
  hr = pITask->GetPriority(&pdwPriority);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetPriority: error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  if(pdwPriority == HIGH_PRIORITY_CLASS)
  {
     wprintf(L"Test Task is a high priority task.\n");
  }
  else
  {
     wprintf(L"Test Task is not a high priority task.\n");
  }
  
  CoUninitialize();
  return 0;
  
}
```



## <a name="related-topics"></a><span data-ttu-id="aae89-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aae89-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae89-110">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="aae89-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




