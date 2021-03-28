---
title: ID3DX11EffectVariable IsValid-Methode (D3dx11effect. h)
description: Vergleichen Sie den Datentyp mit den gespeicherten Daten.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- IsValid-Methode Direct3D 11
- IsValid-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, IsValid-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996138"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="c6d45-106">ID3DX11EffectVariable:: IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="c6d45-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="c6d45-107">Vergleichen Sie den Datentyp mit den gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="c6d45-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d45-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6d45-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="c6d45-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6d45-109">Parameters</span></span>

<span data-ttu-id="c6d45-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c6d45-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6d45-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6d45-111">Return value</span></span>

<span data-ttu-id="c6d45-112">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6d45-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6d45-113">**True** , wenn die Syntax gültig ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c6d45-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6d45-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6d45-114">Remarks</span></span>

<span data-ttu-id="c6d45-115">Diese Methode überprüft, ob der Datentyp mit den Daten übereinstimmt, die nach dem Umwandeln einer Schnittstelle in eine andere gespeichert wurden (mithilfe einer der AS-Methoden).</span><span class="sxs-lookup"><span data-stu-id="c6d45-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="c6d45-116">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="c6d45-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c6d45-117">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6d45-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c6d45-118">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c6d45-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6d45-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c6d45-119">Requirements</span></span>



| <span data-ttu-id="c6d45-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6d45-120">Requirement</span></span> | <span data-ttu-id="c6d45-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c6d45-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d45-122">Header</span><span class="sxs-lookup"><span data-stu-id="c6d45-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c6d45-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6d45-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c6d45-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6d45-124">Library</span></span><br/> | <dl> <span data-ttu-id="c6d45-125"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="c6d45-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d45-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6d45-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d45-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c6d45-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

