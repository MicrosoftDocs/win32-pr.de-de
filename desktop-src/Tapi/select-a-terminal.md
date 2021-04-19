---
description: Im folgenden Codebeispiel wird veranschaulicht, wie Terminals in Streams ausgewählt werden, die mit einem-Befehl verknüpft sind.
ms.assetid: ff43e81c-ff39-466d-870a-54b75c2938a4
title: Terminal auswählen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d195e021f5937c733f3d7a0efce0cfee5eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363814"
---
# <a name="select-a-terminal"></a><span data-ttu-id="82397-103">Terminal auswählen</span><span class="sxs-lookup"><span data-stu-id="82397-103">Select a Terminal</span></span>

<span data-ttu-id="82397-104">Im folgenden Codebeispiel wird veranschaulicht, wie Terminals in Streams ausgewählt werden, die mit einem-Befehl verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="82397-104">The following code example demonstrates how to select terminals onto streams associated with a call.</span></span>

<span data-ttu-id="82397-105">Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md) ausführen und [eine Adresse auswählen](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="82397-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="82397-106">Außerdem erfordert dieses Beispiel, dass die Anwendung bereits über einen Zeiger auf die [**itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) -Schnittstelle eines eingehenden oder ausgehenden Aufrufes verfügt.</span><span class="sxs-lookup"><span data-stu-id="82397-106">Also, this example requires that the application already have a pointer to the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) interface of either an incoming or outgoing call.</span></span> <span data-ttu-id="82397-107">Weitere Informationen zum Abrufen dieses Zeigers finden Sie unter [tätigen eines Aufrufes](make-a-call.md) oder [empfangen eines aufrufscodes](receive-a-call.md) .</span><span class="sxs-lookup"><span data-stu-id="82397-107">See [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md) for code examples on how to obtain this pointer.</span></span>

> [!Note]  
> <span data-ttu-id="82397-108">Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="82397-108">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// pAddress is an ITAddress interface pointer.
// pBasicCall is an ITBasicCallControl interface pointer.

// Get the ITStreamControl interface.
ITStreamControl * pStreamControl;
HRESULT hr = pBasicCall->QueryInterface(
        IID_ITStreamControl,
        (void **) &pStreamControl
        );
// If ( hr != S_OK ) process the error here. 

// Enumerate the streams and select 
// terminals onto them.
IEnumStream * pEnumStreams;
ITStream    * pStream;
hr = pStreamControl->EnumerateStreams(&pEnumStreams);
// If ( hr != S_OK ) process the error here. 

while ( S_OK == pEnumStreams->Next(1, &pStream, NULL) )
{
    // Get the media type and direction of this stream.
    long                lMediaType;
    TERMINAL_DIRECTION  dir;
    hr = pStream->get_MediaType( &lMediaType );
    // If ( hr != S_OK ) process the error here. 
    hr = pStream->get_Direction( &dir );
    // If ( hr != S_OK ) process the error here. 

    // Create the default terminal for this media type and direction.
    //   If lMediaType == TAPIMEDIATYPE_VIDEO and
    //   dir == TD_RENDER, a dynamic video render terminal
    //   is required. Please see Incoming.cpp in 
    //   the samples section of the SDK. 
    // For all other terminals, get the default static terminal.
    ITTerminal * pTerminal;
    ITTerminalSupport * pTerminalSupport;
    hr = pAddress->QueryInterface( 
            IID_ITTerminalSupport, 
            (void **)&pTerminalSupport
         );
    // If ( hr != S_OK ) process the error here. 
    hr = pTerminalSupport->GetDefaultStaticTerminal(
            lMediaType,
            dir,
            pTerminal
         );
    // If ( hr != S_OK ) process the error here. 
    // Select the terminal on the stream.
    hr = pStream->SelectTerminal(pTerminal);
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a><span data-ttu-id="82397-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82397-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82397-110">**Itaddress**</span><span class="sxs-lookup"><span data-stu-id="82397-110">**ITAddress**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)
</dt> <dt>

[<span data-ttu-id="82397-111">**Itbasiccallcontrol**</span><span class="sxs-lookup"><span data-stu-id="82397-111">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="82397-112">**Itstreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="82397-112">**ITStreamControl**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)
</dt> <dt>

[<span data-ttu-id="82397-113">**Itstream**</span><span class="sxs-lookup"><span data-stu-id="82397-113">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="82397-114">**Ienumstream**</span><span class="sxs-lookup"><span data-stu-id="82397-114">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="82397-115">**Itterminal**</span><span class="sxs-lookup"><span data-stu-id="82397-115">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> <dt>

[<span data-ttu-id="82397-116">**Itterminalsupport**</span><span class="sxs-lookup"><span data-stu-id="82397-116">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
