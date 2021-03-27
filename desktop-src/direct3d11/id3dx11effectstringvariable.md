---
title: ID3DX11EffectStringVariable-Schnittstelle (D3dx11effect. h)
description: Eine Zeichen folgen Variable-Schnittstelle greift auf eine Zeichen folgen Variable zu.
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- ID3DX11EffectStringVariable-Schnittstelle Direct3D 11
- ID3DX11EffectStringVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995811"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="60cf0-105">ID3DX11EffectStringVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="60cf0-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="60cf0-106">Eine Zeichen folgen Variable-Schnittstelle greift auf eine Zeichen folgen Variable zu.</span><span class="sxs-lookup"><span data-stu-id="60cf0-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="60cf0-107">Member</span><span class="sxs-lookup"><span data-stu-id="60cf0-107">Members</span></span>

<span data-ttu-id="60cf0-108">Die **ID3DX11EffectStringVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="60cf0-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="60cf0-109">**ID3DX11EffectStringVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60cf0-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="60cf0-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="60cf0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60cf0-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="60cf0-111">Methods</span></span>

<span data-ttu-id="60cf0-112">Die **ID3DX11EffectStringVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60cf0-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="60cf0-113">Methode</span><span class="sxs-lookup"><span data-stu-id="60cf0-113">Method</span></span>                                                               | <span data-ttu-id="60cf0-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60cf0-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="60cf0-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="60cf0-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="60cf0-116">Die Zeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="60cf0-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="60cf0-117">**GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="60cf0-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="60cf0-118">Ein Array von Zeichen folgen erhalten.</span><span class="sxs-lookup"><span data-stu-id="60cf0-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60cf0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60cf0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60cf0-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="60cf0-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="60cf0-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60cf0-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="60cf0-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="60cf0-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60cf0-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="60cf0-123">Requirements</span></span>



| <span data-ttu-id="60cf0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60cf0-124">Requirement</span></span> | <span data-ttu-id="60cf0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="60cf0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60cf0-126">Header</span><span class="sxs-lookup"><span data-stu-id="60cf0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="60cf0-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="60cf0-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60cf0-128">Library</span></span><br/> | <dl> <span data-ttu-id="60cf0-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60cf0-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60cf0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cf0-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="60cf0-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="60cf0-132">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="60cf0-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="60cf0-133">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="60cf0-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





