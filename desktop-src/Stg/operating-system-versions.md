---
title: Betriebs System Versionen
description: Dieser DWORD-Datentyp sollte den Betriebs Systemtyp im hohen Bestell Wort und die Versionsnummer des Betriebssystems im nieder wertigen Wort enthalten. Mögliche Werte für das Betriebssystem sind in der folgenden Tabelle aufgeführt.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Strukturierte Speicherung von Betriebs System Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338070"
---
# <a name="operating-system-versions"></a><span data-ttu-id="b8a03-105">Betriebs System Versionen</span><span class="sxs-lookup"><span data-stu-id="b8a03-105">Operating System Versions</span></span>

<span data-ttu-id="b8a03-106">Dieser **DWORD** -Datentyp sollte den Betriebs Systemtyp im hohen Bestell Wort und die Versionsnummer des Betriebssystems im nieder wertigen Wort enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8a03-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="b8a03-107">Mögliche Werte für das Betriebssystem sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8a03-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="b8a03-108">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b8a03-108">Operating system</span></span>       | <span data-ttu-id="b8a03-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b8a03-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="b8a03-110">32-Bit-Windows (Win32)</span><span class="sxs-lookup"><span data-stu-id="b8a03-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="b8a03-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="b8a03-111">0x0002</span></span> |
| <span data-ttu-id="b8a03-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="b8a03-112">Macintosh</span></span>              | <span data-ttu-id="b8a03-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="b8a03-113">0x0001</span></span> |
| <span data-ttu-id="b8a03-114">16-Bit-Windows (Win16)</span><span class="sxs-lookup"><span data-stu-id="b8a03-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="b8a03-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="b8a03-115">0x0000</span></span> |



 

<span data-ttu-id="b8a03-116">Bei Microsoft Windows-Betriebssystemen ist die Betriebssystemversion das von der Funktion " [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) " zurückgegebene Wort mit niedriger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b8a03-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="b8a03-117">Im folgenden Beispielcode wird für Microsoft Windows die Version des Ursprungs Betriebssystems ordnungsgemäß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8a03-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 