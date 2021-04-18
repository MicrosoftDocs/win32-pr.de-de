---
description: In diesem Thema wird beschrieben, wie eine Komponente in Microsoft DirectShow als Dynamic Link Library (dll) implementiert wird.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: DLL-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344772"
---
# <a name="dll-functions"></a><span data-ttu-id="ef396-103">DLL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ef396-103">DLL Functions</span></span>

<span data-ttu-id="ef396-104">In diesem Thema wird beschrieben, wie eine Komponente in Microsoft DirectShow als Dynamic Link Library (dll) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="ef396-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="ef396-105">Eine DLL muss die folgenden Funktionen implementieren, damit Sie registriert, nicht registriert und in den Arbeitsspeicher geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef396-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="ef396-106">[*DllMain*](/windows/desktop/Dlls/dllmain): der DLL-Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="ef396-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="ef396-107">Der Name *DllMain* ist ein Platzhalter für den Namen der Bibliothek definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="ef396-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="ef396-108">Die DirectShow-Implementierung verwendet den Namen **DllEntryPoint**.</span><span class="sxs-lookup"><span data-stu-id="ef396-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="ef396-109">Weitere Informationen finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ef396-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="ef396-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): erstellt eine klassenfactoryinstanz.</span><span class="sxs-lookup"><span data-stu-id="ef396-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="ef396-111">Wird in den vorherigen Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef396-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="ef396-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): fragt ab, ob die DLL sicher entladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef396-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="ef396-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): erstellt Registrierungseinträge für die dll.</span><span class="sxs-lookup"><span data-stu-id="ef396-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="ef396-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): entfernt Registrierungseinträge für die dll.</span><span class="sxs-lookup"><span data-stu-id="ef396-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="ef396-115">Die ersten drei werden von DirectShow implementiert.</span><span class="sxs-lookup"><span data-stu-id="ef396-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="ef396-116">Wenn Ihre Factoryvorlage eine Initialisierungsfunktion in der [**m \_ lpfninit**](cfactorytemplate-m-lpfninit.md) -Element Variablen bereitstellt, wird diese Funktion innerhalb der DLL-Einstiegspunkt Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ef396-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="ef396-117">Weitere Informationen dazu, wann das System die DLL-Einstiegspunkt Funktion aufruft, finden Sie unter [*DllMain*](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="ef396-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="ef396-118">Sie müssen [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)implementieren, aber DirectShow bietet eine Funktion mit dem Namen [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) , die die erforderliche Arbeit erledigt.</span><span class="sxs-lookup"><span data-stu-id="ef396-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="ef396-119">Die Komponente kann diese Funktion einfach einschließen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ef396-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="ef396-120">Allerdings können Sie in [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) den Registrierungsprozess nach Bedarf anpassen.</span><span class="sxs-lookup"><span data-stu-id="ef396-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="ef396-121">Wenn Ihre DLL einen Filter enthält, müssen Sie möglicherweise zusätzliche Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef396-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="ef396-122">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ef396-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="ef396-123">Exportieren Sie in der Modul Definitionsdatei (. def) alle DLL-Funktionen mit Ausnahme der Einstiegspunkt Funktion.</span><span class="sxs-lookup"><span data-stu-id="ef396-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="ef396-124">Im folgenden finden Sie eine Beispieldatei für die DEF-Datei:</span><span class="sxs-lookup"><span data-stu-id="ef396-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="ef396-125">Sie können die DLL mit dem Regsvr32.exe-Hilfsprogramm registrieren.</span><span class="sxs-lookup"><span data-stu-id="ef396-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef396-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef396-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef396-127">Erstellen einer DirectShow-Filter-dll</span><span class="sxs-lookup"><span data-stu-id="ef396-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
