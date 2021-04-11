---
description: Legen Sie die Arbeitselemente auf das Gerät fest, nachdem das Laden und verarbeiten abgeschlossen ist.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump::P rocess deviceworkitems-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132416"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="6819b-103">ID3DX10ThreadPump::P rocess deviceworkitems-Methode</span><span class="sxs-lookup"><span data-stu-id="6819b-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="6819b-104">Legen Sie die Arbeitselemente auf das Gerät fest, nachdem das Laden und verarbeiten abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6819b-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="6819b-105">Wenn die Thread Pumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird Sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. an diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6819b-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="6819b-106">Dies ist hilfreich, um die Verarbeitungs Menge zu steuern, die für die Bindung von Ressourcen an das Gerät für jeden Frame aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6819b-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="6819b-107">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="6819b-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="6819b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6819b-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="6819b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6819b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6819b-110">*iworkitemcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6819b-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6819b-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6819b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6819b-112">Die Anzahl der Arbeitselemente, die auf das Gerät festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6819b-112">The number of work items to set to the device.</span></span> <span data-ttu-id="6819b-113">Processdeviceobjectcreation erstellt höchstens iworkitemcount-Objekte.</span><span class="sxs-lookup"><span data-stu-id="6819b-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="6819b-114">Wenn nicht genügend Arbeitselemente in der Warteschlange vorhanden sind, um iworkitemcount-Objekte zu verarbeiten, erstellt processdeviceobjectcreation so viele Geräte Objekte, wie sich Elemente in der Warteschlange befinden.</span><span class="sxs-lookup"><span data-stu-id="6819b-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6819b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6819b-115">Return value</span></span>

<span data-ttu-id="6819b-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6819b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6819b-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="6819b-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6819b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6819b-118">Remarks</span></span>

<span data-ttu-id="6819b-119">Ein Beispiel dafür, wie Sie diese API verwenden können, ist, dass Sie das Ende einer Ebene im Spiel nähern und damit beginnen möchten, die Texturen, Shader und andere Ressourcen für die nächste Ebene vorab zu laden.</span><span class="sxs-lookup"><span data-stu-id="6819b-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="6819b-120">Die Thread Pumpe lädt das Laden, dekomprimieren und Verarbeiten der Ressourcen und Shader in einem separaten Thread, bis Sie für die Festlegung auf das Gerät bereit sind. an diesem Punkt werden Sie in einer Warteschlange belassen.</span><span class="sxs-lookup"><span data-stu-id="6819b-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="6819b-121">Möglicherweise möchten Sie nicht alle Ressourcen und Shader gleichzeitig auf das Gerät festlegen, da dies dazu führen kann, dass die Leistung eines temporären Benachrichtigungs verkabels verlangsamt wird.</span><span class="sxs-lookup"><span data-stu-id="6819b-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="6819b-122">Daher könnte diese API einmal pro Frame aufgerufen werden, sodass nur eine kleine Anzahl von Arbeitsaufgaben auf das Gerät in jedem Frame festgelegt wird. Dadurch wird die Arbeitslast der Bindungs Ressourcen auf das Gerät über mehrere Frames verteilt, und die Wahrscheinlichkeit eines Benachrichtigungs Kabels in der Spielleistung wird minimiert.</span><span class="sxs-lookup"><span data-stu-id="6819b-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6819b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6819b-123">Requirements</span></span>



| <span data-ttu-id="6819b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6819b-124">Requirement</span></span> | <span data-ttu-id="6819b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6819b-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6819b-126">Header</span><span class="sxs-lookup"><span data-stu-id="6819b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6819b-127"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6819b-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6819b-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6819b-128">Library</span></span><br/> | <dl> <span data-ttu-id="6819b-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6819b-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6819b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6819b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6819b-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="6819b-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="6819b-132">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6819b-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
