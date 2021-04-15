---
title: Application-Allocated Puffer
description: Das ACF-Attribut \ Byte \_ Anzahl \ weist die Stub an, einen vorab zugeordneten Puffer zu verwenden, der nicht von den Client-Unterstützungs Routinen zugeordnet oder freigegeben wird.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473916"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="812c5-103">Application-Allocated Puffer</span><span class="sxs-lookup"><span data-stu-id="812c5-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="812c5-104">Die Byte Anzahl der ACF-Attribute weist \[ [**\_**](/windows/desktop/Midl/byte-count) \] die Stub an, einen vorab zugeordneten Puffer zu verwenden, der nicht von den Client-Unterstützungs Routinen zugeordnet oder freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="812c5-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="812c5-105">Das \[ **Byte \_ count** - \] Attribut wird auf einen Zeiger-oder Array Parameter angewendet, der auf den Puffer zeigt.</span><span class="sxs-lookup"><span data-stu-id="812c5-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="812c5-106">Hierfür ist ein Parameter erforderlich, der die Puffergröße in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="812c5-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="812c5-107">Der vom Client zugewiesene Speicherbereich kann komplexe Datenstrukturen mit mehreren Zeigern enthalten.</span><span class="sxs-lookup"><span data-stu-id="812c5-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="812c5-108">Da der Speicherbereich zusammenhängend ist, muss die Anwendung nicht mehrere Aufrufe durchführen, um jeden Zeiger und jede Struktur einzeln freizugeben.</span><span class="sxs-lookup"><span data-stu-id="812c5-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="812c5-109">Wie bei Verwendung des Attributs "Allocation" \[ [**(alle \_ Knoten)**](/windows/desktop/Midl/allocate) \] kann der Speicherbereich mit einem Rückruf der Speicher Belegungs Routine oder der kostenlosen Routine zugeordnet oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="812c5-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="812c5-110">Anders als bei Verwendung des \[ Attributs " **zuordnen" (alle \_ Knoten)** \] wird der Puffer Parameter jedoch nicht vom Client-Stub, sondern von der Client Anwendung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="812c5-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="812c5-111">Der Puffer muss ein \[ [](/windows/desktop/Midl/out-idl) \] nur-Out-Parameter sein, und die Pufferlänge in Byte muss ein \[ [](/windows/desktop/Midl/in) \] nur-der-Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="812c5-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="812c5-112">Das \[ [**Byte \_ count**](/windows/desktop/Midl/byte-count) - \] Attribut kann nur auf Zeiger Typen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="812c5-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="812c5-113">Das \[ ACF-Attribut für die **Byte \_ Anzahl** \] ist eine Microsoft-Erweiterung für DCE-IDL und ist daher nicht verfügbar, wenn Sie mit dem [**/OSF**](/windows/desktop/Midl/-osf) -Schalter für mittlere Kompilierung kompilieren.</span><span class="sxs-lookup"><span data-stu-id="812c5-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="812c5-114">Im folgenden Beispiel verwendet der Parameter *Proot* Byte Anzahl:</span><span class="sxs-lookup"><span data-stu-id="812c5-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="812c5-115">Das \[ [**Byte \_ count**](/windows/desktop/Midl/byte-count) - \] Attribut wird in der ACF wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="812c5-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="812c5-116">Der von diesen IDL-und ACF-Dateien generierte Clientstub weist den Speicher für diesen Puffer nicht zu oder gibt diesen frei.</span><span class="sxs-lookup"><span data-stu-id="812c5-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="812c5-117">Der Serverstub ordnet den Puffer zu und gibt ihn in einem einzelnen-Befehl mit dem angegebenen Size-Parameter frei.</span><span class="sxs-lookup"><span data-stu-id="812c5-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="812c5-118">Wenn die Daten für die angegebene Puffergröße zu groß sind, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="812c5-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 