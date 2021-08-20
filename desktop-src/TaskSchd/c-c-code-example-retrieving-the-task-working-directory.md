---
title: C/C++-Codebeispiel zum Abrufen des Aufgabenarbeitsverzeichnisses
description: In diesem Beispiel wird das Arbeitsverzeichnis abgerufen, das einer Aufgabe zugeordnet ist, und der Pfad zum Arbeitsverzeichnis wird auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: 46dfd996-6d5f-4a77-87a9-daf1909e1509
keywords:
- Abrufen von Arbeitsverzeichnis-Taskplaner
- Abrufen von Taskeigenschaften Taskplaner , Arbeitsverzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73858e7994bc4cfe91676131b9f0770d306390b6ae3d0f2cb9c5b36ee134d4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943902"
---
# <a name="cc-code-example-retrieving-the-task-working-directory"></a>C/C++-Codebeispiel: Abrufen des Aufgabenarbeitsverzeichnisses

In diesem Beispiel wird das Arbeitsverzeichnis abgerufen, das einer Aufgabe zugeordnet ist, und der Pfad zum Arbeitsverzeichnis wird auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.


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
  // Call ITask::GetWorkingDirectory to display the working 
  // directory associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszWorkDir;
  hr = pITask->GetWorkingDirectory(&lpwszWorkDir);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetWorkingDirectory: \n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process returned string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with : %s\n", lpwszWorkDir);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszWorkDir);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




