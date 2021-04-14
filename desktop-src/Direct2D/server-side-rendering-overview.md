---
title: Verwenden von Direct2D zum Server-Side Rendering
description: Beschreibt die Verwendung von Direct2D für serverseitiges Rendering.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, serverseitiges Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390438"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="c37c3-104">Verwenden von Direct2D zum Server-Side Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="c37c3-105">Direct2D eignet sich gut für Grafikanwendungen, die serverseitiges Rendering auf Windows Server erfordern.</span><span class="sxs-lookup"><span data-stu-id="c37c3-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="c37c3-106">In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D für serverseitiges Rendering beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c37c3-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="c37c3-107">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c37c3-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="c37c3-108">Anforderungen für Server-Side Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="c37c3-109">Optionen für verfügbare APIs</span><span class="sxs-lookup"><span data-stu-id="c37c3-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="c37c3-110">GDI</span><span class="sxs-lookup"><span data-stu-id="c37c3-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="c37c3-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="c37c3-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="c37c3-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="c37c3-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="c37c3-113">Verwenden von Direct2D zum Server-Side Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="c37c3-114">Software Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="c37c3-115">Multithreading</span><span class="sxs-lookup"><span data-stu-id="c37c3-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="c37c3-116">Erstellen einer Bitmapdatei</span><span class="sxs-lookup"><span data-stu-id="c37c3-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="c37c3-117">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c37c3-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="c37c3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c37c3-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="c37c3-119">Anforderungen für Server-Side Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="c37c3-120">Im folgenden finden Sie ein typisches Szenario für einen Diagramm Server: Diagramme und Grafiken werden auf einem Server gerendert und als Bitmaps in Reaktion auf Webanforderungen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="c37c3-121">Der Server ist möglicherweise mit einer Low-End-Grafikkarte oder einer Grafikkarte ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="c37c3-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="c37c3-122">In diesem Szenario werden drei Anwendungsanforderungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="c37c3-123">Zuerst muss die Anwendung mehrere gleichzeitige Anforderungen effizient verarbeiten, insbesondere auf multikernservern.</span><span class="sxs-lookup"><span data-stu-id="c37c3-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="c37c3-124">Zweitens muss die Anwendung das Software Rendering bei der Ausführung auf Servern mit einer Low-End-Grafikkarte oder einer Grafikkarte verwenden.</span><span class="sxs-lookup"><span data-stu-id="c37c3-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="c37c3-125">Schließlich muss die Anwendung als Dienst in Sitzung 0 ausgeführt werden, damit kein Benutzer angemeldet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c37c3-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="c37c3-126">Weitere Informationen zu Sitzung 0 finden Sie unter [Auswirkung der Sitzung 0-Isolation auf Dienste und Treiber in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span><span class="sxs-lookup"><span data-stu-id="c37c3-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="c37c3-127">Optionen für verfügbare APIs</span><span class="sxs-lookup"><span data-stu-id="c37c3-127">Options for Available APIs</span></span>

<span data-ttu-id="c37c3-128">Es gibt drei Optionen für serverseitiges Rendering: GDI, GDI+ und Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c37c3-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="c37c3-129">Wie GDI und GDI+ ist Direct2D eine native 2D-Rendering-API, mit der Anwendungen mehr Kontrolle über die Verwendung von Grafik Geräten erhalten.</span><span class="sxs-lookup"><span data-stu-id="c37c3-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="c37c3-130">Außerdem unterstützt Direct2D eindeutig einen Single Thread und eine Multithread-Factory.</span><span class="sxs-lookup"><span data-stu-id="c37c3-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="c37c3-131">In den folgenden Abschnitten wird jede API in Bezug auf Zeichnungs Qualitäten und serverseitiges Multithread-Rendering verglichen.</span><span class="sxs-lookup"><span data-stu-id="c37c3-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="c37c3-132">GDI</span><span class="sxs-lookup"><span data-stu-id="c37c3-132">GDI</span></span>

<span data-ttu-id="c37c3-133">Im Gegensatz zu Direct2D und GDI+ unterstützt GDI keine hochwertigen Zeichnungs Features.</span><span class="sxs-lookup"><span data-stu-id="c37c3-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="c37c3-134">Beispielsweise unterstützt GDI keine Antialiasing zum Erstellen von Smooth Lines und bietet nur eingeschränkte Unterstützung für Transparenz.</span><span class="sxs-lookup"><span data-stu-id="c37c3-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="c37c3-135">Basierend auf den Ergebnissen der Grafik Leistungstests unter Windows 7 und Windows Server 2008 R2 skaliert Direct2D effizienter als GDI, trotz der Umgestaltung der Sperren in GDI.</span><span class="sxs-lookup"><span data-stu-id="c37c3-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="c37c3-136">Weitere Informationen zu diesen Testergebnissen finden Sie unter [Engineering Windows 7 graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span><span class="sxs-lookup"><span data-stu-id="c37c3-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="c37c3-137">Außerdem sind Anwendungen, die GDI verwenden, auf 10240 GDI-Handles pro Prozess und 65536 GDI-Handles pro Sitzung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="c37c3-138">Der Grund hierfür ist, dass intern in Windows ein 16-Bit-Wort verwendet wird, um den Index von Handles für jede Sitzung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c37c3-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="c37c3-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="c37c3-139">GDI+</span></span>

<span data-ttu-id="c37c3-140">Obwohl GDI+ Antialiasing und Alpha Blending für qualitativ hochwertige Zeichnungen unterstützt, besteht das Hauptproblem mit GDI+ für Server Szenarien darin, dass die Ausführung in Sitzung 0 nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c37c3-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="c37c3-141">Da Sitzung 0 nur nicht interaktive Funktionen unterstützt, erhalten Funktionen, die direkt oder indirekt mit Anzeigegeräten interagieren, Fehler.</span><span class="sxs-lookup"><span data-stu-id="c37c3-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="c37c3-142">Bestimmte Beispiele für Funktionen umfassen nicht nur diejenigen, die mit Anzeigegeräten arbeiten, sondern auch diejenigen, die indirekt mit Gerätetreibern arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c37c3-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="c37c3-143">Ähnlich wie bei GDI ist GDI+ durch seinen Sperrmechanismus eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="c37c3-144">Die Sperrmechanismen in GDI+ sind in Windows 7 und Windows Server 2008 R2 identisch, wie in früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="c37c3-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="c37c3-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="c37c3-145">Direct2D</span></span>

<span data-ttu-id="c37c3-146">Bei Direct2D handelt es sich um eine hardwarebeschleunigte, 2D-Grafik-API, die leistungsstarke und qualitativ hochwertige Rendering bietet.</span><span class="sxs-lookup"><span data-stu-id="c37c3-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="c37c3-147">Er bietet eine Single Thread-und Multithread Factory sowie die Lineare Skalierung des Kurs orientierten Software Rendering.</span><span class="sxs-lookup"><span data-stu-id="c37c3-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="c37c3-148">Zu diesem Zweck definiert Direct2D eine root Factory-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c37c3-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="c37c3-149">Als Regel kann ein Objekt, das auf einer Factory erstellt wird, nur mit anderen Objekten verwendet werden, die aus derselben Factory erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c37c3-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="c37c3-150">Der Aufrufer kann bei der Erstellung entweder eine Single Thread-oder eine Multithread-Factory anfordern.</span><span class="sxs-lookup"><span data-stu-id="c37c3-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="c37c3-151">Wenn eine Single Thread Factory angefordert wird, wird kein Sperren von Threads ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="c37c3-152">Wenn der Aufrufer eine multithreadfactory anfordert, wird immer dann eine Werks weite Thread Sperre eingerichtet, wenn ein Aufruf in Direct2D erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="c37c3-153">Außerdem ist das Sperren von Threads in Direct2D präziser als in GDI und GDI+, sodass sich die Anzahl der Threads nur minimal auf die Leistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="c37c3-154">Verwenden von Direct2D zum Server-Side Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="c37c3-155">In den folgenden Abschnitten wird beschrieben, wie Sie das Software Rendering verwenden, eine Single Thread-und eine Multithread-Factory optimal verwenden und eine komplexe Zeichnung in einer Datei zeichnen und speichern.</span><span class="sxs-lookup"><span data-stu-id="c37c3-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="c37c3-156">Software Rendering</span><span class="sxs-lookup"><span data-stu-id="c37c3-156">Software Rendering</span></span>

<span data-ttu-id="c37c3-157">Server seitige Anwendungen verwenden das Software Rendering durch Erstellen des [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -Renderziels, wobei der renderzieltyp entweder auf D2D1 \_ Rendering \_ Target \_ Type \_ Software oder D2D1 \_ renderzieltyp \_ \_ \_ Default festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c37c3-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="c37c3-158">Weitere Informationen zu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -renderzielen finden Sie unter der [**ID2D1Factory:: samatewicbitmaprendertarget**](id2d1factory-createwicbitmaprendertarget.md) -Methode. Weitere Informationen zu den renderzieltypen finden Sie unter [**D2D1 \_ Rendering \_ Target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span><span class="sxs-lookup"><span data-stu-id="c37c3-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="c37c3-159">Multithreading</span><span class="sxs-lookup"><span data-stu-id="c37c3-159">Multithreading</span></span>

<span data-ttu-id="c37c3-160">Wenn Sie wissen, wie Factorys erstellt und freigegeben werden, kann die Leistung einer Anwendung erheblich beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c37c3-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="c37c3-161">Die folgenden drei Abbildungen zeigen drei verschiedene Ansätze.</span><span class="sxs-lookup"><span data-stu-id="c37c3-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="c37c3-162">Der optimale Ansatz ist in Abbildung 3 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-162">The optimal approach is shown in figure 3.</span></span>

![Direct2D Multithreading-Diagramm mit einem einzelnen Renderziel.](images/server-side-rendering-1.png)

<span data-ttu-id="c37c3-164">In Abbildung 1 verwenden verschiedene Threads dieselbe Factory und dasselbe Renderziel.</span><span class="sxs-lookup"><span data-stu-id="c37c3-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="c37c3-165">Diese Vorgehensweise kann zu unvorhersehbaren Ergebnissen in Fällen führen, in denen mehrere Threads gleichzeitig den Status des freigegebenen Renderziels ändern, z. b. das gleichzeitige Festlegen der Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="c37c3-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="c37c3-166">Da bei der internen Sperrung in Direct2D keine freigegebene Ressource wie Renderziele synchronisiert wird, kann dieser Ansatz dazu führen, dass der [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Befehl in Thread 1 fehlschlägt, da der **beginDraw** -Befehl in Thread 2 bereits das freigegebene Renderziel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c37c3-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![Direct2D Multithreading-Diagramm mit mehreren renderzielen.](images/server-side-rendering-2.png)

<span data-ttu-id="c37c3-168">Um die in Abbildung 1 gefundenen unvorhersehbaren Ergebnisse zu vermeiden, zeigt Abbildung 2 eine multithreadfactory, bei der jeder Thread über ein eigenes Renderziel verfügt.</span><span class="sxs-lookup"><span data-stu-id="c37c3-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="c37c3-169">Diese Vorgehensweise funktioniert, aber Sie fungiert effektiv als Single Thread-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c37c3-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="c37c3-170">Der Grund hierfür ist, dass die Sperre für die Werks weite nur für die Zeichnungs Vorgangs Ebene gilt und dass alle Zeichnungs Aufrufe in derselben Factory serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c37c3-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="c37c3-171">Infolgedessen wird Thread 1 blockiert, wenn versucht wird, einen Zeichnungs Befehl einzugeben, während Thread 2 in der Mitte der Ausführung eines weiteren Zeichnungs Aufrufes ist.</span><span class="sxs-lookup"><span data-stu-id="c37c3-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![Direct2D Multithreading-Diagramm mit mehreren Factorys und mehreren Renderingzielen.](images/server-side-rendering-3.png)

<span data-ttu-id="c37c3-173">Abbildung 3 zeigt den optimalen Ansatz, bei dem eine Single Thread Factory und ein Single Thread-Renderziel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c37c3-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="c37c3-174">Da bei der Verwendung einer Single Thread Factory keine Sperre ausgeführt wird, können Zeichnungsvorgänge in jedem Thread gleichzeitig ausgeführt werden, um eine optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c37c3-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="c37c3-175">Erstellen einer Bitmapdatei</span><span class="sxs-lookup"><span data-stu-id="c37c3-175">Generating a Bitmap File</span></span>

<span data-ttu-id="c37c3-176">Verwenden Sie zum Generieren einer Bitmapdatei mit dem Software Rendering ein [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -Renderziel.</span><span class="sxs-lookup"><span data-stu-id="c37c3-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="c37c3-177">Verwenden Sie einen [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) , um die Bitmap in eine Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c37c3-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="c37c3-178">Verwenden Sie [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) , um die Bitmap in ein bestimmtes Bildformat zu codieren.</span><span class="sxs-lookup"><span data-stu-id="c37c3-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="c37c3-179">Im folgenden Codebeispiel wird gezeigt, wie das folgende Bild gezeichnet und in einer Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c37c3-179">The following code example shows how to draw and save the following image to a file.</span></span>

![Beispiel eines Ausgabe Bilds.](images/saveasimagefile-sample.png)

<span data-ttu-id="c37c3-181">Dieses Codebeispiel erstellt zuerst eine [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) und ein [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -Renderziel.</span><span class="sxs-lookup"><span data-stu-id="c37c3-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="c37c3-182">Anschließend wird eine Zeichnung mit Text, einer Pfad Geometrie, die ein Stundenglas darstellt, und einem transformierten Stundenglas in eine WIC-Bitmap gerendert.</span><span class="sxs-lookup"><span data-stu-id="c37c3-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="c37c3-183">Anschließend wird [IWICStream:: initializefromfilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) verwendet, um die Bitmap in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c37c3-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="c37c3-184">Wenn die Anwendung die Bitmap im Arbeitsspeicher speichern muss, verwenden Sie stattdessen [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="c37c3-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="c37c3-185">Schließlich wird [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) verwendet, um die Bitmap zu codieren.</span><span class="sxs-lookup"><span data-stu-id="c37c3-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="c37c3-186">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c37c3-186">Conclusion</span></span>

<span data-ttu-id="c37c3-187">Wie oben gezeigt, ist die Verwendung von Direct2D für serverseitiges Rendering einfach und unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="c37c3-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="c37c3-188">Außerdem bietet Sie ein hochwertiges und hochgradig parallelisierbares Rendering, das in Umgebungen mit geringen Rechten auf dem Server ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c37c3-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c37c3-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c37c3-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c37c3-190">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="c37c3-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 