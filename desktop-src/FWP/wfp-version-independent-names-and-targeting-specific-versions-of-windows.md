---
title: WFP-Version-Independent Namen und für bestimmte Versionen von Windows
description: In vielen Fällen stellt die Windows-Filter Plattform-API (WFP) mehr als eine Version einer Funktion oder Struktur bereit.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341218"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="82856-103">WFP-Version-Independent Namen und für bestimmte Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="82856-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="82856-104">In vielen Fällen stellt die Windows-Filter Plattform-API (WFP) mehr als eine Version einer Funktion oder Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="82856-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="82856-105">Die meisten Daten-und Funktionsnamen in der WFP-API enden mit einer Versionsnummer, z. b. "0" oder "1", auch wenn nur eine Version vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82856-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="82856-106">Versions Zuordnung in "f. h"</span><span class="sxs-lookup"><span data-stu-id="82856-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="82856-107">Die Header Datei "swpvi. h" ist ab dem Windows 7 SDK und dem WDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="82856-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="82856-108">Diese Header Datei ordnet den Namen der versionlosen API der Version zu, die für die Verwendung mit einem bestimmten Betriebssystem geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="82856-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="82856-109">Hier ist beispielsweise ein kurzer Auszug aus der Version von "f. h", die im Windows 8 SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="82856-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



<span data-ttu-id="82856-110">Wie oben gezeigt, gibt es nur eine Version von **fwpmneteventkreateenumhandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – daher wird jeder **fwpmneteventkreateenumhandle** -Befehl immer **FwpmNetEventCreateEnumHandle0** aufrufen, unabhängig vom Ziel des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="82856-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="82856-111">Es gibt jedoch drei Versionen von von " **f**", " [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)", " [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)" und " [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)".</span><span class="sxs-lookup"><span data-stu-id="82856-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="82856-112">Die Header Datei "fwpvi. h" stellt sicher, dass ein Aufrufen von **fwpmneteventerum** die Version aufruft, die für das Ziel Betriebssystem am besten geeignet ist:</span><span class="sxs-lookup"><span data-stu-id="82856-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="82856-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) für Windows 8 (oder höher)</span><span class="sxs-lookup"><span data-stu-id="82856-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="82856-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) für Windows 7 ist Ziel</span><span class="sxs-lookup"><span data-stu-id="82856-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="82856-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) für frühere Betriebssysteme (z. b. Windows Vista oder Windows Vista mit Service Pack 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="82856-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="82856-116">Aufrufen von Version-Independent-Funktionen und-Strukturen</span><span class="sxs-lookup"><span data-stu-id="82856-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="82856-117">Für WFP-Entwickler, die auf ein bestimmtes Betriebssystem oder eine WDK-Version abzielen, wird empfohlen, immer für Versions unabhängige Makros zu programmieren.</span><span class="sxs-lookup"><span data-stu-id="82856-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="82856-118">Dadurch wird automatisch die aktuellste Version ausgewählt, die im Ziel Betriebssystem unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="82856-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="82856-119">Die Verwendung der neuesten Header Dateien wird empfohlen, selbst wenn ein älteres Betriebssystem als Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82856-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="82856-120">Dadurch wird sichergestellt, dass die neueste unterstützte Version verwendet wird, und Sie können den Code leichter verwalten und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="82856-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="82856-121">In der [WFP-API-Referenz Dokumentation](fwp-reference.md) werden die einzelnen Versionen einer nummerierten API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82856-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="82856-122">Wenn mehr als eine Version vorhanden ist, wird das Ziel Betriebssystem notiert.</span><span class="sxs-lookup"><span data-stu-id="82856-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="82856-123">Entwickler möchten jedoch in der Regel die Versions unabhängigen (zahllosen) APIs aufzurufen und das Ziel Betriebssystem angeben (z. b. **ntddi \_ WIN6** für Windows Vista oder **ntddi \_ WIN8** für Windows 8).</span><span class="sxs-lookup"><span data-stu-id="82856-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="82856-124">Um die ordnungsgemäße Handhabung von Funktionen sicherzustellen, die verschiedene Parameter in verschiedenen Versionen verwenden, können Sie bedingte Blöcke wie einschließen `#if (NTDDI_VERSION >= NTDDI_WIN7)` .</span><span class="sxs-lookup"><span data-stu-id="82856-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




