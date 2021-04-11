---
description: Optionen zum Speichern und Erstellen von Effekten.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123386"
---
# <a name="d3dxfx"></a><span data-ttu-id="2a225-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="2a225-103">D3DXFX</span></span>

<span data-ttu-id="2a225-104">Optionen zum Speichern und Erstellen von Effekten.</span><span class="sxs-lookup"><span data-stu-id="2a225-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="2a225-105">Die Konstanten in der folgenden Tabelle sind in d3dx9effect. h definiert.</span><span class="sxs-lookup"><span data-stu-id="2a225-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a225-106">Speicher-und Wiederherstellungs Flags des Wirkungs Zustands</span><span class="sxs-lookup"><span data-stu-id="2a225-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="2a225-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a225-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a225-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="2a225-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="2a225-109">Beim Aufrufen von " <a href="id3dxeffect--end.md"><strong>End</strong></a>" <a href="id3dxeffect--begin.md"><strong>oder "</strong></a> wieder hergestellt" wird kein Status gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2a225-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a225-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="2a225-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="2a225-111">Ein stateblock speichert den Zustand beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wieder her.</span><span class="sxs-lookup"><span data-stu-id="2a225-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a225-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="2a225-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="2a225-113">Ein stateblock speichert den Zustand (außer Shader und shaderkonstanten) beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wieder her.</span><span class="sxs-lookup"><span data-stu-id="2a225-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a225-114">Effekte erstellungsflags</span><span class="sxs-lookup"><span data-stu-id="2a225-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="2a225-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a225-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a225-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="2a225-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="2a225-117">Der Effekt ist nicht klonbar und enthält keine Shader-Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="2a225-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="2a225-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>Getpassde SC</strong></a> gibt keine shaderfunktionszeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="2a225-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="2a225-119">Wenn Sie dieses Flag festlegen, wird die Arbeitsspeicher Auslastung um etwa 50% reduziert, da das Effektsystem nicht mehr benötigt, um eine Kopie der Shader im Arbeitsspeicher beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="2a225-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="2a225-120">Dieses Flag wird von <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>und <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a225-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a225-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="2a225-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="2a225-122">Ermöglicht die Zuordnung einer Effekt Ressource in den uppder-Adressraum eines Computers.</span><span class="sxs-lookup"><span data-stu-id="2a225-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="2a225-123">Eine wichtige Einschränkung ist, dass Sie Zeichen folgen und Handles nicht austauschbar verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2a225-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="2a225-124">Beispielsweise würde Folgendes nicht mehr funktionieren.</span><span class="sxs-lookup"><span data-stu-id="2a225-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a225-125">Stattdessen muss eine Methode wie z. b. [<strong>getparameterbyname</strong>](id3dxbaseeffect--getparameterbyname.md) verwendet werden, um das Handle des-Parameters zu speichern, das dann verwendet wird, um Variablen an den Effekt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="2a225-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2a225-126">Die Konstanten in der folgenden Tabelle sind nicht standardmäßig definiert und müssen vom Entwickler definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a225-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a225-127">Effekt \# Präprozessordefinition</span><span class="sxs-lookup"><span data-stu-id="2a225-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="2a225-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a225-128">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="2a225-129">D3DXFX \_ largeaddress- \_ handle</span><span class="sxs-lookup"><span data-stu-id="2a225-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="2a225-130">Definieren Sie diesen Wert, bevor Sie d3dx9. h einschließen, damit die Anwendung nicht kompiliert werden kann, wenn Sie versuchen, Zeichen folgen an D3DXHANDLE-Parameter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="2a225-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="2a225-131">Dadurch wird sichergestellt, dass gültige Informationen an die Laufzeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="2a225-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="2a225-132">Effekt-Linker-Flags</span><span class="sxs-lookup"><span data-stu-id="2a225-132">Effect Linker Flags</span></span>            | <span data-ttu-id="2a225-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a225-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="2a225-134">hohe \_ Adressen \_ Unterstützung</span><span class="sxs-lookup"><span data-stu-id="2a225-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="2a225-135">Wenn Sie das Linker-Flag "große Adressen" festlegen \_ \_ = 1, kann die Anwendung bei Bedarf Ressourcen über dem Adress Limit von 2 GB zuordnen.</span><span class="sxs-lookup"><span data-stu-id="2a225-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="2a225-136">Das Effektsystem verwendet Zustands Blöcke zum automatischen Speichern und Wiederherstellen des Zustands.</span><span class="sxs-lookup"><span data-stu-id="2a225-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="2a225-137">Weitere Informationen zu Status Blöcken finden Sie unter [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="2a225-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a225-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a225-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a225-139">Effekt Konstanten</span><span class="sxs-lookup"><span data-stu-id="2a225-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



