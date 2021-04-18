---
description: Damit eine Anwendung ordnungsgemäß ausgeführt werden kann, müssen die entsprechenden DLLs auf dem Host Computer installiert sein. Diese DLLs können entweder vom Betriebssystem oder vom verteilbaren Paket der Anwendung bereitgestellt werden.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Verknüpfen statischer und dynamischer Bibliotheken (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338899"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="6b87f-104">Verknüpfen statischer und dynamischer Bibliotheken (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="6b87f-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="6b87f-105">Damit eine Anwendung ordnungsgemäß ausgeführt werden kann, müssen die entsprechenden DLLs auf dem Host Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="6b87f-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="6b87f-106">Diese DLLs können entweder vom Betriebssystem oder vom verteilbaren Paket der Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="6b87f-107">Bibliotheken laden geeignete DLLs</span><span class="sxs-lookup"><span data-stu-id="6b87f-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="6b87f-108">Die Bibliotheken, die im DirectX SDK enthalten sind, laden die richtigen DLLs zur Laufzeit automatisch.</span><span class="sxs-lookup"><span data-stu-id="6b87f-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="6b87f-109">Die Ausnahme von dieser Regel ist d3dx10. lib/d3dx10d. lib, mit der die d3dx10.dll geladen wird, die mit dieser Version des SDK ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="6b87f-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="6b87f-110">Wenn das heruntergeladene SDK beispielsweise d3dx10 \_33.dll und d3dx10 \_34.dll enthält, wird die Bibliothek (d3dx10. lib), die mit diesem SDK ausgeliefert wurde, d3dx10 \_34.dll laden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="6b87f-111">Wenn ein nachfolgendes SDK später installiert wird \_ , das d3dx10 35. lib enthält, wird die Datei "d3dx10. lib" aus dem vorherigen SDK weiterhin d3dx10 \_34.dll geladen.</span><span class="sxs-lookup"><span data-stu-id="6b87f-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="6b87f-112">Der d3dx10. lib-Eintrag aus dem neueren SDK lädt d3dx10 \_35.dll.</span><span class="sxs-lookup"><span data-stu-id="6b87f-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="6b87f-113">Neuverteilen von Binärdateien</span><span class="sxs-lookup"><span data-stu-id="6b87f-113">Redistributing Binaries</span></span>

<span data-ttu-id="6b87f-114">Nur d3dx10.dll (und nachfolgende Versionen der gleichen Datei) können neu verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="6b87f-115">Zum erneuten Verteilen dieser Datei müssen Sie die **directxsetup** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="6b87f-116">Ausführliche Informationen zur Verwendung dieser Funktion und zum Verbinden eines verteilbaren Pakets finden Sie unter [Installieren von DirectX mit DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="6b87f-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="6b87f-117">Alle anderen erforderlichen Binärdateien sind in Windows Vista enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b87f-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="6b87f-118">Die einzigen Binärdateien, die neu verteilt werden können, sind die, die sich im folgenden Verzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="6b87f-119">In der folgenden Tabelle werden die Binärdateien beschrieben, die Entwicklern bekannt sein sollten.</span><span class="sxs-lookup"><span data-stu-id="6b87f-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="6b87f-120">Direct3D 10-Binärdateien</span><span class="sxs-lookup"><span data-stu-id="6b87f-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="6b87f-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b87f-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b87f-122">d3dx10.dll/d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="6b87f-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="6b87f-123">Einzelhandel und Debuggen d3dx10 Komponenten; die Einzelhandels Komponenten können im Redist-CAB neu verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6b87f-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="6b87f-124">d3d10ref.dll</span></span>           | <span data-ttu-id="6b87f-125">Verweis Raster.</span><span class="sxs-lookup"><span data-stu-id="6b87f-125">Reference Rasterizer.</span></span> <span data-ttu-id="6b87f-126">Stellt die Software Implementierung der Grafik Pipeline bereit.</span><span class="sxs-lookup"><span data-stu-id="6b87f-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="6b87f-127">Nur als Teil des DirectX SDK für Windows SDK oder Legacy enthalten und kann nicht weiter verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="6b87f-128">Der Verweis Raster dient nur zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="6b87f-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="6b87f-129">Explizites verknüpfen ist nicht erforderlich. Wenn Sie versuchen, ein Referenzgerät zu erstellen (siehe [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)), wird diese DLL geladen, sofern Sie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6b87f-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="6b87f-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="6b87f-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="6b87f-131">Eine Reihe von SDK-Hilfsprogrammen, die als Schicht zwischen API-aufrufen und Lauf Zeit Ausführung fungieren, einschließlich der [Debug-Ebene](d3d10-graphics-programming-guide-api-features-layers.md) und der Switch-to-Reference-Schicht.</span><span class="sxs-lookup"><span data-stu-id="6b87f-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="6b87f-132">Explizites verknüpfen ist nicht erforderlich. Wenn ein Gerät mit dem entsprechenden ebenenflag erstellt wird, wird diese DLL automatisch geladen.</span><span class="sxs-lookup"><span data-stu-id="6b87f-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="6b87f-133">Diese Komponente ist nur für Entwicklungs-und Debugzwecke gedacht.</span><span class="sxs-lookup"><span data-stu-id="6b87f-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="6b87f-134">Nur als Teil des DirectX SDK für Windows SDK oder Legacy enthalten und kann nicht weiter verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6b87f-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6b87f-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b87f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b87f-136">Programmier Handbuch für Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="6b87f-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6b87f-137">Direct3D 10-Grafiken</span><span class="sxs-lookup"><span data-stu-id="6b87f-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



