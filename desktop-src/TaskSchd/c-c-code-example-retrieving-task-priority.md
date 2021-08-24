---
title: C/C++-Codebeispiel zum Abrufen der Aufgabenpriorität
description: In diesem Beispiel wird die Prioritätsstufe einer Aufgabe abgerufen und der Pfad zum Arbeitsverzeichnis auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: 6e7eccce-406a-4827-8fe2-abe93251668a
keywords:
- Abrufen der Aufgabenpriorität Taskplaner
- Abrufen von Taskeigenschaften Taskplaner , Priorität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b9a746f956131954b7e048b416f6e1c348aff8893417d0bd872f6750c43ce7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738660"
---
# <a name="cc-code-example-retrieving-task-priority"></a>C/C++-Codebeispiel: Abrufen der Aufgabenpriorität

In diesem Beispiel wird die Prioritätsstufe einer Aufgabe abgerufen und der Pfad zum Arbeitsverzeichnis auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




