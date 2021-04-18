---
description: Diese Flags bieten zusätzliche Informationen zu Effekt Parametern.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371923"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="0ab06-103">D3DX- \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="0ab06-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="0ab06-104">Diese Flags bieten zusätzliche Informationen zu Effekt Parametern.</span><span class="sxs-lookup"><span data-stu-id="0ab06-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="0ab06-105">Effektparameter Konstanten werden von [**D3DXPARAMETER- \_**](d3dxparameter-desc.md)Elementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ab06-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="0ab06-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="0ab06-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="0ab06-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ab06-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="0ab06-108"><dt>**D3DX- \_ Parameter \_ Anmerkung**</dt></span><span class="sxs-lookup"><span data-stu-id="0ab06-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="0ab06-109">Dieser Parameter ist als Anmerkung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0ab06-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="0ab06-110">Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit Anmerkungen](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="0ab06-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="0ab06-111"><dt>**D3DX \_ \_ Parameterliterale**</dt></span><span class="sxs-lookup"><span data-stu-id="0ab06-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="0ab06-112">Dieser Parameter ist als Literalwert gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0ab06-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="0ab06-113">Literalparameter können nach der Kompilierung nicht geändert werden, sodass der Compiler seine Verwendung optimieren kann.</span><span class="sxs-lookup"><span data-stu-id="0ab06-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="0ab06-114">Freigegebene Parameter können nicht als Literale gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="0ab06-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="0ab06-115">Weitere Informationen finden Sie unter [Verwendungen und Literale (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="0ab06-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="0ab06-116"><dt>**D3DX- \_ Parameter frei \_ gegeben**</dt></span><span class="sxs-lookup"><span data-stu-id="0ab06-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="0ab06-117">Der Wert eines Parameters wird von allen Effekten im gleichen Namespace gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="0ab06-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="0ab06-118">Wenn Sie den Wert in einem Effekt ändern, wird er in allen gemeinsam genutzten Effekten geändert.</span><span class="sxs-lookup"><span data-stu-id="0ab06-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="0ab06-119">Siehe [Freigabe Parameter](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="0ab06-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="0ab06-120">**D3DX \_ Der frei \_ gegebene Parameter** kann nicht mit der **D3DX- \_ Parameter \_ Literale** oder der **D3DX- \_ Parameter \_ Anmerkung** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="0ab06-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0ab06-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ab06-121">Requirements</span></span>



| <span data-ttu-id="0ab06-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ab06-122">Requirement</span></span> | <span data-ttu-id="0ab06-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0ab06-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab06-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ab06-124">Header</span></span><br/> | <dl> <span data-ttu-id="0ab06-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab06-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ab06-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ab06-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab06-127">Effekt Konstanten</span><span class="sxs-lookup"><span data-stu-id="0ab06-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




