---
title: C/C++-Code Beispiel Festlegen von Aufgaben Parametern
description: In diesem Beispiel werden alle Befehlszeilenparameter gelöscht, die einer bekannten Aufgabe zugeordnet sind. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: cd71379a-7eb2-4966-a28b-5b7d31d60c16
keywords:
- Festlegen von Task Eigenschaften Taskplaner, Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509776aa87d414cb1cb4c590c2be2c0ea3912269
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709347"
---
# <a name="cc-code-example-setting-task-parameters"></a><span data-ttu-id="6db22-105">C/C++-Code Beispiel: Festlegen von Aufgaben Parametern</span><span class="sxs-lookup"><span data-stu-id="6db22-105">C/C++ Code Example: Setting Task Parameters</span></span>

<span data-ttu-id="6db22-106">In diesem Beispiel werden alle Befehlszeilenparameter gelöscht, die einer bekannten Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6db22-106">This example clears all command-line parameters associated with a known task.</span></span> <span data-ttu-id="6db22-107">In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6db22-107">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  
  // Release the ITaskScheduler interface.
  pITS->Release();  
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::SetParameters to L"" to clear the parameters for
  // Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszParameters = L"";
  
  hr = pITask->SetParameters(pwszParameters);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetParameters: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }

  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"Cleared the parameters of TestTask.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="6db22-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6db22-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db22-109">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="6db22-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




