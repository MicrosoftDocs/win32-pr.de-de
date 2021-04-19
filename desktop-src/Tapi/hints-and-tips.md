---
description: Im folgenden finden Sie Hinweise und Tipps, die beim Schreiben einer Anwendung für TAPI 3 zu beachten sind.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Hinweise und Tipps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363065"
---
# <a name="hints-and-tips"></a>Hinweise und Tipps

Im folgenden finden Sie Hinweise und Tipps, die beim Schreiben einer Anwendung für TAPI 3 zu beachten sind:

1.  COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) erstellt indirekt Windows. Dies ist besonders wichtig für Apartment Threading. Wenn ein Thread Windows erstellt, muss er Nachrichten verarbeiten. Wenn Ihre Threads **CoInitialize** aufzurufen, führen Sie ein nachrichtenpump aus, um Probleme zu vermeiden. Beispielsweise könnte com das Marshalling ordnungsgemäß verhindern, oder Methoden für COM-Schnittstellen, wie z. **b. iglobalinterfacetable** , hängen möglicherweise auf.

    In Apartment Threading müssen Sie über ein nachrichtenpump verfügen, unabhängig davon, ob Sie auf Synchronisierungs Objekte warten. Dies ist besonders wichtig, wenn Sie über eine Konsolenanwendung verfügen oder ein lokales com-/Remote Server Objekt schreiben, das Apartment Thread ist (wobei keine Konsole oder GUI vorhanden ist, das Steuerelement aber nur im System ausgeführt wird).

    > [!Caution]  
    > Beim Aufrufen der Warte-und Synchronisierungs Funktionen, z. b. " [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep)", " [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)", " [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)", " [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)", " [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)" usw. Verwenden Sie stattdessen [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) , und verarbeiten Sie die Nachrichten, oder verwenden Sie [**cowaitformultiplehandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), die automatisch erkennen, in welchem Apartment der Thread sich der Thread befindet (STA oder MTA) und entweder in einer für com modalen Schleife (if STA) oder in einem Block auf **WaitForMultipleObjects** (if MTA) warten. **MsgWaitForMultipleObjects** und **cowaitformultiplehandles** verarbeiten Windows-Meldungen auch gemäß den com-Regeln.

     

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

2.  **Ittapieventnotification:: Event** ist die Ereignis Funktion für apps, die in einem TAPI 3-Rückruf Thread aufgerufen wird.

    Führen Sie das minimal in der Ereignis Routine aus. Verwenden Sie stattdessen Ihren eigenen Thread, wenn möglich.

    Beachten Sie, dass das folgende Codebeispiel bereitgestellt wird. Dies ist jedoch keine Voraussetzung.

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

3.  Bearbeiten Sie keine COM-Objekte nach dem Aufruf von " [**zählinitialisieren**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)". Die Ergebnisse sind unvorhersehbar und schädlich für eine fehlerfreie Anwendung. Einige Beispiele hierfür sind Arbeitsthreads und C++-Dekonstruktoren, die möglicherweise ausgeführt werden, nachdem die Anwendung die **Initialisierung** aufruft.

 

 
