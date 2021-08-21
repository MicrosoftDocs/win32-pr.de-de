---
title: C/C++-Codebeispiel zum Abrufen von Taskparametern
description: In diesem Beispiel wird die Parameterzeichenfolge abgerufen, die ausgeführt wird, wenn der Task ausgeführt wird, und diese Zeichenfolge wird auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.
ms.assetid: fefa668e-803f-4e05-8097-b75231ee8f72
keywords:
- Abrufen von Taskparametern Taskplaner
- Abrufen von Taskeigenschaften Taskplaner Parametern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e18df24eee8f2de6d7a796aeb11febad8d9e79e95be6dd47bcd9be0a5392078d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738750"
---
# <a name="cc-code-example-retrieving-task-parameters"></a>C/C++-Codebeispiel: Abrufen von Taskparametern

In diesem Beispiel wird die Parameterzeichenfolge abgerufen, die ausgeführt wird, wenn der Task ausgeführt wird, und diese Zeichenfolge wird auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




