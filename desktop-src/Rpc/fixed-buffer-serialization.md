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
# <a name="fixed-buffer-serialization"></a>Serialisierung fester Puffer

Geben Sie bei Verwendung des festgelegten Puffer Stils einen Puffer an, der groß genug ist, um die mit dem Handle ausgeführten Codierungs Vorgänge (Marshalling) aufnehmen zu können. Wenn Sie das Marshalling durchlaufen, stellen Sie den Puffer bereit, der alle zu decodierende Daten enthält.

Der Puffer Stil der Serialisierung verwendet die folgenden Routinen:

-   [**Mesencodefixedbufferlenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**Mesdecodebufferlagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**Mesbufferhandlereset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**Meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Die **mesencodefixedbuffergscreate** -Funktion ordnet den erforderlichen Arbeitsspeicher für das Codierungs Handle zu und initialisiert ihn anschließend. Die Anwendung kann [**mesbufferhandlereset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) aufrufen, um das Handle erneut zu initialisieren, oder Sie kann [**meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree) aufrufen, um den Arbeitsspeicher des Handles freizugeben. Zum Erstellen eines Decodierungs Handles, das dem –-Codierungs Handle mit festem Format entspricht, müssen Sie [**mesdecodebuffergsercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)verwenden.

Die Anwendung ruft [**meslenker Free**](/windows/desktop/api/Midles/nf-midles-meshandlefree) auf, um das Codierungs-oder Decodierungs Puffer Handle freizugeben.

## <a name="examples-of-fixed-buffer-encoding"></a>Beispiele für die Verschlüsselung fester Puffer

Der folgende Abschnitt enthält ein Beispiel für die Verwendung eines Festes Puffer Stils – Serialisieren des Handles für die Prozedur Codierung.

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

Der folgende Auszug stellt einen Teil einer Anwendung dar.

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

Der folgende Abschnitt enthält ein Beispiel für die Verwendung eines Festes Puffer Stils – Serialisieren des Handles für die typcodierung.

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

Der folgende Auszug stellt die relevanten Anwendungs Fragmente dar.


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



 

 




