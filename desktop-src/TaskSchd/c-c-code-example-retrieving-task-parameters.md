---
title: C/C++-Code Beispiel Abrufen von Aufgaben Parametern
description: Dieses Beispiel ruft die Parameter Zeichenfolge ab, die ausgeführt wird, wenn die Aufgabe ausgeführt wird, und zeigt diese Zeichenfolge auf dem Bildschirm an. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: fefa668e-803f-4e05-8097-b75231ee8f72
keywords:
- Abrufen von Aufgaben Parametern Taskplaner
- Abrufen von Task Eigenschaften Taskplaner, Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6adff7baeb4d4151c06ab192e336712716fb9d80
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388319"
---
# <a name="cc-code-example-retrieving-task-parameters"></a><span data-ttu-id="44a61-106">C/C++-Code Beispiel: Abrufen von Aufgaben Parametern</span><span class="sxs-lookup"><span data-stu-id="44a61-106">C/C++ Code Example: Retrieving Task Parameters</span></span>

<span data-ttu-id="44a61-107">Dieses Beispiel ruft die Parameter Zeichenfolge ab, die ausgeführt wird, wenn die Aufgabe ausgeführt wird, und zeigt diese Zeichenfolge auf dem Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="44a61-107">This example retrieves the parameter string that is executed when the task is run and displays that string on the screen.</span></span> <span data-ttu-id="44a61-108">In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="44a61-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetParameters to display the parameters string 
  // associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszParameters;
  hr = pITask->GetParameters(&lpwszParameters);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetApplicationName\n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process returned parameter string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with the following parameters:\n");
  wprintf(L"  %s\n", lpwszParameters);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszParameters);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="44a61-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44a61-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44a61-110">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="44a61-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




