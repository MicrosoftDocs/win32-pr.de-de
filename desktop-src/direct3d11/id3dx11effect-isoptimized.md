---
title: ID3DX11Effect isoptimierte-Methode (D3dx11effect. h)
description: Testen eines Effekts, um zu ermitteln, ob die reflektionsintemetadaten aus dem Arbeitsspeicher entfernt wurden.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Isoptimierte Methode Direct3D 11
- Isoptimierte Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, isoptimierte Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355537"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="55f3a-106">ID3DX11Effect:: isoptimierte-Methode</span><span class="sxs-lookup"><span data-stu-id="55f3a-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="55f3a-107">Testen eines Effekts, um zu ermitteln, ob die reflektionsintemetadaten aus dem Arbeitsspeicher entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="55f3a-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f3a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="55f3a-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="55f3a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="55f3a-109">Parameters</span></span>

<span data-ttu-id="55f3a-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="55f3a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55f3a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55f3a-111">Return value</span></span>

<span data-ttu-id="55f3a-112">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55f3a-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="55f3a-113">**True** , wenn der Effekt optimiert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="55f3a-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55f3a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55f3a-114">Remarks</span></span>

<span data-ttu-id="55f3a-115">Ein Effekt verwendet zwei verschiedene Möglichkeiten, um die für die Laufzeit erforderlichen Informationen zum Ausführen eines Effekts zu speichern und die Metadaten zu speichern, die für die Wiedergabe von Informationen an eine Anwendung mithilfe der API erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="55f3a-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="55f3a-116">Sie können den von einem Effekt benötigten Arbeitsspeicher verringern, indem Sie [**ID3DX11Effect:: optimiert**](id3dx11effect-optimize.md) aufrufen, wodurch die reflektionsmetadaten aus dem Arbeitsspeicher entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="55f3a-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="55f3a-117">Natürlich funktionieren API-Methoden zum Lesen von Variablen nicht mehr, sobald die reflektionsliste entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="55f3a-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="55f3a-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="55f3a-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="55f3a-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="55f3a-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="55f3a-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="55f3a-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55f3a-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="55f3a-121">Requirements</span></span>



| <span data-ttu-id="55f3a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55f3a-122">Requirement</span></span> | <span data-ttu-id="55f3a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="55f3a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f3a-124">Header</span><span class="sxs-lookup"><span data-stu-id="55f3a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="55f3a-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f3a-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="55f3a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55f3a-126">Library</span></span><br/> | <dl> <span data-ttu-id="55f3a-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="55f3a-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f3a-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55f3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f3a-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="55f3a-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

