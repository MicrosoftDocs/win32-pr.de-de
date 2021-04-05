---
title: C/C++-Code Beispiel Abrufen von auslöserzeichenfolgen
description: In diesem Beispiel wird eine triggerzeichenfolge für alle Trigger abgerufen, die mit einer bekannten Aufgabe verknüpft sind.
ms.assetid: cd605c68-efaa-4ce7-9e44-59f516d85627
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b99f986692c3bfb1297a98e9afdcea65606446
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711730"
---
# <a name="cc-code-example-retrieving-trigger-strings"></a><span data-ttu-id="e01f4-103">C/C++-Code Beispiel: Abrufen von auslöserzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="e01f4-103">C/C++ Code Example: Retrieving Trigger Strings</span></span>

<span data-ttu-id="e01f4-104">In diesem Beispiel wird eine triggerzeichenfolge für alle Trigger abgerufen, die mit einer bekannten Aufgabe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e01f4-104">This example retrieves a trigger string for all the triggers associated with a known task.</span></span>


```C++
#include <windows.h>
#include <winbase.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
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
  LPCWSTR lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  pITS->Release();
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::TriggerCount to retrieve the number of triggers
  // associated with the task.
  ///////////////////////////////////////////////////////////////////
  
  WORD plTriggerCount;
  hr = pITask->GetTriggerCount (&plTriggerCount);
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetTriggerCount: ");
    wprintf(L"error = 0x%x\n",hr);
    pTask->Release();
    CoUninitialize();
    return 1;
  } 
  
  
  ///////////////////////////////////////////////////////////////////
  // Display the trigger stings, calling ITask::GetTriggerString for 
  // each trigger associated with the task.
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"There are %i triggers with Test Task.\n",plTriggerCount);
  wprintf(L"They are:\n");  
   
  WORD CurrentTrigger=0;
  LPWSTR ppwszTrigger;
  
  for (CurrentTrigger=0; CurrentTrigger<plTriggerCount; CurrentTrigger++)
  {  
    pITask->GetTriggerString (CurrentTrigger,
                              &ppwszTrigger); 
    if (FAILED(hr))
    {
      wprintf(L"Failed calling ITask::GetTriggerString: ");
      wprintf(L"error = 0x%x\n",hr);
      pTask->Release();
      CoUninitialize();
      return 1;
    }
    
    wprintf(L"%i) %s\n",CurrentTrigger+1, ppwszTrigger);
  } 
  
  
  ///////////////////////////////////////////////////////////////////
  // Release resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(ppwszTrigger);
  pITask->Release();
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="e01f4-105">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e01f4-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e01f4-106">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e01f4-106">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




