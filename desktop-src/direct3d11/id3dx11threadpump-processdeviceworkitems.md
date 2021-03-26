---
title: ID3DX11ThreadPump processdeviceworkitems-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Legt Arbeitselemente auf das Gerät fest, nachdem Sie geladen und verarbeitet wurden.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Processdeviceworkitems-Methode Direct3D 11
- Processdeviceworkitems-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump Interface Direct3D 11, processdeviceworkitems-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982227"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="afcd4-107">ID3DX11ThreadPump::P rocess deviceworkitems-Methode</span><span class="sxs-lookup"><span data-stu-id="afcd4-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="afcd4-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="afcd4-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="afcd4-109">Legt Arbeitselemente auf das Gerät fest, nachdem Sie geladen und verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="afcd4-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="afcd4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="afcd4-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="afcd4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="afcd4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afcd4-112">*iworkitemcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afcd4-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afcd4-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="afcd4-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="afcd4-114">Die Anzahl der Arbeitselemente, die auf das Gerät festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="afcd4-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afcd4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afcd4-115">Return value</span></span>

<span data-ttu-id="afcd4-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="afcd4-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="afcd4-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="afcd4-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="afcd4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afcd4-118">Remarks</span></span>

<span data-ttu-id="afcd4-119">Wenn die Thread Pumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird Sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. an diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="afcd4-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="afcd4-120">Dies ist hilfreich, um die Verarbeitungs Menge zu steuern, die für die Bindung von Ressourcen an das Gerät für jeden Frame aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="afcd4-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="afcd4-121">Ein Beispiel dafür, wie Sie diese API verwenden können, ist, dass Sie das Ende einer Ebene im Spiel nähern und damit beginnen möchten, die Texturen, Shader und andere Ressourcen für die nächste Ebene vorab zu laden.</span><span class="sxs-lookup"><span data-stu-id="afcd4-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="afcd4-122">Die Thread Pumpe lädt das Laden, dekomprimieren und Verarbeiten der Ressourcen und Shader in einem separaten Thread, bis Sie für die Festlegung auf das Gerät bereit sind. an diesem Punkt werden Sie in einer Warteschlange belassen.</span><span class="sxs-lookup"><span data-stu-id="afcd4-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="afcd4-123">Möglicherweise möchten Sie nicht alle Ressourcen und Shader gleichzeitig auf das Gerät festlegen, da dies zu einer merklichen vorübergehenden Verlangsamung der Spielleistung führen kann.</span><span class="sxs-lookup"><span data-stu-id="afcd4-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="afcd4-124">Daher könnte diese API einmal pro Frame aufgerufen werden, sodass nur eine kleine Anzahl von Arbeitsaufgaben auf das Gerät in jedem Frame festgelegt wird. Dadurch wird die Arbeitslast der Bindungs Ressourcen über mehrere Frames auf das Gerät verteilt.</span><span class="sxs-lookup"><span data-stu-id="afcd4-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="afcd4-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="afcd4-125">Requirements</span></span>



| <span data-ttu-id="afcd4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afcd4-126">Requirement</span></span> | <span data-ttu-id="afcd4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="afcd4-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afcd4-128">Header</span><span class="sxs-lookup"><span data-stu-id="afcd4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="afcd4-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="afcd4-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="afcd4-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afcd4-130">Library</span></span><br/> | <dl> <span data-ttu-id="afcd4-131"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afcd4-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="afcd4-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="afcd4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afcd4-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="afcd4-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="afcd4-134">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="afcd4-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

