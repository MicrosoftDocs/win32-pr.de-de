---
title: Die midl_user_allocate-Funktion
description: Die Funktion "Mittel l- \_ Benutzer \_ zuweisen" ist ein Verfahren, das von Entwicklern von RPC-Anwendungen bereitgestellt werden muss.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102006"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="d39b4-103">Die Funktion "Mittel l- \_ Benutzer \_ zuweisen"</span><span class="sxs-lookup"><span data-stu-id="d39b4-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="d39b4-104">Die Funktion " **Mittel l- \_ Benutzer \_ zuweisen** " ist ein Verfahren, das von Entwicklern von RPC-Anwendungen bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d39b4-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="d39b4-105">Dadurch wird Arbeitsspeicher für die RPC-stubspeicher und Bibliotheks Routinen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d39b4-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="d39b4-106">Die Funktion " **Mittel l- \_ Benutzer \_ Zuordnung** " muss dem folgenden Prototyp entsprechen:</span><span class="sxs-lookup"><span data-stu-id="d39b4-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="d39b4-107">Der *cbytes* -Parameter gibt die Anzahl der zuzuordnenden Bytes an.</span><span class="sxs-lookup"><span data-stu-id="d39b4-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="d39b4-108">Sowohl Client Anwendungen als auch Server Anwendungen müssen die Funktion " **Mittell- \_ Benutzer \_ zuweisen** " implementieren, es sei denn, Sie kompilieren ihn im OSF-Kompatibilitätsmodus (/OSF).</span><span class="sxs-lookup"><span data-stu-id="d39b4-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="d39b4-109">Von Anwendungen und generierten stubjekten wird die **\_ \_ Zuordnung von Benutzer** Zuordnungen direkt oder indirekt zum Verwalten zugewiesener Objekte aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d39b4-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="d39b4-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d39b4-110">For example:</span></span>

-   <span data-ttu-id="d39b4-111">Die Client-und Server Anwendungen wenden die Benutzer Zuordnungen für den **\_ Benutzer \_** an, um Arbeitsspeicher für die Anwendung zuzuweisen, z. b. Wenn ein neuer Knoten in einer Struktur oder verknüpften Liste erstellt wird</span><span class="sxs-lookup"><span data-stu-id="d39b4-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="d39b4-112">Der Serverstub Ruft beim Marshalling von Daten in den Server Adressraum die **mittlere \_ Benutzer \_** Zuordnungen auf.</span><span class="sxs-lookup"><span data-stu-id="d39b4-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="d39b4-113">Der Clientstub Ruft bei der Aufhebung des Marshalling von Daten von dem Server, auf den von einem out-Zeiger verwiesen wird, die Benutzer Zuordnungen für **mittlere \_ Benutzer \_** auf \[ \]</span><span class="sxs-lookup"><span data-stu-id="d39b4-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="d39b4-114">Beachten Sie, \[ dass \] \[ \] der Client-Stub bei in-, out-und \[ Unique \] -Zeigern nur dann die **\_ Benutzer \_** Zuordnungen aufruft, wenn der \[ eindeutige \] Zeiger Wert bei Eingabe NULL war und während des Aufrufs zu einem Wert ungleich NULL wechselt.</span><span class="sxs-lookup"><span data-stu-id="d39b4-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="d39b4-115">Wenn der \[ eindeutige \] Zeiger bei Eingabe ungleich Null war, schreibt der Clientstub die zugeordneten Daten in den vorhandenen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d39b4-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="d39b4-116">Wenn die Benutzer Zuordnungen von **\_ Benutzer \_** Zuordnungen keinen Arbeitsspeicher zuordnen können, sollte ein NULL-Zeiger zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d39b4-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="d39b4-117">Die **\_ Benutzer \_** Zuordnungs Funktion "Mittel l" sollte einen 8-Byte-ausgerichteten Zeiger zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d39b4-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="d39b4-118">Beispielsweise implementieren die Beispiel Programme, die mit dem Platform Software Development Kit (SDK) bereitgestellt werden, eine **mittlere \_ Benutzer \_** Zuordnungen im Hinblick auf die C-Funktion [**malloc**](pointers-and-memory-allocation.md):</span><span class="sxs-lookup"><span data-stu-id="d39b4-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="d39b4-119">Wenn das RPCSS-Paket aktiviert ist (z. b. als Ergebnis der Verwendung des \[ Attributs " [**\_ zuordnen**](/windows/desktop/Midl/enable-allocate) " \] ), verwenden Sie " [**rpcsmallo"**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) , um Arbeitsspeicher auf der Serverseite zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d39b4-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="d39b4-120">Weitere Informationen zum Aktivieren von " \[ **\_ zuordnen**" \] finden Sie unter " [Mittel l Reference](/windows/desktop/Midl/midl-language-reference)".</span><span class="sxs-lookup"><span data-stu-id="d39b4-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 