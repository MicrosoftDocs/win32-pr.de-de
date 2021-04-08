---
description: Eine Dynamic Link Library (dll) ist ein Modul, das Funktionen und Daten enthält, die von einem anderen Modul (Anwendung oder dll) verwendet werden können.
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Dynamic-Link-Bibliotheken (Dynamic Link Libraries)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753784"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="a250b-103">Dynamic-Link-Bibliotheken (Dynamic Link Libraries)</span><span class="sxs-lookup"><span data-stu-id="a250b-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="a250b-104">Eine *Dynamic Link Library* (dll) ist ein Modul, das Funktionen und Daten enthält, die von einem anderen Modul (Anwendung oder dll) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a250b-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="a250b-105">Eine DLL kann zwei Arten von Funktionen definieren: "exportiert" und "intern".</span><span class="sxs-lookup"><span data-stu-id="a250b-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="a250b-106">Die exportierten Funktionen sind für das Aufrufen durch andere Module sowie für das Aufrufen in der dll vorgesehen, in der Sie definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a250b-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="a250b-107">Interne Funktionen sollten in der Regel nur innerhalb der dll aufgerufen werden, in der Sie definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a250b-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="a250b-108">Obwohl eine DLL Daten exportieren kann, werden Ihre Daten im Allgemeinen nur von ihren Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a250b-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="a250b-109">Es ist jedoch nichts zu verhindern, dass ein anderes Modul diese Adresse liest oder schreibt.</span><span class="sxs-lookup"><span data-stu-id="a250b-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="a250b-110">DLLs bieten eine Möglichkeit, Anwendungen zu modularisieren, damit ihre Funktionalität leichter aktualisiert und wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a250b-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="a250b-111">DLLs helfen auch, den Arbeitsspeicher Aufwand zu reduzieren, wenn mehrere Anwendungen gleichzeitig dieselbe Funktionalität verwenden, denn obwohl jede Anwendung eine eigene Kopie der DLL-Daten erhält, verwenden die Anwendungen den DLL-Code gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="a250b-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="a250b-112">Die Windows-Anwendungsprogrammierschnittstelle (API) ist als ein Satz von DLLs implementiert, sodass jeder Prozess, der die Windows-API verwendet, dynamisches Verknüpfen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a250b-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="a250b-113">Informationen zu Dynamic-Link-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="a250b-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="a250b-114">Verwenden von Dynamic-Link-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="a250b-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="a250b-115">Dynamic Link Library-Referenz</span><span class="sxs-lookup"><span data-stu-id="a250b-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="a250b-116">Wenn ein Benutzer Probleme mit einer DLL auf Ihrem Computer hat, wenden Sie sich an den Kundensupport des Softwareanbieters, der die dll veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a250b-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="a250b-117">Wenn Sie der Meinung sind, dass Sie Unterstützung für ein Microsoft-Produkt (einschließlich Windows) benötigen, besuchen Sie unsere technische Support Website unter [Support.Microsoft.com](https://support.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a250b-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a250b-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a250b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a250b-119">DLLs (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="a250b-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
