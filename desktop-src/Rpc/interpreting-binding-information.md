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
# <a name="interpreting-binding-information"></a><span data-ttu-id="5a3c5-104">Interpretieren von Bindungs Informationen</span><span class="sxs-lookup"><span data-stu-id="5a3c5-104">Interpreting Binding Information</span></span>

<span data-ttu-id="5a3c5-105">Microsoft RPC ermöglicht es Ihren Client-und Serverprogrammen, auf die Informationen in einem Bindungs handle zuzugreifen und diese zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="5a3c5-106">Dies bedeutet nicht, dass Sie direkt auf den Inhalt eines Bindungs Handles zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="5a3c5-107">Microsoft RPC stellt Funktionen bereit, mit denen die Informationen in Bindungs Handles festgelegt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="5a3c5-108">Um die Informationen in einem Bindungs Handle zu erhalten, übergeben Sie das Handle an [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="5a3c5-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="5a3c5-109">Die Bindungs Informationen werden als Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-109">It returns the binding information as a string.</span></span> <span data-ttu-id="5a3c5-110">Für jeden Aufrufen von **rpcbindingtostringbinding** müssen Sie über einen entsprechenden Aufrufs der Funktion [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree)verfügen.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="5a3c5-111">Sie können die Funktion [**rpcstringbindinganalyse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) aufrufen, um die Zeichenfolge zu analysieren, die Sie von [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)erhalten.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="5a3c5-112">Diese Funktion ordnet Zeichen folgen zu, die die Informationen enthalten, die Sie analysiert.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="5a3c5-113">Wenn Sie nicht möchten, dass ein bestimmtes Bindungs Informationselement analysiert wird, übergeben Sie einen **null** -Wert als Wert dieses Parameters.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="5a3c5-114">Stellen Sie sicher, dass Sie für jede der Zeichen folgen, die Sie zuordnet, [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) aufruft.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="5a3c5-115">Das folgende Code Fragment veranschaulicht, wie eine Anwendung diese Funktionen aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-115">The following code fragment illustrates how an application might call these functions.</span></span>


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



<span data-ttu-id="5a3c5-116">Im obigen Beispielcode werden die Funktionen [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) und [**rpcstringbindinganalyse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) aufgerufen, um die Informationen in einem gültigen Bindungs Handle zu erhalten und zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="5a3c5-117">Beachten Sie, dass der Wert **null** als zweiter Parameter an **rpcstringbindinganalyse** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="5a3c5-118">Dies bewirkt, dass diese Funktion das Auswerten der Objekt-UUID überspringt.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="5a3c5-119">Da die UUID nicht analysiert wird, weist **rpcstringbindinganalyse** keine Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="5a3c5-120">Diese Technik ermöglicht der Anwendung, nur Speicher für die Informationen zuzuweisen, die analysiert und analysiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a3c5-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 




