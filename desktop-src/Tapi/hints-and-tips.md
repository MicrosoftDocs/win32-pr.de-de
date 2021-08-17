---
description: Im Folgenden sind Hinweise und Tipps, die Beim Schreiben einer Anwendung für TAPI 3 berücksichtigt werden sollten.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Hinweise und Tipps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d51e8c7e3f8c6e4a9e38b27fa5cfe4c10e45d37cfa67af095d573eea319614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762933"
---
# <a name="hints-and-tips"></a>Hinweise und Tipps

Im Folgenden sind Hinweise und Tipps zu beachten, wenn Sie eine Anwendung für TAPI 3 schreiben:

1.  COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) erstellt indirekt Fenster; dies ist besonders wichtig für Apartmentthreading. Wenn ein Thread Fenster erstellt, muss er Nachrichten verarbeiten. Wenn Ihre Threads **CoInitialize** aufrufen, führen Sie eine Nachrichtenpump aus, um Probleme zu vermeiden. Beispielsweise kann COM das Marshalling ordnungsgemäß beenden, oder Methoden in COM-Schnittstellen, z. **B. IGlobalInterfaceTable,** können hängen bleiben.

    Beim Apartmentthreading muss eine Nachrichtenpumpe vorhanden sein, unabhängig davon, ob Sie auf Synchronisierungsobjekte warten. Dies ist besonders wichtig, wenn Sie über eine Konsolenanwendung verfügen oder ein lokales COM-/Remoteserverobjekt schreiben, das im Apartmentthread ausgeführt wird (wenn Sie keine Konsole oder GUI haben, das Steuerelement jedoch nur im System ausgeführt wird).

    > [!Caution]  
    > Beim Aufrufen der Warte- und Synchronisierungsfunktionen wie [**Sleep,**](/windows/desktop/api/synchapi/nf-synchapi-sleep) [**WaitForMultipleObjects,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) [**WaitForMultipleObjectsEx,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex) [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)usw. Verwenden Sie stattdessen [**MsgWaitForMultipleObjects,**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) und verarbeiten Sie die Nachrichten, oder verwenden Sie [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), das automatisch erkennt, in welchem Apartmenttyp sich der Thread befindet (STA oder MTA) und entweder in einer modalen COM-Schleife (bei STA) oder auf **WaitForMultipleObjects** (bei MTA) wartet. **MsgWaitForMultipleObjects** und **CoWaitForMultipleHandles** verarbeiten auch Windows-Nachrichten gemäß den COM-Regeln.

     

    Verwenden Sie anstelle von

    `Sleep (5000);`

    Verwendung:

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  **ITTAPIEventNotification::Event** ist die Ereignisfunktion der Apps, die in einem TAPI 3-Rückrufthread aufgerufen wird.

    Gehen Sie in der Ereignisroutine so gering wie nötig vor. Verwenden Sie stattdessen nach Möglichkeit Ihren eigenen Thread.

    Beachten Sie, dass das folgende Codebeispiel bereitgestellt wird, aber keine Anforderung ist.

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  Bearbeiten Sie COM-Objekte nicht, nachdem [**Sie CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)aufgerufen haben. Die Ergebnisse sind unvorhersehbar und schädlich für eine fehlerfreie Anwendung. Beispiele dafür sind Arbeitsthreads und C++-Destruktoren, die ausgeführt werden können, nachdem eine Anwendung **CoUninitialize aufruft.**

 

 
