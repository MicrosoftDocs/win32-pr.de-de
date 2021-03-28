---
title: D3DX11_PASS_SHADER_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt Durchlauf.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982548"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="4072f-104">Bibliothek d3dx11 \_ Pass- \_ Shader- \_ debustruktur</span><span class="sxs-lookup"><span data-stu-id="4072f-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="4072f-105">Beschreibt einen Effekt Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="4072f-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="4072f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4072f-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="4072f-107">Member</span><span class="sxs-lookup"><span data-stu-id="4072f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4072f-108">**pshadervariable**</span><span class="sxs-lookup"><span data-stu-id="4072f-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="4072f-109">Typ: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4072f-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="4072f-110">Die Variable, von der dieser Shader stammt.</span><span class="sxs-lookup"><span data-stu-id="4072f-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="4072f-111">**Shaderindex**</span><span class="sxs-lookup"><span data-stu-id="4072f-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4072f-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4072f-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4072f-113">Das-Element von pshadervariable (bei einem Array) oder 0 (null), wenn es nicht zutreffend ist.</span><span class="sxs-lookup"><span data-stu-id="4072f-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4072f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4072f-114">Remarks</span></span>

<span data-ttu-id="4072f-115">Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC wird mit [**ID3DX11EffectPass**](id3dx11effectpass.md) get \* shaderdesc-Methoden verwendet.</span><span class="sxs-lookup"><span data-stu-id="4072f-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="4072f-116">Wenn es sich um eine Inline-shaderzuweisung handelt, ist die zurückgegebene Schnittstelle eine anonyme Shader-Variable, die nicht auf andere Weise abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4072f-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="4072f-117">Der Name in der Variablen Beschreibung lautet "$Anonymous".</span><span class="sxs-lookup"><span data-stu-id="4072f-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="4072f-118">Wenn keine Zuweisung dieses Typs im Pass-Block vorhanden ist, pshadervariable! = **null**, aber pshadervariable->IsValid () = = **false**.</span><span class="sxs-lookup"><span data-stu-id="4072f-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4072f-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4072f-119">Requirements</span></span>



| <span data-ttu-id="4072f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4072f-120">Requirement</span></span> | <span data-ttu-id="4072f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4072f-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4072f-122">Header</span><span class="sxs-lookup"><span data-stu-id="4072f-122">Header</span></span><br/> | <dl> <span data-ttu-id="4072f-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4072f-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4072f-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4072f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4072f-125">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4072f-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

