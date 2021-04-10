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
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="ced72-103">Aufbauen eines ISO7816-4-APDU-Befehls</span><span class="sxs-lookup"><span data-stu-id="ced72-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="ced72-104">Wenn Sie einem Dienstanbieter Funktionen hinzufügen möchten, müssen Sie wissen, wie eine ISO7816-4-APDU ( [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) ) in den Basis Dienstanbieter-DLLs erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ced72-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="ced72-105">Das folgende Verfahren bietet eine kurze Übersicht über den Buildprozess.</span><span class="sxs-lookup"><span data-stu-id="ced72-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="ced72-106">Das hier enthaltene Beispiel ist nicht notwendigerweise fertiggestellt. Weitere Informationen finden Sie in den Beispielanwendungen und DLLs.</span><span class="sxs-lookup"><span data-stu-id="ced72-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="ced72-107">**So erstellen Sie einen ISO7816-4-APDU-Befehl**</span><span class="sxs-lookup"><span data-stu-id="ced72-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="ced72-108">Erstellen Sie ein [**iscardcmd**](iscardcmd.md) -Objekt und ein [**ISCardISO7816**](iscardiso7816.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ced72-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

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

    

    <span data-ttu-id="ced72-109">Die [**iscardcmd**](iscardcmd.md) -Schnittstelle enthält zwei **ibytebuffer** -Puffer.</span><span class="sxs-lookup"><span data-stu-id="ced72-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="ced72-110">Ein Puffer enthält die tatsächliche APDU-Befehls Zeichenfolge (sowie alle Daten, die mit dem Befehl gesendet werden sollen).</span><span class="sxs-lookup"><span data-stu-id="ced72-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="ced72-111">Der andere enthält alle Antwortinformationen, die von der Karte nach der Befehlsausführung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ced72-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="ced72-112">Erstellen Sie mit diesen Objekten einen gültigen ISO7816-4-Befehl wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ced72-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="ced72-113">Dies ist der Code, der in der [**getchallenge**](iscardiso7816-getchallenge.md) -Methode verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="ced72-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

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

    

    <span data-ttu-id="ced72-114">Die [**ISCardISO7816:: getchallenge**](iscardiso7816-getchallenge.md) -Methode verwendet die [**iscardcmd:: buildcmd**](iscardcmd-buildcmd.md) -Methode, um das angeforderte APDU zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ced72-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="ced72-115">Hierzu werden die entsprechenden Informationen in der folgenden Anweisung in den APDU-Puffer von [**iscardcmd**](iscardcmd.md) geschrieben:</span><span class="sxs-lookup"><span data-stu-id="ced72-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="ced72-116">Führen Sie mit dem erstellten [**iscardcmd**](iscardcmd.md) -Objekt eine Transaktion mit der Karte aus, interpretieren Sie die Ergebnisse, und fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="ced72-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="ced72-117">Erweiterung über ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="ced72-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="ced72-118">Die empfohlene Vorgehensweise zum Erweitern des oben beschriebenen Dienstanbieter-Build/-Ausführungsprozesses ist das Erstellen eines neuen COM-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ced72-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="ced72-119">Dieses com-Objekt sollte eine neue Schnittstelle unterstützen, die das Erstellen von nicht-ISO7816-4-Befehlen ermöglicht und die [**ISCardISO7816**](iscardiso7816.md) -Schnittstelle aggregieren sollte.</span><span class="sxs-lookup"><span data-stu-id="ced72-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="ced72-120">Beispiel für das Aufbauen eines ISO7816-4-APDU-Befehls</span><span class="sxs-lookup"><span data-stu-id="ced72-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="ced72-121">Das folgende Beispiel zeigt den Code, der im obigen Verfahren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ced72-121">The following example shows the code used in the procedure above.</span></span>


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



 

 
