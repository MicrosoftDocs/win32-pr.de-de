---
description: Weitere Informationen finden Sie im Artikel zu Extensible Storage Engine-Fehlern.
title: Erweiterbare Speicher-Engine-Fehler
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868967"
---
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="5b822-103">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="5b822-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="5b822-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5b822-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="5b822-105">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="5b822-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="5b822-106">Alle möglichen Fehler, die von der ESE-API (Extensible Storage Engine) zurückgegeben werden, werden durch den [JET_ERR](./jet-err.md) -Datentyp definiert.</span><span class="sxs-lookup"><span data-stu-id="5b822-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="5b822-107">Eine Liste der Fehlerflags, die für diese API definiert sind, finden Sie unter [Fehler Codes der Extensible Storage Engine](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b822-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="5b822-108">In der gesamten ESE-API-Dokumentation werden nur die wichtigsten Fehler dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="5b822-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="5b822-109">Diese Fehlerstellen in der Regel API-Verwendungs Fehler oder sehr wichtige Fehlerbedingungen dar.</span><span class="sxs-lookup"><span data-stu-id="5b822-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="5b822-110">Beachten Sie, dass jede dieser ESE-APIs auch andere Fehler zurückgeben kann, die für jede API nicht dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="5b822-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="5b822-111">In diesen Fällen sollte der Aufrufer einfach den Fehler behandeln, wie bei jedem anderen Fehler, der von der API zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b822-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="5b822-112">Der spezifische Fehlerwert kann dann zu Diagnose Zwecken wie der Ablauf Verfolgung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b822-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="5b822-113">Im Allgemeinen sollte ein Wert, der größer als 0 (null) ist, als Warnung interpretiert werden. der Wert 0 (null) sollte als Success interpretiert werden, und ein Wert, der kleiner als 0 (null) ist, sollte als Fehler interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="5b822-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="5b822-114">Keine anderen Muster in diesen Werten (z. b. Wertebereiche) sollten von einer Anwendung abhängig sein.</span><span class="sxs-lookup"><span data-stu-id="5b822-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="5b822-115">Wenn ESE auf einige der schwerwiegenderen Fehler stößt, wird ein Ereignisprotokoll Eintrag erstellt, der Details zu den Fehlern enthält.</span><span class="sxs-lookup"><span data-stu-id="5b822-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="5b822-116">Die Protokollierungsebene kann durch [Ereignisprotokoll Parameter](./event-log-parameters.md)gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="5b822-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="5b822-117">Für einige Anwendungen ist es erforderlich, dass [JET_ERR](./jet-err.md)s als HRESULTs zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b822-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="5b822-118">Im folgenden C++ Beispiel wird gezeigt, wie Sie diese Konvertierung vornehmen:</span><span class="sxs-lookup"><span data-stu-id="5b822-118">The following C++ example shows how to make that conversion:</span></span>

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

<span data-ttu-id="5b822-119">Weitere Informationen zum Konfigurieren von Systemparametern für die Fehlerbehandlung finden Sie unter Parameter für die [Fehlerbehandlung](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5b822-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="5b822-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5b822-120">See Also</span></span>

[<span data-ttu-id="5b822-121">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="5b822-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="5b822-122">Fehler Codes für erweiterbare Speicher-Engine</span><span class="sxs-lookup"><span data-stu-id="5b822-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="5b822-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5b822-123">JET_ERR</span></span>](./jet-err.md)
