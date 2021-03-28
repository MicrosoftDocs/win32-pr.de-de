---
title: ID3DX11Effect getconstantbufferbyname-Methode (D3dx11effect. h)
description: Einen konstanten Puffer anhand des Namens erhalten.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Getconstantbufferbyname-Methode Direct3D 11
- Getconstantbufferbyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, getconstantbufferbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870172"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="eba32-106">ID3DX11Effect:: getconstantbufferbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="eba32-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="eba32-107">Einen konstanten Puffer anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="eba32-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba32-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eba32-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="eba32-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eba32-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba32-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="eba32-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="eba32-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eba32-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eba32-112">Der Name des Konstanten Puffers.</span><span class="sxs-lookup"><span data-stu-id="eba32-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba32-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eba32-113">Return value</span></span>

<span data-ttu-id="eba32-114">Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="eba32-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="eba32-115">Ein Zeiger auf den konstanten Puffer, der durch den Namen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eba32-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="eba32-116">Siehe [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="eba32-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eba32-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eba32-117">Remarks</span></span>

<span data-ttu-id="eba32-118">Ein Effekt, der eine Variable enthält, die von einer Anwendung gelesen/geschrieben wird, erfordert mindestens einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="eba32-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="eba32-119">Um die optimale Leistung zu erzielen, sollten Sie die Variablen basierend auf Ihrer Aktualisierungshäufigkeit in mindestens einen konstanten Puffer anordnen.</span><span class="sxs-lookup"><span data-stu-id="eba32-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="eba32-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="eba32-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="eba32-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eba32-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="eba32-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="eba32-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eba32-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="eba32-123">Requirements</span></span>



| <span data-ttu-id="eba32-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eba32-124">Requirement</span></span> | <span data-ttu-id="eba32-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eba32-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba32-126">Header</span><span class="sxs-lookup"><span data-stu-id="eba32-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eba32-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eba32-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="eba32-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eba32-128">Library</span></span><br/> | <dl> <span data-ttu-id="eba32-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="eba32-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eba32-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eba32-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba32-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="eba32-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

