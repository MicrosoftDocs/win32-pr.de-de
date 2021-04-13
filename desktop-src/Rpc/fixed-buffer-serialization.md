---
title: Serialisierung fester Puffer
description: Fixierte pufferserialisierung.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388387"
---
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="4503e-103">Serialisierung fester Puffer</span><span class="sxs-lookup"><span data-stu-id="4503e-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="4503e-104">Geben Sie bei Verwendung des festgelegten Puffer Stils einen Puffer an, der groß genug ist, um die mit dem Handle ausgeführten Codierungs Vorgänge (Marshalling) aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="4503e-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="4503e-105">Wenn Sie das Marshalling durchlaufen, stellen Sie den Puffer bereit, der alle zu decodierende Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="4503e-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="4503e-106">Der Puffer Stil der Serialisierung verwendet die folgenden Routinen:</span><span class="sxs-lookup"><span data-stu-id="4503e-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="4503e-107">**Mesencodefixedbufferlenker Create**</span><span class="sxs-lookup"><span data-stu-id="4503e-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="4503e-108">**Mesdecodebufferlagercreate**</span><span class="sxs-lookup"><span data-stu-id="4503e-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="4503e-109">**Mesbufferhandlereset**</span><span class="sxs-lookup"><span data-stu-id="4503e-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="4503e-110">**Meslenker frei**</span><span class="sxs-lookup"><span data-stu-id="4503e-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="4503e-111">Die **mesencodefixedbuffergscreate** -Funktion ordnet den erforderlichen Arbeitsspeicher für das Codierungs Handle zu und initialisiert ihn anschließend.</span><span class="sxs-lookup"><span data-stu-id="4503e-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="4503e-112">Die Anwendung kann [**mesbufferhandlereset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) aufrufen, um das Handle erneut zu initialisieren, oder Sie kann [**meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree) aufrufen, um den Arbeitsspeicher des Handles freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4503e-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="4503e-113">Zum Erstellen eines Decodierungs Handles, das dem –-Codierungs Handle mit festem Format entspricht, müssen Sie [**mesdecodebuffergsercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)verwenden.</span><span class="sxs-lookup"><span data-stu-id="4503e-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="4503e-114">Die Anwendung ruft [**meslenker Free**](/windows/desktop/api/Midles/nf-midles-meshandlefree) auf, um das Codierungs-oder Decodierungs Puffer Handle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4503e-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="4503e-115">Beispiele für die Verschlüsselung fester Puffer</span><span class="sxs-lookup"><span data-stu-id="4503e-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="4503e-116">Der folgende Abschnitt enthält ein Beispiel für die Verwendung eines Festes Puffer Stils – Serialisieren des Handles für die Prozedur Codierung.</span><span class="sxs-lookup"><span data-stu-id="4503e-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

<span data-ttu-id="4503e-117">Der folgende Auszug stellt einen Teil einer Anwendung dar.</span><span class="sxs-lookup"><span data-stu-id="4503e-117">The following excerpt represents a part of an application.</span></span>

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

<span data-ttu-id="4503e-118">Der folgende Abschnitt enthält ein Beispiel für die Verwendung eines Festes Puffer Stils – Serialisieren des Handles für die typcodierung.</span><span class="sxs-lookup"><span data-stu-id="4503e-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

<span data-ttu-id="4503e-119">Der folgende Auszug stellt die relevanten Anwendungs Fragmente dar.</span><span class="sxs-lookup"><span data-stu-id="4503e-119">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




