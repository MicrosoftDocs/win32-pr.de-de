---
description: Aufbauen von DirectShow-Filtern
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Aufbauen von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747072"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="f9d42-103">Aufbauen von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="f9d42-103">Building DirectShow Filters</span></span>

<span data-ttu-id="f9d42-104">Die DirectShow-Basisklassen werden zum Implementieren von DirectShow-Filtern empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f9d42-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="f9d42-105">Um mit den Basisklassen zu erstellen, führen Sie zusätzlich zu den unter [Einrichten der Buildumgebung](setting-up-the-build-environment.md)aufgeführten Schritten die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f9d42-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="f9d42-106">Erstellen Sie die Basisklassen Bibliothek, die sich in den Verzeichnis Beispielen \\ Multimedia \\ DirectShow \\ baseclasses unter dem SDK-Stammverzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="f9d42-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="f9d42-107">Es gibt zwei Versionen der Bibliothek: eine Verkaufsversion ("-Version. lib") und eine Debugversion ("straumbasd. lib").</span><span class="sxs-lookup"><span data-stu-id="f9d42-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="f9d42-108">Schließen Sie die Header Datei Streams. h ein.</span><span class="sxs-lookup"><span data-stu-id="f9d42-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="f9d42-109">Verwenden Sie die \_ \_ StdCall-Aufruf Konvention.</span><span class="sxs-lookup"><span data-stu-id="f9d42-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="f9d42-110">Verwenden Sie die Multithread-C-Lauf Zeit Bibliothek (Debug oder Retail).</span><span class="sxs-lookup"><span data-stu-id="f9d42-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="f9d42-111">Schließen Sie eine Definitionsdatei (. def) ein, mit der die DLL-Funktionen exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9d42-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="f9d42-112">Im folgenden finden Sie ein Beispiel für eine Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="f9d42-112">The following is an example of a definition file.</span></span> <span data-ttu-id="f9d42-113">Dabei wird davon ausgegangen, dass die Ausgabedatei MyFilter.dll benannt ist.</span><span class="sxs-lookup"><span data-stu-id="f9d42-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="f9d42-114">Verknüpfen Sie die folgenden lib-Dateien.</span><span class="sxs-lookup"><span data-stu-id="f9d42-114">Link to the following lib files.</span></span>

    |              |                                      |
    |--------------|--------------------------------------|
    | <span data-ttu-id="f9d42-115">Build Debuggen</span><span class="sxs-lookup"><span data-stu-id="f9d42-115">Debug Build</span></span>  | <span data-ttu-id="f9d42-116">"Straumbasd. lib", "msvcrtd. lib", "winmm. lib"</span><span class="sxs-lookup"><span data-stu-id="f9d42-116">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="f9d42-117">Retail-Build</span><span class="sxs-lookup"><span data-stu-id="f9d42-117">Retail Build</span></span> | <span data-ttu-id="f9d42-118">"Ermbase. lib", "Msvcrt. lib", "winmm. lib"</span><span class="sxs-lookup"><span data-stu-id="f9d42-118">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="f9d42-119">Wählen Sie die Option "Standardbibliotheken ignorieren" in den Linker-Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="f9d42-119">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="f9d42-120">Deklarieren Sie den DLL-Einstiegspunkt wie folgt im Quellcode:</span><span class="sxs-lookup"><span data-stu-id="f9d42-120">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="f9d42-121">Frühere Versionen</span><span class="sxs-lookup"><span data-stu-id="f9d42-121">Previous Versions</span></span>

<span data-ttu-id="f9d42-122">Für Versionen der Basisklassen Bibliothek vor DirectShow 9,0 müssen Sie auch die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="f9d42-122">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="f9d42-123">Definieren Sie für Debugbuilds das präprozessorflag Debuggen.</span><span class="sxs-lookup"><span data-stu-id="f9d42-123">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="f9d42-124">Dieser Schritt ist für die Version der Basisklassen Bibliothek, die in DirectShow 9,0 und höher verfügbar ist, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f9d42-124">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9d42-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9d42-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9d42-126">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="f9d42-126">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="f9d42-127">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="f9d42-127">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



