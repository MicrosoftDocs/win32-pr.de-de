---
title: Primitive und benutzerdefinierte Bindungs Handles
description: Alle Handles, die mit den Handle \_ t-oder RPC- \_ Bindungs handle-Typen deklariert werden, \_ sind primitive Bindungs Handles.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039491"
---
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="ca23f-103">Primitive und benutzerdefinierte Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="ca23f-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="ca23f-104">Alle Handles, die mit den [handle \_ t](/windows/desktop/Midl/handle-t) -oder [**RPC- \_ Bindungs \_ handle**](rpc-binding-handle.md) -Typen deklariert werden, sind primitive Bindungs Handles.</span><span class="sxs-lookup"><span data-stu-id="ca23f-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="ca23f-105">Sie können die [handle \_ t](/windows/desktop/Midl/handle-t) -oder [**RPC- \_ Bindungs \_ handle**](rpc-binding-handle.md) -Typen so erweitern, dass mehr oder andere Informationen als der primitive Handle-Typ enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ca23f-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="ca23f-106">Wenn Sie dies tun, erstellen Sie ein benutzerdefiniertes Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="ca23f-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="ca23f-107">Um ein benutzerdefiniertes Bindungs Handle für Ihre verteilte Anwendung zu erstellen, müssen Sie einen eigenen Datentyp erstellen und das \[ [handle](/windows/desktop/Midl/handle) - \] Attribut für eine Typdefinition in der IDL-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="ca23f-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="ca23f-108">Letztendlich ordnen die Stub-Dateien primitive Handles benutzerdefinierte Bindungs Handles zu.</span><span class="sxs-lookup"><span data-stu-id="ca23f-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="ca23f-109">Wenn Sie einen eigenen Bindungs Handle-Typ erstellen, müssen Sie auch Bindungs-und Bindung-Routinen bereitstellen, die der Clientstub verwendet, um ein benutzerdefiniertes Handle einem primitiven handle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ca23f-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="ca23f-110">Der Stub Ruft die BIND-und Bindung-Routinen am Anfang und am Ende jedes Remote Prozedur Aufrufs auf.</span><span class="sxs-lookup"><span data-stu-id="ca23f-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="ca23f-111">Die Bindungs-und Bindung-Routinen müssen den folgenden Funktionsprototypen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ca23f-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="ca23f-112">Funktionsprototyp</span><span class="sxs-lookup"><span data-stu-id="ca23f-112">Function prototype</span></span>                     | <span data-ttu-id="ca23f-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca23f-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="ca23f-114">Handle \_ t- \_ Typbindung (*Typ*)</span><span class="sxs-lookup"><span data-stu-id="ca23f-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="ca23f-115">Bindungs Routine</span><span class="sxs-lookup"><span data-stu-id="ca23f-115">Binding routine</span></span>   |
| <span data-ttu-id="ca23f-116">void Type \_ Unbind (*Type*, *handle \_ t*)</span><span class="sxs-lookup"><span data-stu-id="ca23f-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="ca23f-117">Bindung der Routine aufheben</span><span class="sxs-lookup"><span data-stu-id="ca23f-117">Unbinding routine</span></span> |



 

<span data-ttu-id="ca23f-118">Im folgenden Beispiel wird gezeigt, wie ein benutzerdefiniertes Bindungs Handle in der IDL-Datei definiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="ca23f-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

<span data-ttu-id="ca23f-119">Wenn die Bindungs Routine einen Fehler feststellt, sollte Sie mithilfe der [**rpcraiseexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) -Funktion eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="ca23f-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="ca23f-120">Der Clientstub wird dann bereinigt, und die Ausnahme wird durch den Ausnahme Block für den Remote Prozedur Aufrufe auf der Clientseite gefiltert.</span><span class="sxs-lookup"><span data-stu-id="ca23f-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="ca23f-121">Wenn die Bindungs Routine einfach **null** zurückgibt, wird der Client Code Fehler-RPC \_ S \_ ungültige \_ Bindung erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca23f-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="ca23f-122">Dies kann in bestimmten Situationen akzeptabel sein, aber andere Situationen (z. b. nicht genügend Arbeitsspeicher) Antworten nicht gut.</span><span class="sxs-lookup"><span data-stu-id="ca23f-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="ca23f-123">Die Bindung-Routine sollte so entworfen werden, dass Sie nicht fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ca23f-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="ca23f-124">Die Bindung-Routine sollte keine Ausnahmen ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ca23f-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="ca23f-125">Die vom Programmierer definierten Bindungs-und Bindung-Routinen werden in der Client Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca23f-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="ca23f-126">Im folgenden Beispiel ruft die BIND-Routine [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um die Zeichen folgen Bindungs Informationen in ein Bindungs Handle zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ca23f-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="ca23f-127">Die Bindung-Routine ruft [**rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) auf, um das Bindungs Handle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ca23f-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="ca23f-128">Der Name des vom Programmierer definierten Bindungs Handles, Daten \_ handle \_ Type, wird als Teil des Namens der Funktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca23f-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="ca23f-129">Sie wird auch als Parametertyp in den Funktionsparametern verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca23f-129">It is also used as the parameter type in the function parameters.</span></span>

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

<span data-ttu-id="ca23f-130">Sowohl implizite als auch explizite Bindungs Handles können primitive oder benutzerdefinierte Handles sein.</span><span class="sxs-lookup"><span data-stu-id="ca23f-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="ca23f-131">Das heißt, ein Handle kann sein:</span><span class="sxs-lookup"><span data-stu-id="ca23f-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="ca23f-132">Primitiv und implizit</span><span class="sxs-lookup"><span data-stu-id="ca23f-132">Primitive and implicit</span></span>
-   <span data-ttu-id="ca23f-133">Benutzer definiert und implizit</span><span class="sxs-lookup"><span data-stu-id="ca23f-133">Custom and implicit</span></span>
-   <span data-ttu-id="ca23f-134">Primitiv und explizit</span><span class="sxs-lookup"><span data-stu-id="ca23f-134">Primitive and explicit</span></span>
-   <span data-ttu-id="ca23f-135">Benutzer definiert und explizit</span><span class="sxs-lookup"><span data-stu-id="ca23f-135">Custom and explicit</span></span>

 

 