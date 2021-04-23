---
description: Erstellen von DirectShow-Filtern
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Erstellen von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7090eed702b1abe8ee863d5fa3ac9c1fd413690e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908618"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="458a1-103">Erstellen von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="458a1-103">Building DirectShow Filters</span></span>

<span data-ttu-id="458a1-104">Die DirectShow-Basisklassen werden für die Implementierung von DirectShow-Filtern empfohlen.</span><span class="sxs-lookup"><span data-stu-id="458a1-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="458a1-105">Führen Sie zum Erstellen mit den Basisklassen zusätzlich zu den unter Einrichten der [Buildumgebung](setting-up-the-build-environment.md)aufgeführten Schritten die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="458a1-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="458a1-106">Erstellen Sie die Basisklassenbibliothek im Verzeichnis Samples \\ Multimedia \\ DirectShow \\ BaseClasses unter dem SDK-Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="458a1-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="458a1-107">Es gibt zwei Versionen der Bibliothek: eine Verkaufsversion (Strmbase.lib) und eine Debugversion (Strmbasd.lib).</span><span class="sxs-lookup"><span data-stu-id="458a1-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="458a1-108">Schließen Sie die Headerdatei Streams.h ein.</span><span class="sxs-lookup"><span data-stu-id="458a1-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="458a1-109">Verwenden Sie die \_ \_ Stdcall-Aufrufkonvention.</span><span class="sxs-lookup"><span data-stu-id="458a1-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="458a1-110">Verwenden Sie die Multithread-C-Laufzeitbibliothek (debuggen oder retail, je nach Bedarf).</span><span class="sxs-lookup"><span data-stu-id="458a1-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="458a1-111">Schließen Sie eine Definitionsdatei (DEF-Datei) ein, die die DLL-Funktionen exportiert.</span><span class="sxs-lookup"><span data-stu-id="458a1-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="458a1-112">Im Folgenden wird ein Beispiel für eine Definitionsdatei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="458a1-112">The following is an example of a definition file.</span></span> <span data-ttu-id="458a1-113">Es wird davon ausgegangen, dass die Ausgabedatei MyFilter.dll heißt.</span><span class="sxs-lookup"><span data-stu-id="458a1-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="458a1-114">Link zu den folgenden Bibliothekendateien.</span><span class="sxs-lookup"><span data-stu-id="458a1-114">Link to the following lib files.</span></span>

| <span data-ttu-id="458a1-115">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="458a1-115">Label</span></span> | <span data-ttu-id="458a1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="458a1-116">Value</span></span> |
    |--------------|--------------------------------------|
    | <span data-ttu-id="458a1-117">Debugbuild</span><span class="sxs-lookup"><span data-stu-id="458a1-117">Debug Build</span></span>  | <span data-ttu-id="458a1-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span><span class="sxs-lookup"><span data-stu-id="458a1-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="458a1-119">Retail Build</span><span class="sxs-lookup"><span data-stu-id="458a1-119">Retail Build</span></span> | <span data-ttu-id="458a1-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span><span class="sxs-lookup"><span data-stu-id="458a1-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="458a1-121">Wählen Sie in den Linkereinstellungen die Option "Standardbibliotheken ignorieren" aus.</span><span class="sxs-lookup"><span data-stu-id="458a1-121">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="458a1-122">Deklarieren Sie den DLL-Einstiegspunkt im Quellcode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="458a1-122">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="458a1-123">Frühere Versionen</span><span class="sxs-lookup"><span data-stu-id="458a1-123">Previous Versions</span></span>

<span data-ttu-id="458a1-124">Für Versionen der Basisklassenbibliothek vor DirectShow 9.0 müssen Sie auch folgende Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="458a1-124">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="458a1-125">Definieren Sie für Debugbuilds das Präprozessorflag DEBUG.</span><span class="sxs-lookup"><span data-stu-id="458a1-125">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="458a1-126">Dieser Schritt ist für die Version der Basisklassenbibliothek, die in DirectShow 9.0 und höher verfügbar ist, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="458a1-126">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="458a1-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="458a1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="458a1-128">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="458a1-128">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="458a1-129">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="458a1-129">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



