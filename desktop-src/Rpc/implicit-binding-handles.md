---
title: Implizite Bindungs Handles
description: Implizite Bindungs Handles ermöglichen der Anwendung, einen bestimmten Server für die Ausführung der Remote Prozedur Aufrufe auszuwählen.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039100"
---
# <a name="implicit-binding-handles"></a><span data-ttu-id="af394-103">Implizite Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="af394-103">Implicit Binding Handles</span></span>

<span data-ttu-id="af394-104">Implizite Bindungs Handles ermöglichen der Anwendung, einen bestimmten Server für die Ausführung der Remote Prozedur Aufrufe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="af394-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="af394-105">Weitere Informationen finden Sie unter [Client seitige Bindung](client-side-binding.md).</span><span class="sxs-lookup"><span data-stu-id="af394-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="af394-106">Außerdem können Sie mit dem Client/Server-Programm authentifizierte Bindungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="af394-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="af394-107">Das heißt, der Client kann Authentifizierungsinformationen in einem impliziten Bindungs Handle angeben.</span><span class="sxs-lookup"><span data-stu-id="af394-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="af394-108">Die RPC-Lauf Zeit Bibliothek verwendet die Authentifizierungsinformationen, um eine authentifizierte RPC-Sitzung zwischen dem Client und dem Server einzurichten.</span><span class="sxs-lookup"><span data-stu-id="af394-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="af394-109">Weitere Informationen finden Sie unter [Sicherheit](security.md).</span><span class="sxs-lookup"><span data-stu-id="af394-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="af394-110">Implizite Bindungs Handles sind nicht Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="af394-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="af394-111">Multithreadanwendungen sollten daher die Verwendung impliziter Bindungs Handles vermeiden.</span><span class="sxs-lookup"><span data-stu-id="af394-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="af394-112">Wenn Ihre Anwendung implizite Bindungen verwendet, muss der Client die Bindungs Informationen so festlegen, dass die Bindung erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="af394-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="af394-113">Nachdem der Client eine implizite Bindung erstellt hat, muss er keine Bindungs Handles an Remote Prozeduren übergeben.</span><span class="sxs-lookup"><span data-stu-id="af394-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="af394-114">Die RPC-Bibliothek behandelt die restlichen Mechanismen der Kommunikationssitzung.</span><span class="sxs-lookup"><span data-stu-id="af394-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="af394-115">Der Client speichert die Bindungs Informationen für ein implizites Handle in einer globalen Variablen.</span><span class="sxs-lookup"><span data-stu-id="af394-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="af394-116">Wenn der Mittell-Compiler den Clientstub und die Header Datei aus der Schnittstellen Spezifikation in der mittleren l-Datei generiert, generiert er auch Code für eine globale Bindungs handle-Variable.</span><span class="sxs-lookup"><span data-stu-id="af394-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="af394-117">Das Client Programm initialisiert das Handle und verweist erst wieder auf das Handle, wenn die Bindung zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="af394-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="af394-118">Sie erstellen ein implizites handle, indem Sie das \[ [**implizite \_ handle**](/windows/desktop/Midl/implicit-handle) - \] Attribut in der ACF für eine Schnittstelle wie folgt angeben:</span><span class="sxs-lookup"><span data-stu-id="af394-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="af394-119">Der **handle \_ t** -Typ, der im vorherigen Beispiel verwendet wird, ist ein mittlerer Datentyp, der zum Definieren von Bindungs Handles verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af394-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="af394-120">Nachdem Sie das implizite Handle erstellt haben, muss es von der Anwendung als Parameter für die RPC-Lauf Zeit Bibliotheksfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af394-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="af394-121">Verwenden Sie das implizite Handle nicht als Parameter für Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="af394-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="af394-122">Im folgenden Codebeispiel wird die Verwendung impliziter Bindungs Handles veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="af394-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="af394-123">Im vorherigen Beispiel mussten die RPC-Lauf Zeit Bibliotheksfunktionen [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) und [**rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) den impliziten Bindungs Handle in ihren Parameterlisten übergeben.</span><span class="sxs-lookup"><span data-stu-id="af394-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="af394-124">Bei der Remote Prozedur myremoteprocedure ist dies jedoch nicht der Fall, da es sich nicht um eine RPC-Lauf Zeit Bibliotheksfunktion handelt.</span><span class="sxs-lookup"><span data-stu-id="af394-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 