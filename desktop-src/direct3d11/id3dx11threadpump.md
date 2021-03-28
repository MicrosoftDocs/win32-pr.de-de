---
title: ID3DX11ThreadPump-Schnittstelle (D3DX11core. h)
description: Ein Thread-Pump führt Aufgaben asynchron aus.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- ID3DX11ThreadPump-Schnittstelle Direct3D 11
- ID3DX11ThreadPump Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103070"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="631e0-105">ID3DX11ThreadPump-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="631e0-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="631e0-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="631e0-107">Ein Thread-Pump führt Aufgaben asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="631e0-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="631e0-108">Sie wird durch Aufrufen von [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="631e0-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="631e0-109">Es gibt mehrere APIs, die ein optionales threadpump als Parameter akzeptieren, z. b. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile**](d3dx11compilefromfile.md). Wenn Sie eine Thread-Pump-Schnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="631e0-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="631e0-110">Vor allem bei Multiprozessorcomputern kann ein Thread-Pump Ressourcen laden und Daten verarbeiten, ohne eine spürbare Leistungsminderung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="631e0-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="631e0-111">Member</span><span class="sxs-lookup"><span data-stu-id="631e0-111">Members</span></span>

<span data-ttu-id="631e0-112">Die **ID3DX11ThreadPump** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="631e0-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="631e0-113">**ID3DX11ThreadPump** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="631e0-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="631e0-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="631e0-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="631e0-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="631e0-115">Methods</span></span>

<span data-ttu-id="631e0-116">Die **ID3DX11ThreadPump** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="631e0-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="631e0-117">Methode</span><span class="sxs-lookup"><span data-stu-id="631e0-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="631e0-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="631e0-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="631e0-119"><a href="id3dx11threadpump-addworkitem.md"><strong>Addworkitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="631e0-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="631e0-120">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="631e0-121">Fügt der Thread Pumpe ein Arbeits Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="631e0-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="631e0-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>Getqueuestatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="631e0-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="631e0-123">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="631e0-124">Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe ab.</span><span class="sxs-lookup"><span data-stu-id="631e0-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="631e0-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>Getworkitemcount</strong></a></span><span class="sxs-lookup"><span data-stu-id="631e0-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="631e0-126">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="631e0-127">Ruft die Anzahl der Arbeitselemente in der Thread Pumpe ab.</span><span class="sxs-lookup"><span data-stu-id="631e0-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="631e0-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>Processdeviceworkitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="631e0-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="631e0-129">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="631e0-130">Legt Arbeitselemente auf das Gerät fest, nachdem Sie geladen und verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="631e0-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="631e0-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>Purgeallitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="631e0-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="631e0-132">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="631e0-133">Löscht alle Arbeitselemente aus der Thread Pumpe.</span><span class="sxs-lookup"><span data-stu-id="631e0-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="631e0-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>Waitforallitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="631e0-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="631e0-135">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631e0-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="631e0-136">Wartet, bis alle Arbeitselemente in der Thread Pumpe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="631e0-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="631e0-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="631e0-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="631e0-138">Verwenden eines Thread Pump</span><span class="sxs-lookup"><span data-stu-id="631e0-138">Using a Thread Pump</span></span>

<span data-ttu-id="631e0-139">Die Thread Pumpe lädt und verarbeitet Daten mit dem folgenden dreistufigen Prozess:</span><span class="sxs-lookup"><span data-stu-id="631e0-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="631e0-140">Laden und decokomprimieren der Daten mit einem [**Daten Lader**](id3dx11dataloader.md).</span><span class="sxs-lookup"><span data-stu-id="631e0-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="631e0-141">Das Data Loader-Objekt verfügt über drei Methoden, die vom threadpump intern beim Laden und Dekomprimieren der Daten aufgerufen werden: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D eComPress**](id3dx11dataloader-decompress.md)und [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="631e0-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="631e0-142">Die spezifischen Funktionen dieser drei APIs unterscheiden sich abhängig vom Typ der geladenen und dekomprimierten Daten.</span><span class="sxs-lookup"><span data-stu-id="631e0-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="631e0-143">Die Schnittstelle des Daten Laders kann auch geerbt werden, und die zugehörigen APIs können geändert werden, wenn eine Datendatei geladen wird, die in einem eigenen benutzerdefinierten Format definiert ist.</span><span class="sxs-lookup"><span data-stu-id="631e0-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="631e0-144">Verarbeiten Sie die Daten mit einem [**Datenprozessor**](id3dx11dataprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="631e0-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="631e0-145">Das Data Processor-Objekt verfügt über drei Methoden, die von der Thread Pumpe intern aufgerufen werden, während Sie die Daten verarbeitet: [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: foratedeviceobject**](id3dx11dataprocessor-createdeviceobject.md)und [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="631e0-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="631e0-146">Die Art und Weise, wie die Daten verarbeitet werden, unterscheidet sich je nach Art der Daten.</span><span class="sxs-lookup"><span data-stu-id="631e0-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="631e0-147">Wenn es sich bei den Daten z. b. um eine Textur handelt, die als JPEG gespeichert ist, führt [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) eine JPEG-Komprimierung durch, um die rohbildbits des Bilds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="631e0-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="631e0-148">Wenn es sich bei den Daten um einen Shader handelt, kompiliert [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) den HLSL in Bytecode.</span><span class="sxs-lookup"><span data-stu-id="631e0-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="631e0-149">Nachdem die Daten verarbeitet wurden, wird ein Geräte Objekt für diese Daten erstellt (mit [**ID3DX11DataProcessor:: kreatedeviceobject**](id3dx11dataprocessor-createdeviceobject.md)), und das Objekt wird einer Warteschlange von Geräte Objekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="631e0-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="631e0-150">Die Datenprozessor Schnittstelle kann auch geerbt werden, und die zugehörigen APIs können geändert werden, wenn eine Datendatei verarbeitet wird, die in einem eigenen benutzerdefinierten Format definiert ist.</span><span class="sxs-lookup"><span data-stu-id="631e0-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="631e0-151">Binden Sie das Geräte Objekt an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="631e0-151">Bind the device object to the device.</span></span> <span data-ttu-id="631e0-152">Dies geschieht, wenn eine Anwendung [**ID3DX11ThreadPump::P rocess deviceworkitems**](id3dx11threadpump-processdeviceworkitems.md)aufruft, die eine angegebene Anzahl von Objekten in der Warteschlange von Geräte Objekten an das Gerät bindet.</span><span class="sxs-lookup"><span data-stu-id="631e0-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="631e0-153">Die Thread Pumpe kann zum Laden von Daten auf zwei Arten verwendet werden: durch Aufrufen einer API, die eine Thread Pumpe als Parameter annimmt, z. b. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), oder durch Aufrufen von [**ID3DX11ThreadPump:: addworkitem**](id3dx11threadpump-addworkitem.md).</span><span class="sxs-lookup"><span data-stu-id="631e0-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="631e0-154">Bei den APIs, die eine Thread Pumpe verwenden, werden der Daten Lader und der Datenprozessor intern erstellt.</span><span class="sxs-lookup"><span data-stu-id="631e0-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="631e0-155">Im Fall von addworkitem müssen der Daten Lader und der Datenprozessor vorab erstellt und dann an addworkitem übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="631e0-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="631e0-156">Bibliothek d3dx11 bietet eine Reihe von APIs zum Erstellen von Daten Lade Programmen und Datenprozessoren mit Funktionen zum Laden und Verarbeiten von allgemeinen Datenformaten.</span><span class="sxs-lookup"><span data-stu-id="631e0-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="631e0-157">Bei benutzerdefinierten Datenformaten müssen die Daten Lader-und Datenprozessor Schnittstellen geerbt werden, und ihre Methoden müssen neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="631e0-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="631e0-158">Das Thread-Pump Objekt nimmt eine beträchtliche Menge an Ressourcen in Rechnung, daher sollte im Allgemeinen nur eine pro Anwendung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="631e0-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="631e0-159">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="631e0-159">Requirements</span></span>



| <span data-ttu-id="631e0-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="631e0-160">Requirement</span></span> | <span data-ttu-id="631e0-161">Wert</span><span class="sxs-lookup"><span data-stu-id="631e0-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="631e0-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="631e0-162">Minimum supported client</span></span><br/> | <span data-ttu-id="631e0-163">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="631e0-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="631e0-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="631e0-164">Minimum supported server</span></span><br/> | <span data-ttu-id="631e0-165">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="631e0-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="631e0-166">Header</span><span class="sxs-lookup"><span data-stu-id="631e0-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="631e0-167"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="631e0-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="631e0-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="631e0-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="631e0-169"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="631e0-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="631e0-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="631e0-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631e0-171">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="631e0-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

