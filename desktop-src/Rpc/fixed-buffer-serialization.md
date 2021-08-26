---
title: Pufferserialisierung korrigiert
description: Pufferserialisierung korrigiert.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce58d3bdf92673c97ae8dc9fbbf8f366cb4a59a9e3ce114431de1581af30ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021210"
---
# <a name="fixed-buffer-serialization"></a>Pufferserialisierung korrigiert

Geben Sie bei Verwendung des festen Pufferstils einen Puffer an, der groß genug ist, um die mit dem Handle ausgeführten Codierungsvorgänge (Marshalling) zu unterstützen. Beim Unmarshaling stellen Sie den Puffer mit allen zu decodenden Daten zur Verfügung.

Der feste Pufferstil der Serialisierung verwendet die folgenden Routinen:

-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Die **MesEncodeFixedBufferHandleCreate-Funktion** weist den für das Codierungshandle benötigten Arbeitsspeicher zu und initialisiert ihn anschließend. Die Anwendung kann [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) aufrufen, um das Handle erneut zu initialisieren, oder [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) aufrufen, um den Arbeitsspeicher des Handles frei zu geben. Um ein Decodierungshandle zu erstellen, das dem Handle mit fester Formatcodierung entspricht, müssen Sie [**MesDecodeBufferHandleCreate verwenden.**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)

Die Anwendung ruft [**MesHandleFree auf,**](/windows/desktop/api/Midles/nf-midles-meshandlefree) um das Codierungs- oder Decodierungspufferhandle frei zu geben.

## <a name="examples-of-fixed-buffer-encoding"></a>Beispiele für feste Puffercodierung

Der folgende Abschnitt enthält ein Beispiel für die Verwendung eines festen Pufferformats– serialisierendes Handle für die Prozedurcodierung.

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

Der folgende Abschnitt enthält ein Beispiel für die Verwendung eines festen Pufferformats– serialisierendes Handle für die Typcodierung.

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

Der folgende Auszug stellt die relevanten Anwendungsfragmente dar.


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



 

 




