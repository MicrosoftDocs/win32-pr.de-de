---
title: C/C++-Code Beispiel festlegen des Arbeitsverzeichnisses
description: In diesem Beispiel wird das Arbeitsverzeichnis einer bekannten Aufgabe festgelegt. In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: bcfcd6af-a3aa-45a8-bde6-0c90aec3e27a
keywords:
- Festlegen von Aufgaben Eigenschaften Taskplaner, Arbeitsverzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc60a7af33889d6442d4f95cf2121e77275fd57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709167"
---
# <a name="cc-code-example-setting-working-directory"></a><span data-ttu-id="7d08b-105">C/C++-Code Beispiel: Festlegen des Arbeitsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="7d08b-105">C/C++ Code Example: Setting Working Directory</span></span>

<span data-ttu-id="7d08b-106">In diesem Beispiel wird das Arbeitsverzeichnis einer bekannten Aufgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7d08b-106">This example sets the working directory of a known task.</span></span> <span data-ttu-id="7d08b-107">In diesem Beispiel wird davon ausgegangen, dass der Task und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7d08b-107">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::SetWorkingDirectory to specify the current 
  // working directory for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszWorkingDirectory = L"C:\\Temp";
  
  hr = pITask->SetWorkingDirectory(pwszWorkingDirectory);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetWorkingDirectory: ");
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
  
  wprintf(L"Set the working directory to C:\\Temp.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="7d08b-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d08b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d08b-109">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d08b-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




