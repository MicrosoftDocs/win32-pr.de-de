---
title: ID3DX11Effect-Optimierungsmethode (D3dx11effect. h)
description: Minimieren Sie den für einen Effekt benötigten Arbeitsspeicher.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimieren der Methode Direct3D 11
- Optimieren der Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, Methode optimieren
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996088"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="43049-106">ID3DX11Effect:: optimiert-Methode</span><span class="sxs-lookup"><span data-stu-id="43049-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="43049-107">Minimieren Sie den für einen Effekt benötigten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="43049-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="43049-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="43049-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="43049-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="43049-109">Parameters</span></span>

<span data-ttu-id="43049-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="43049-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43049-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43049-111">Return value</span></span>

<span data-ttu-id="43049-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43049-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43049-113">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="43049-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43049-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43049-114">Remarks</span></span>

<span data-ttu-id="43049-115">Ein Effekt verwendet zwei verschiedene Möglichkeiten, um die für die Laufzeit erforderlichen Informationen zum Ausführen eines Effekts zu speichern und die Metadaten zu speichern, die für die Wiedergabe von Informationen an eine Anwendung mithilfe der API erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="43049-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="43049-116">Sie können den von einem Effekt benötigten Arbeitsspeicher verringern, indem Sie **ID3DX11Effect:: optimiert** aufrufen, wodurch die reflektionsmetadaten aus dem Arbeitsspeicher entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="43049-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="43049-117">API-Methoden zum Lesen von Variablen funktionieren nicht mehr, sobald die reflektionsingendaten entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="43049-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="43049-118">Die folgenden Methoden schlagen fehl, nachdem die Optimierung für einen Effekt aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="43049-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="43049-119">**ID3DX11Effect:: getconstantbufferbyindex**</span><span class="sxs-lookup"><span data-stu-id="43049-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="43049-120">**ID3DX11Effect:: getconstantbufferbyname**</span><span class="sxs-lookup"><span data-stu-id="43049-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="43049-121">**ID3DX11Effect:: getdebug**</span><span class="sxs-lookup"><span data-stu-id="43049-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="43049-122">**ID3DX11Effect:: getdevice**</span><span class="sxs-lookup"><span data-stu-id="43049-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="43049-123">**ID3DX11Effect:: gettechniquebyindex**</span><span class="sxs-lookup"><span data-stu-id="43049-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="43049-124">**ID3DX11Effect:: gettechniquebyname**</span><span class="sxs-lookup"><span data-stu-id="43049-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="43049-125">**ID3DX11Effect:: getvariablebyindex**</span><span class="sxs-lookup"><span data-stu-id="43049-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="43049-126">**ID3DX11Effect:: getvariablebyname**</span><span class="sxs-lookup"><span data-stu-id="43049-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="43049-127">**ID3DX11Effect:: getvariablebysemantic**</span><span class="sxs-lookup"><span data-stu-id="43049-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="43049-128">Verweise, die mit diesen Methoden vor dem Aufruf von **ID3DX11Effect:: optimiert** abgerufen werden, sind nach wie vor für den Aufruf von **ID3DX11Effect::** Optimierungen gültig</span><span class="sxs-lookup"><span data-stu-id="43049-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="43049-129">Dadurch kann die Anwendung alle Variablen, Techniken und Verläufen abrufen, die Sie verwenden werden, und dann optimieren und dann den Effekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="43049-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="43049-130">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="43049-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="43049-131">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="43049-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="43049-132">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="43049-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43049-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="43049-133">Requirements</span></span>



| <span data-ttu-id="43049-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43049-134">Requirement</span></span> | <span data-ttu-id="43049-135">Wert</span><span class="sxs-lookup"><span data-stu-id="43049-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43049-136">Header</span><span class="sxs-lookup"><span data-stu-id="43049-136">Header</span></span><br/>  | <dl> <span data-ttu-id="43049-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43049-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="43049-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43049-138">Library</span></span><br/> | <dl> <span data-ttu-id="43049-139"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="43049-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43049-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43049-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43049-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="43049-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





