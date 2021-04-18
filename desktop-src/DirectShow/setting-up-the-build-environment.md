---
description: Entwickeln von DirectShow-Anwendungen
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Entwickeln von DirectShow-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338850"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="e7548-103">Entwickeln von DirectShow-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e7548-103">Building DirectShow Applications</span></span>

<span data-ttu-id="e7548-104">In diesem Thema werden die Header und Bibliotheken beschrieben, die zum Erstellen von DirectShow-Anwendungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e7548-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="e7548-105">Die neuesten DirectShow-Header und-Bibliotheken sind im [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7548-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="e7548-106">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e7548-106">Header Files</span></span>

<span data-ttu-id="e7548-107">Alle DirectShow-Anwendungen verwenden die in der folgenden Tabelle gezeigte Header Datei.</span><span class="sxs-lookup"><span data-stu-id="e7548-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="e7548-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e7548-108">Header File</span></span> | <span data-ttu-id="e7548-109">Erforderlich für</span><span class="sxs-lookup"><span data-stu-id="e7548-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="e7548-110">DShow. h</span><span class="sxs-lookup"><span data-stu-id="e7548-110">Dshow.h</span></span>     | <span data-ttu-id="e7548-111">Alle DirectShow-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e7548-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="e7548-112">Einige DirectShow-Schnittstellen erfordern zusätzliche Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="e7548-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="e7548-113">Diese Anforderungen sind in der Schnittstellenreferenz aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7548-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="e7548-114">Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="e7548-114">Library Files</span></span>

<span data-ttu-id="e7548-115">DirectShow verwendet die statischen Bibliotheksdateien, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e7548-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="e7548-116">Bibliotheksdatei</span><span class="sxs-lookup"><span data-stu-id="e7548-116">Library File</span></span> | <span data-ttu-id="e7548-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7548-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7548-118">"" "" ". Lib"</span><span class="sxs-lookup"><span data-stu-id="e7548-118">Strmiids.lib</span></span> | <span data-ttu-id="e7548-119">Exportiert Klassen Bezeichner (CLSIDs) und Schnittstellen Bezeichner (IIDs).</span><span class="sxs-lookup"><span data-stu-id="e7548-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="e7548-120">Quarz. lib</span><span class="sxs-lookup"><span data-stu-id="e7548-120">Quartz.lib</span></span>   | <span data-ttu-id="e7548-121">Exportiert die [**amgeterrortext**](/windows/win32/api/errors/nf-errors-amgeterrortexta) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e7548-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="e7548-122">Wenn Sie diese Funktion nicht aufzurufen, ist diese Bibliothek nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e7548-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="e7548-123">Verwenden Sie die gleichen lib-Dateien für Debug-und Releasebuilds.</span><span class="sxs-lookup"><span data-stu-id="e7548-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="e7548-124">Filtern von Basisklassen</span><span class="sxs-lookup"><span data-stu-id="e7548-124">Filter Base Classes</span></span>

<span data-ttu-id="e7548-125">Der Windows SDK stellt eine Reihe von C++-Klassen bereit, die empfohlen werden, wenn Sie einen benutzerdefinierten DirectShow-Filter schreiben.</span><span class="sxs-lookup"><span data-stu-id="e7548-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="e7548-126">Diese Klassen werden als Beispielcode bereitgestellt, der in einer statischen Bibliothek kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7548-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="e7548-127">Weitere Informationen finden Sie unter [DirectShow-Basisklassen](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="e7548-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="e7548-128">Verteilbare DLLs</span><span class="sxs-lookup"><span data-stu-id="e7548-128">Redistributable DLLs</span></span>

<span data-ttu-id="e7548-129">Für DirectShow-Anwendungen, die für Windows XP mit Service Pack 2 (SP2) und höher geschrieben wurden, müssen keine DirectShow-DLLs neu verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="e7548-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="e7548-130">Für Windows XP mit Service Pack 1 (SP1) und früher sind verteilbare DirectShow-DLLs über das Microsoft DirectX SDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7548-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="e7548-131">Die neueste Version dieser DLLs ist Version 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="e7548-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="e7548-132">Es ist keine weitere Entwicklung dieser verteilbaren DLLs geplant.</span><span class="sxs-lookup"><span data-stu-id="e7548-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="e7548-133">Windows XP mit Service Pack 2 (SP2) enthält die c-DLLs der Version 9.0.</span><span class="sxs-lookup"><span data-stu-id="e7548-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="e7548-134">Die redstributable-Pakete enthalten die folgenden DLLs:</span><span class="sxs-lookup"><span data-stu-id="e7548-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="e7548-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="e7548-135">dxnt.cab</span></span>
    -   <span data-ttu-id="e7548-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-136">amstream.dll</span></span>
    -   <span data-ttu-id="e7548-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-137">devenum.dll</span></span>
    -   <span data-ttu-id="e7548-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-138">encapi.dll</span></span>
    -   <span data-ttu-id="e7548-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-139">ks.sys</span></span>
    -   <span data-ttu-id="e7548-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-140">ksolay.ax</span></span>
    -   <span data-ttu-id="e7548-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="e7548-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-142">ksuser.dll</span></span>
    -   <span data-ttu-id="e7548-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="e7548-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="e7548-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="e7548-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-146">msdmo.dll</span></span>
    -   <span data-ttu-id="e7548-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="e7548-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-148">mspclock.sys</span></span>
    -   <span data-ttu-id="e7548-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-149">mspqm.sys</span></span>
    -   <span data-ttu-id="e7548-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-150">mstee.sys</span></span>
    -   <span data-ttu-id="e7548-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="e7548-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-152">qasf.dll</span></span>
    -   <span data-ttu-id="e7548-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-153">qcap.dll</span></span>
    -   <span data-ttu-id="e7548-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-154">qdv.dll</span></span>
    -   <span data-ttu-id="e7548-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-155">qdvd.dll</span></span>
    -   <span data-ttu-id="e7548-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-156">qedit.dll</span></span>
    -   <span data-ttu-id="e7548-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="e7548-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-158">quartz.dll</span></span>
    -   <span data-ttu-id="e7548-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-159">stream.sys</span></span>
    -   <span data-ttu-id="e7548-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-160">swenum.sys</span></span>
-   <span data-ttu-id="e7548-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="e7548-161">bda.cab</span></span>
    -   <span data-ttu-id="e7548-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="e7548-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-163">bdasup.sys</span></span>
    -   <span data-ttu-id="e7548-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="e7548-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-165">ipsink.ax</span></span>
    -   <span data-ttu-id="e7548-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="e7548-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="e7548-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="e7548-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-169">mpe.sys</span></span>
    -   <span data-ttu-id="e7548-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="e7548-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-171">msdv.sys</span></span>
    -   <span data-ttu-id="e7548-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="e7548-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="e7548-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-174">msyuv.dll</span></span>
    -   <span data-ttu-id="e7548-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="e7548-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-176">ndisip.sys</span></span>
    -   <span data-ttu-id="e7548-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="e7548-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="e7548-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-179">slip.sys</span></span>
    -   <span data-ttu-id="e7548-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-180">streamip.sys</span></span>
    -   <span data-ttu-id="e7548-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="e7548-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="e7548-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="e7548-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="e7548-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="e7548-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7548-184">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7548-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7548-185">Aufbauen von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="e7548-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 
