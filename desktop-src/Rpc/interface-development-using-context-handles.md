---
title: Schnittstellen Entwicklung mithilfe von Kontext Handles
description: In der Regel erstellen Sie ein Kontext Handle, indem Sie das \ Context \_ handle \-Attribut für eine Typdefinition in der IDL-Datei angeben.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729312"
---
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="77789-103">Schnittstellen Entwicklung mithilfe von Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="77789-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="77789-104">In der Regel erstellen Sie ein Kontext Handle, indem Sie das \[ [**Kontext \_ handle**](/windows/desktop/Midl/context-handle) - \] Attribut für eine Typdefinition in der IDL-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="77789-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="77789-105">Die Typdefinition gibt auch implizit eine Kontext-Lauf Ablaufroutine an, die Sie bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="77789-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="77789-106">Wenn die Kommunikation zwischen dem Client und dem Server unterbrochen wird, ruft die Server Laufzeit diese Routine auf, um alle erforderlichen Bereinigungs Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="77789-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="77789-107">Weitere Informationen zu Kontext-run-down-Routinen finden Sie unter [Server Context-Lauf-ab-Routine](server-context-run-down-routine.md).</span><span class="sxs-lookup"><span data-stu-id="77789-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="77789-108">Eine Schnittstelle, die ein Kontext Handle verwendet, muss über ein Bindungs Handle für die anfängliche Bindung verfügen, das durchgeführt werden muss, bevor der Server ein Kontext Handle zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="77789-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="77789-109">Sie können ein automatisches, implizites oder explizites Bindungs Handle verwenden, um die Bindung zu erstellen und den Kontext festzulegen.</span><span class="sxs-lookup"><span data-stu-id="77789-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="77789-110">Ein Kontext Handle muss den [**void \***](/windows/desktop/Midl/void) -Typ oder einen Typ aufweisen, der in " [**void \***](/windows/desktop/Midl/void)" aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="77789-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="77789-111">Das Serverprogramm wandelt es in den erforderlichen Typ um.</span><span class="sxs-lookup"><span data-stu-id="77789-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="77789-112">Die Verwendung von \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] für Kontext handle-Parameter wird davon abgeraten, mit Ausnahme von Routinen, die Kontext Handles schließen.</span><span class="sxs-lookup"><span data-stu-id="77789-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="77789-113">Wenn Kontext handle-Parameter, die \[ [**in**](/windows/desktop/Midl/in)gekennzeichnet [](/windows/desktop/Midl/out-idl) \] sind, verwendet werden, übergeben Sie kein **null** -oder nicht initialisiertes Kontext Handle vom Client an den Server.</span><span class="sxs-lookup"><span data-stu-id="77789-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="77789-114">Stattdessen sollte ein **null** -Zeiger auf ein Kontext Handle übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="77789-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="77789-115">Beachten Sie, dass die in markierten Kontext handle-Parameter \[ [](/windows/desktop/Midl/in) \] keine **null** -Zeiger akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="77789-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="77789-116">Das folgende Fragment einer Beispiel Schnittstellen Definition zeigt, wie eine verteilte Anwendung ein Kontext Handle verwenden kann, um einen Server zu öffnen und eine Datendatei für jeden Client zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="77789-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="77789-117">Die-Schnittstelle muss einen Remote Prozedur aufrufsbefehl enthalten, um das Handle zu initialisieren und es auf einen Wert ungleich **null** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="77789-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="77789-118">In diesem Beispiel führt die remoteopen-Funktion diesen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="77789-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="77789-119">Er gibt das Kontext Handle mit einem \[ [**out**](/windows/desktop/Midl/out-idl) - \] direktionalen Attribut an.</span><span class="sxs-lookup"><span data-stu-id="77789-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="77789-120">Alternativ könnten Sie das Kontext Handle als Rückgabewert der Prozedur zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="77789-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="77789-121">In diesem Beispiel übergeben wir das Kontext Handle in der Parameterliste.</span><span class="sxs-lookup"><span data-stu-id="77789-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="77789-122">In diesem Beispiel handelt es sich bei den Kontextinformationen um ein Datei handle.</span><span class="sxs-lookup"><span data-stu-id="77789-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="77789-123">Der aktuelle Speicherort in der Datei wird nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="77789-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="77789-124">Die-Schnittstelle verpackt das Datei Handle als Kontext Handle und übergibt es als Parameter an Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="77789-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="77789-125">Eine-Struktur enthält den Dateinamen und das Datei handle.</span><span class="sxs-lookup"><span data-stu-id="77789-125">A structure contains the file name and the file handle.</span></span>

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

<span data-ttu-id="77789-126">Die Funktion remoteopen erstellt ein gültiges Kontext Handle, das nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="77789-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="77789-127">Er übergibt das Kontext Handle an den Client.</span><span class="sxs-lookup"><span data-stu-id="77789-127">It passes the context handle to the client.</span></span> <span data-ttu-id="77789-128">Nachfolgende Remote Prozedur Aufrufe, wie z. b. RemoteRead, verwenden das Kontext Handle als in-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="77789-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="77789-129">Zusätzlich zu der Remote Prozedur, mit der das Kontext Handle initialisiert wird, muss die-Schnittstelle eine Prozedur enthalten, die den Server Kontext freigibt und das Kontext Handle auf **null** festlegt.</span><span class="sxs-lookup"><span data-stu-id="77789-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="77789-130">Im vorherigen Beispiel führt die remoteclose-Funktion diesen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="77789-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 