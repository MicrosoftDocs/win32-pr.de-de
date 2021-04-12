---
title: Interpretieren von Bindungs Informationen
description: Microsoft RPC ermöglicht es Ihren Client-und Serverprogrammen, auf die Informationen in einem Bindungs handle zuzugreifen und diese zu interpretieren.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Interpretieren von Bindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471733"
---
# <a name="interpreting-binding-information"></a>Interpretieren von Bindungs Informationen

Microsoft RPC ermöglicht es Ihren Client-und Serverprogrammen, auf die Informationen in einem Bindungs handle zuzugreifen und diese zu interpretieren. Dies bedeutet nicht, dass Sie direkt auf den Inhalt eines Bindungs Handles zugreifen können. Microsoft RPC stellt Funktionen bereit, mit denen die Informationen in Bindungs Handles festgelegt und abgerufen werden.

Um die Informationen in einem Bindungs Handle zu erhalten, übergeben Sie das Handle an [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Die Bindungs Informationen werden als Zeichenfolge zurückgegeben. Für jeden Aufrufen von **rpcbindingtostringbinding** müssen Sie über einen entsprechenden Aufrufs der Funktion [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree)verfügen.

Sie können die Funktion [**rpcstringbindinganalyse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) aufrufen, um die Zeichenfolge zu analysieren, die Sie von [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)erhalten. Diese Funktion ordnet Zeichen folgen zu, die die Informationen enthalten, die Sie analysiert. Wenn Sie nicht möchten, dass ein bestimmtes Bindungs Informationselement analysiert wird, übergeben Sie einen **null** -Wert als Wert dieses Parameters. Stellen Sie sicher, dass Sie für jede der Zeichen folgen, die Sie zuordnet, [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) aufruft.

Das folgende Code Fragment veranschaulicht, wie eine Anwendung diese Funktionen aufrufen kann.


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



Im obigen Beispielcode werden die Funktionen [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) und [**rpcstringbindinganalyse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) aufgerufen, um die Informationen in einem gültigen Bindungs Handle zu erhalten und zu analysieren. Beachten Sie, dass der Wert **null** als zweiter Parameter an **rpcstringbindinganalyse** übergeben wurde. Dies bewirkt, dass diese Funktion das Auswerten der Objekt-UUID überspringt. Da die UUID nicht analysiert wird, weist **rpcstringbindinganalyse** keine Zeichenfolge zu. Diese Technik ermöglicht der Anwendung, nur Speicher für die Informationen zuzuweisen, die analysiert und analysiert werden sollen.

 

 




