---
title: Verwenden der Code Beispiele für das Windows Media-Format-SDK
description: Verwenden der Code Beispiele für das Windows Media-Format-SDK
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media-Format-SDK, Codebeispiele
- Windows Media-Format-SDK, Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391475"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="f8fb8-105">Verwenden der Code Beispiele für das Windows Media-Format-SDK</span><span class="sxs-lookup"><span data-stu-id="f8fb8-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="f8fb8-106">Viele der erläuternden Abschnitte dieses SDK enthalten Codebeispiele.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="f8fb8-107">Die Beispiele sind so klar und präzise wie möglich.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="f8fb8-108">Wenn Sie die Beispiele lesen, sollten Sie die folgenden Konventionen beachten.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="f8fb8-109">Bei allen Beispielen wird davon ausgegangen, dass Sie Windows. h und wmsdk. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="f8fb8-110">Alle anderen erforderlichen Header Dateien werden im erläuternden Text erwähnt.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="f8fb8-111">Die Fehlerüberprüfung wurde auf das Abbrechen der Funktion beschränkt, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="f8fb8-112">In einer Anwendung sollten Sie nach bestimmten Fehlercodes suchen und eine Art Fehlerberichterstattung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="f8fb8-113">Wenn Sie Rückgabewerte von Methoden oder Funktionen überprüfen, die einen **HRESULT** -Wert zurückgeben, sollten Sie das **failed** -Makro verwenden, um zu ermitteln, ob der Rückgabewert einen Fehler anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="f8fb8-114">Viele der Beispiele in dieser Dokumentation verwenden ein Makro mit dem Namen GoTo \_ Exit \_ \_ , wenn failed, das im folgenden Code definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="f8fb8-115">Diese Beispiel Funktionen verfügen jeweils über ein Tag mit dem Namen "Exit:", nach dem alle in der Funktion zugeordneten Schnittstellen und Arbeitsspeicher freigegeben werden und ggf. der Fehlercode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="f8fb8-116">Schnittstellen und Arbeitsspeicher werden in den Codebeispielen mithilfe von Makros namens sicheres \_ Release und sicheres Löschen von Arrays freigegeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f8fb8-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="f8fb8-117">Diese Makros sind im folgenden Code definiert:</span><span class="sxs-lookup"><span data-stu-id="f8fb8-117">These macros are defined in the following code:</span></span>
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   <span data-ttu-id="f8fb8-118">Häufig müssen Sie die Logik eines Beispiels in einem anderen Beispiel einschließen, damit das Beispiel sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="f8fb8-119">In diesen Fällen ist ein TODO-Kommentar mit einem Verweis auf das entsprechende Codebeispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="f8fb8-120">Damit der Code leichter lesbar ist, überprüft keines der Beispiel Funktionen in dieser Dokumentation seine Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="f8fb8-121">Wenn Sie eine dieser Funktionen in Ihren Code kopieren, sollten Sie alle Eingabeparameter überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f8fb8-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8fb8-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8fb8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8fb8-123">**Einstieg**</span><span class="sxs-lookup"><span data-stu-id="f8fb8-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




