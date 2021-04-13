---
title: Erstellen der globalen Schnittstellen Tabelle
description: Erstellen der globalen Schnittstellen Tabelle
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391088"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="4e001-103">Erstellen der globalen Schnittstellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="4e001-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="4e001-104">Verwenden Sie den folgenden Aufruf, um das globale Schnittstellen Tabellenobjekt zu erstellen, und rufen Sie einen Zeiger auf [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)ab:</span><span class="sxs-lookup"><span data-stu-id="4e001-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="4e001-105">Beim Erstellen des globalen Schnittstellen Tabellenobjekts mit dem vorhergehenden-Befehl ist es erforderlich, eine Verknüpfung mit der Bibliothek UUID. lib herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4e001-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="4e001-106">Hierdurch werden die externen Symbole CLSID \_ stdglobalinterfaketable und IID \_ iglobalinterfaketable aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4e001-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="4e001-107">Es gibt eine einzelne Instanz der globalen Schnittstellen Tabelle pro Prozess, sodass alle Aufrufe dieser Funktion in einem Prozess dieselbe Instanz zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4e001-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="4e001-108">Nachdem Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufgerufen haben, registrieren Sie die-Schnittstelle aus dem Apartment, in dem Sie sich befindet, mit einem Aufrufen der [**registerinterfaceinglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4e001-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="4e001-109">Diese Methode stellt ein Cookie bereit, das die-Schnittstelle und deren Position identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4e001-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="4e001-110">Ein Apartment, das einen Zeiger auf diese Schnittstelle sucht, ruft dann die [**getinterfacefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) -Methode mit diesem Cookie auf, und die Implementierung stellt dann einen Schnittstellen Zeiger auf das aufrufende Apartment bereit.</span><span class="sxs-lookup"><span data-stu-id="4e001-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="4e001-111">Um die globale Registrierung der Schnittstelle aufzuheben, kann jedes Apartment die [**revokeinterfacefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e001-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="4e001-112">Ein einfaches Beispiel für die Verwendung von [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) wäre, wenn Sie einen Schnittstellen Zeiger für ein Objekt in einem Single Thread-Apartment (STA) an einen Arbeits Thread in einem anderen Apartment übergeben möchten.</span><span class="sxs-lookup"><span data-stu-id="4e001-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="4e001-113">Anstatt Sie in einen Datenstrom zu Mars Hallen und den Datenstrom als Thread Parameter an den Arbeits Thread zu übergeben, ermöglicht **iglobalinterfaketable** lediglich das Übergeben eines Cookies.</span><span class="sxs-lookup"><span data-stu-id="4e001-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="4e001-114">Wenn Sie die Schnittstelle in der globalen Schnittstellen Tabelle registrieren, wird ein Cookie angezeigt, das Sie verwenden können, anstatt den tatsächlichen Zeiger zu übergeben (wenn Sie den Zeiger übergeben müssen), entweder an einen nicht-Methoden Parameter, der zu einem anderen Apartment (als Parameter für [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) durch " [**kreatethread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)") oder zu einem Prozess internen Speicher außerhalb des Apartment.</span><span class="sxs-lookup"><span data-stu-id="4e001-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="4e001-115">Vorsicht ist erforderlich, da durch die Verwendung von globalen Schnittstellen der Programmierer für das Verwalten von Problemen wie Racebedingungen und gegenseitiger Ausschluss, die mit dem gleichzeitigen Zugriff auf den globalen Zustand mehrerer Threads verknüpft sind, zusätzliche Belastung entstehen kann.</span><span class="sxs-lookup"><span data-stu-id="4e001-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="4e001-116">COM stellt eine Standard Implementierung der [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="4e001-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="4e001-117">Es wird dringend empfohlen, diese Standard Implementierung zu verwenden, da Sie eine komplette Thread sichere Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4e001-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e001-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e001-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e001-119">Verwendungszwecke der globalen Schnittstellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="4e001-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 