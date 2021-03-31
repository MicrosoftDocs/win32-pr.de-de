---
title: Direct3D 11 Kern Schnittstellen
description: Dieser Abschnitt enthält Informationen zu den Kern Schnittstellen.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- Schnittstellen, Direct3D 11 Kerne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474525"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="2b883-104">Direct3D 11 Kern Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2b883-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="2b883-105">Dieser Abschnitt enthält Informationen zu den Kern Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2b883-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2b883-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b883-107">Thema</span><span class="sxs-lookup"><span data-stu-id="2b883-107">Topic</span></span></th>
<th><span data-ttu-id="2b883-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b883-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b883-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-110">Diese Schnittstelle kapselt Methoden zum asynchronen Abrufen von Daten aus der GPU.</span><span class="sxs-lookup"><span data-stu-id="2b883-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-112">Die Blend-State-Schnittstelle enthält eine Beschreibung des Mischungs Zustands, die Sie an die <a href="d3d10-graphics-programming-guide-output-merger-stage.md">Ausgabe-Fusion-Phase</a>binden können.</span><span class="sxs-lookup"><span data-stu-id="2b883-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-114">Die Blend-State-Schnittstelle enthält eine Beschreibung des Mischungs Zustands, die Sie an die <a href="d3d10-graphics-programming-guide-output-merger-stage.md">Ausgabe-Fusion-Phase</a>binden können.</span><span class="sxs-lookup"><span data-stu-id="2b883-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="2b883-115">Diese Blend-State-Schnittstelle unterstützt logische Vorgänge und Mischungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2b883-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-117">Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> -Schnittstelle kapselt eine Liste von Grafik Befehlen für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="2b883-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-119">Diese Schnittstelle kapselt Methoden zum Messen der GPU-Leistung.</span><span class="sxs-lookup"><span data-stu-id="2b883-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-121">Die Schnittstelle "tiefen Schablone-Status" enthält eine Beschreibung für den Status der tiefen Schablone, die Sie an die <a href="d3d10-graphics-programming-guide-output-merger-stage.md">Ausgabe-Fusion-Phase</a>binden können.</span><span class="sxs-lookup"><span data-stu-id="2b883-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-123">Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-125">Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="2b883-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> fügt den in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-128">Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="2b883-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-131">Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="2b883-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-134">Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="2b883-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> fügt in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>neue Methoden hinzu, z. b. <strong>registerdeviceremovedevent</strong> und <strong>unregisterdeviceremoved</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b883-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-137">Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b883-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="2b883-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> fügt den in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-140">Eine Geräte untergeordnete Schnittstelle greift auf Daten zu, die von einem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b883-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-142">Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a> -Schnittstelle stellt einen Gerätekontext dar, der renderingbefehle generiert.</span><span class="sxs-lookup"><span data-stu-id="2b883-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b883-143">Die neueste Version dieser Schnittstelle ist <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> , die in Windows 10 Creators Update eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b883-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="2b883-144">Anwendungen, die das Windows 10 Creators Update verwenden, sollten anstelle von <strong>ID3D11Device</strong>die <strong>ID3D11DeviceContext4</strong> -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b883-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-146">Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b883-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="2b883-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> fügt den in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-149">Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b883-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="2b883-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-152">Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b883-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="2b883-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-155">Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b883-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="2b883-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> fügt den in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>neue Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b883-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-158">Die <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> -Schnittstelle stellt ein Kontext Zustands Objekt dar, das Zustands-und Verhaltens Informationen zu einem Microsoft Direct3D-Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="2b883-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-160">Stellt einen Fence dar, ein Objekt, das für die Synchronisierung der CPU und eines oder mehrerer GPUs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b883-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-162">Eine Eingabe Layout-Schnittstelle enthält eine Definition, wie Vertex-Daten, die im Arbeitsspeicher angeordnet sind, in die <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">Eingabe-Assembler-Phase</a> der <a href="overviews-direct3d-11-graphics-pipeline.md">Grafik Pipeline</a>eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2b883-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-164">Bietet Threading Schutz für kritische Abschnitte einer Multithreadanwendung.</span><span class="sxs-lookup"><span data-stu-id="2b883-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-166">Eine Prädikat Schnittstelle bestimmt, ob die Geometrie abhängig von den Ergebnissen eines vorherigen zeichnen-Aufrufes verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b883-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-168">Eine Abfrage Schnittstelle fragt Informationen von der GPU ab.</span><span class="sxs-lookup"><span data-stu-id="2b883-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-170">Stellt ein Abfrageobjekt zum Abfragen von Informationen aus der GPU (Graphics Processing Unit) dar.</span><span class="sxs-lookup"><span data-stu-id="2b883-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-172">Die Raster-State-Schnittstelle enthält eine Beschreibung für den Status des Rasterizers, den Sie an die <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">Raster-Stufe</a>binden können.</span><span class="sxs-lookup"><span data-stu-id="2b883-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-174">Die Raster-State-Schnittstelle enthält eine Beschreibung für den Status des Rasterizers, den Sie an die <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">Raster-Stufe</a>binden können.</span><span class="sxs-lookup"><span data-stu-id="2b883-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="2b883-175">Diese Rasterizer-State-Schnittstelle unterstützt die erzwungene Stichproben Anzahl.</span><span class="sxs-lookup"><span data-stu-id="2b883-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b883-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-177">Die Raster-State-Schnittstelle enthält eine Beschreibung für den Status des Rasterizers, den Sie an die <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">Raster-Stufe</a>binden können.</span><span class="sxs-lookup"><span data-stu-id="2b883-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="2b883-178">Diese Rasterizer-State-Schnittstelle unterstützt die erzwungene Stichproben Anzahl und den konservativen rasterisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="2b883-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b883-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b883-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="2b883-180">Die samplerstatusschnittstelle enthält eine Beschreibung für den samplerstatus, den Sie an jede Shader-Stufe der <a href="overviews-direct3d-11-graphics-pipeline.md">Pipeline</a> binden können, um Sie durch Textur Beispiel Vorgänge zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="2b883-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2b883-181">Direct3D 11 implementiert Schnittstellen für:</span><span class="sxs-lookup"><span data-stu-id="2b883-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="2b883-182">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2b883-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="2b883-183">Shader</span><span class="sxs-lookup"><span data-stu-id="2b883-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="2b883-184">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b883-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b883-185">Kern Referenz</span><span class="sxs-lookup"><span data-stu-id="2b883-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

