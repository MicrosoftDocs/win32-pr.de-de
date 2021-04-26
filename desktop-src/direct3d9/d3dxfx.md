---
description: Optionen zum Speichern und Erstellen von Effekten.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995077"
---
# <a name="d3dxfx"></a><span data-ttu-id="c637d-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="c637d-103">D3DXFX</span></span>

<span data-ttu-id="c637d-104">Optionen zum Speichern und Erstellen von Effekten.</span><span class="sxs-lookup"><span data-stu-id="c637d-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="c637d-105">Die Konstanten in der folgenden Tabelle sind in d3dx9effect.h definiert.</span><span class="sxs-lookup"><span data-stu-id="c637d-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c637d-106">Effect State Save and Restore Flags</span><span class="sxs-lookup"><span data-stu-id="c637d-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="c637d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c637d-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c637d-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="c637d-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="c637d-109">Beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> oder restored beim Aufrufen von End wird kein Zustand <a href="id3dxeffect--end.md"><strong>gespeichert.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c637d-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c637d-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="c637d-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="c637d-111">Ein StateBlock speichert den Zustand beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin und</strong></a> stellt den Zustand beim Aufrufen von End wieder <a href="id3dxeffect--end.md"><strong>wieder auf.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c637d-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c637d-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="c637d-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="c637d-113">Ein Zustandsblock speichert den Zustand (mit Ausnahme von Shadern und Shaderkonstatoren) beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End wieder auf.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c637d-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c637d-114">Flags für die Effekterstellung</span><span class="sxs-lookup"><span data-stu-id="c637d-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="c637d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c637d-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c637d-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="c637d-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="c637d-117">Der Effekt ist nicht klonbar und enthält keine binären Shaderdaten.</span><span class="sxs-lookup"><span data-stu-id="c637d-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="c637d-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc gibt</strong></a> keine Shaderfunktionszeige zurück.</span><span class="sxs-lookup"><span data-stu-id="c637d-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="c637d-119">Durch festlegen dieses Flags wird die Arbeitsspeicherauslastung um etwa 50 % reduziert, da das Effektsystem keine Kopie der Shader im Arbeitsspeicher behalten muss.</span><span class="sxs-lookup"><span data-stu-id="c637d-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="c637d-120">Dieses Flag wird von <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect,</strong></a> <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>und <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource verwendet.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c637d-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c637d-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="c637d-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="c637d-122">Ermöglicht die Zuordnung einer Effektressource in den Adressraum des Uppders eines Computers.</span><span class="sxs-lookup"><span data-stu-id="c637d-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="c637d-123">Eine wichtige Einschränkung besteht darin, dass Zeichenfolgen und Handles nicht austauschbar verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c637d-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="c637d-124">Das folgende Beispiel würde nicht mehr funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c637d-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
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

<span data-ttu-id="c637d-125">Stattdessen muss eine Methode wie [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) verwendet werden, um das Handle des Parameters zu speichern, der dann zum Übergeben von Variablen an den Effekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c637d-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c637d-126">Die Konstanten in der folgenden Tabelle sind nicht standardmäßig definiert und müssen vom Entwickler definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c637d-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



| <span data-ttu-id="c637d-127">Effect Preprocessor \# define es</span><span class="sxs-lookup"><span data-stu-id="c637d-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="c637d-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c637d-128">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c637d-129">D3DXFX \_ \_ LARGEADDRESS-HANDLE</span><span class="sxs-lookup"><span data-stu-id="c637d-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="c637d-130">Definieren Sie diesen Wert, bevor Sie d3dx9.h einschließen, damit ihre Anwendung beim Versuch, Zeichenfolgen an D3DXHANDLE-Parameter zu übergeben, nicht kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c637d-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="c637d-131">Dadurch wird sichergestellt, dass gültige Informationen an die Laufzeit übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c637d-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="c637d-132">Effektlinkerflags</span><span class="sxs-lookup"><span data-stu-id="c637d-132">Effect Linker Flags</span></span>            | <span data-ttu-id="c637d-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c637d-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c637d-134">LARGE \_ ADDRESS \_ AWARE</span><span class="sxs-lookup"><span data-stu-id="c637d-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="c637d-135">Wenn Sie das Linkerflag LARGE ADDRESS AWARE = 1 festlegen, \_ kann die Anwendung Bei Bedarf Ressourcen über den Grenzwert von \_ 2 GB an Adressen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c637d-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="c637d-136">Das Effektsystem verwendet Zustandsblöcke, um den Zustand automatisch zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c637d-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="c637d-137">Weitere Informationen zu Zustandsblöcken finden Sie unter [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9).](state-blocks-save-and-restore-state.md)</span><span class="sxs-lookup"><span data-stu-id="c637d-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c637d-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c637d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c637d-139">Effektkonstanten</span><span class="sxs-lookup"><span data-stu-id="c637d-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



