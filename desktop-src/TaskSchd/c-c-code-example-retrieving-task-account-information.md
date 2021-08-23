---
title: C/C++-Codebeispiel zum Abrufen von Taskkontoinformationen
description: In diesem Codebeispiel werden die Kontoinformationen einer bekannten Aufgabe abgerufen und der Kontoname auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind und dass die Taskplaner ausgeführt wird.
ms.assetid: ef330276-a063-42c6-a837-fddb4723091b
keywords:
- Abrufen von Taskkontoinformationen Taskplaner
- Abrufen von Arbeitselementeigenschaften Taskplaner , Kontoinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce068589ee1284f4c0b655994c9ea13b6fd63affca8146330e93aef12157cb2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738860"
---
# <a name="cc-code-example-retrieving-task-account-information"></a>C/C++-Codebeispiel: Abrufen von Taskkontoinformationen

In diesem Codebeispiel werden die Kontoinformationen einer bekannten Aufgabe abgerufen und der Kontoname auf dem Bildschirm angezeigt. In diesem Beispiel wird davon ausgegangen, dass die Aufgabe und die Testaufgabe bereits auf dem lokalen Computer vorhanden sind und dass die Taskplaner ausgeführt wird.


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
  
  //Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetAccountInformation. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR pwszAccountName;
  
  hr = pITask->GetAccountInformation(&pwszAccountName);
  
  // Release the ITask interface.
  pITask->Release();

  if(hr == SCHED_E_NO_SECURITY_SERVICES)
  {
    wprintf(L"Error: SCHED_E_NO_SECURITY_SERVICES");
    wprintf(L"Security services are available only on Windows Server 2003");
    wprintf(L", Windows XP, and Windows 2000.");
    CoUninitialize();
    return 1;

  }
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetAccountInformation: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The account name for Test Task is: ");
  wprintf(L"  %s\n",pwszAccountName);
  
  CoTaskMemFree(pwszAccountName);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




