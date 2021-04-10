---
description: Das folgende Verfahren bietet eine kurze Übersicht über den Buildprozess.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Aufbauen eines ISO7816-4-APDU-Befehls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214992"
---
# <a name="building-an-iso7816-4-apdu-command"></a>Aufbauen eines ISO7816-4-APDU-Befehls

Wenn Sie einem Dienstanbieter Funktionen hinzufügen möchten, müssen Sie wissen, wie eine ISO7816-4-APDU ( [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) ) in den Basis Dienstanbieter-DLLs erstellt wird. Das folgende Verfahren bietet eine kurze Übersicht über den Buildprozess.

> [!Note]  
> Das hier enthaltene Beispiel ist nicht notwendigerweise fertiggestellt. Weitere Informationen finden Sie in den Beispielanwendungen und DLLs.

 

**So erstellen Sie einen ISO7816-4-APDU-Befehl**

1.  Erstellen Sie ein [**iscardcmd**](iscardcmd.md) -Objekt und ein [**ISCardISO7816**](iscardiso7816.md) -Objekt.

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    Die [**iscardcmd**](iscardcmd.md) -Schnittstelle enthält zwei **ibytebuffer** -Puffer. Ein Puffer enthält die tatsächliche APDU-Befehls Zeichenfolge (sowie alle Daten, die mit dem Befehl gesendet werden sollen). Der andere enthält alle Antwortinformationen, die von der Karte nach der Befehlsausführung zurückgegeben werden.

2.  Erstellen Sie mit diesen Objekten einen gültigen ISO7816-4-Befehl wie folgt:

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    Dies ist der Code, der in der [**getchallenge**](iscardiso7816-getchallenge.md) -Methode verwendet wird:

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    Die [**ISCardISO7816:: getchallenge**](iscardiso7816-getchallenge.md) -Methode verwendet die [**iscardcmd:: buildcmd**](iscardcmd-buildcmd.md) -Methode, um das angeforderte APDU zu erstellen. Hierzu werden die entsprechenden Informationen in der folgenden Anweisung in den APDU-Puffer von [**iscardcmd**](iscardcmd.md) geschrieben:

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  Führen Sie mit dem erstellten [**iscardcmd**](iscardcmd.md) -Objekt eine Transaktion mit der Karte aus, interpretieren Sie die Ergebnisse, und fahren Sie fort.

## <a name="expanding-beyond-iso7816-4"></a>Erweiterung über ISO7816-4

Die empfohlene Vorgehensweise zum Erweitern des oben beschriebenen Dienstanbieter-Build/-Ausführungsprozesses ist das Erstellen eines neuen COM-Objekts. Dieses com-Objekt sollte eine neue Schnittstelle unterstützen, die das Erstellen von nicht-ISO7816-4-Befehlen ermöglicht und die [**ISCardISO7816**](iscardiso7816.md) -Schnittstelle aggregieren sollte.

## <a name="example-of-building-an-iso7816-4-apdu-command"></a>Beispiel für das Aufbauen eines ISO7816-4-APDU-Befehls

Das folgende Beispiel zeigt den Code, der im obigen Verfahren verwendet wird.


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
