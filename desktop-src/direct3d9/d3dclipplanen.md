---
description: Definiert Bitmuster, die benutzerdefinierte Clippingebenen ermöglichen. Diese Makros sind beim Festlegen von Werten für den D3DRS clipplaneenable-Rendering als benutzerfreundlicher Definition definiert \_ .
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: D3DCLIPPLANEn-Makro (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394086"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="40aea-104">D3DCLIPPLANEn-Makro</span><span class="sxs-lookup"><span data-stu-id="40aea-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="40aea-105">Definiert Bitmuster, die benutzerdefinierte Clippingebenen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="40aea-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="40aea-106">Diese Makros sind beim Festlegen von Werten für den D3DRS clipplaneenable-Rendering als benutzerfreundlicher Definition definiert \_ .</span><span class="sxs-lookup"><span data-stu-id="40aea-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="40aea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40aea-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="40aea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40aea-108">Parameters</span></span>

<span data-ttu-id="40aea-109">Dieses Makro weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="40aea-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40aea-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40aea-110">Return value</span></span>

<span data-ttu-id="40aea-111">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="40aea-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40aea-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40aea-112">Remarks</span></span>

<span data-ttu-id="40aea-113">Benutzerdefinierte Clippingebenen werden aktiviert, wenn der im D3DRS \_ clipplaneenable-renderzustand festgelegte Wert mindestens ein Set Bits enthält (d. h. ist nicht 0).</span><span class="sxs-lookup"><span data-stu-id="40aea-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="40aea-114">Der Wert des "Rendering-State" ist nicht wichtig. der Wert wird vom System nicht als Zahl interpretiert.</span><span class="sxs-lookup"><span data-stu-id="40aea-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="40aea-115">Stattdessen aktiviert der Wert die Clipping-Ebene, deren entsprechendes Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40aea-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="40aea-116">Mit Bit 0 wird der Zustand der ersten Clippingebene (bei Index 0), Bit 1 der zweiten Ebene usw. gesteuert.</span><span class="sxs-lookup"><span data-stu-id="40aea-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="40aea-117">Die von diesen Makros erstellten Bitmuster können mithilfe eines logischen OR-Vorgangs kombiniert werden, um mehrere Clippingebenen gleichzeitig zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="40aea-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="40aea-118">Wenn Sie eines dieser Makros aus der Kombination weglassen, wird die Clippingebene an diesem Index deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="40aea-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="40aea-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40aea-119">Requirements</span></span>



| <span data-ttu-id="40aea-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40aea-120">Requirement</span></span> | <span data-ttu-id="40aea-121">Wert</span><span class="sxs-lookup"><span data-stu-id="40aea-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40aea-122">Header</span><span class="sxs-lookup"><span data-stu-id="40aea-122">Header</span></span><br/> | <dl> <span data-ttu-id="40aea-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="40aea-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40aea-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40aea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40aea-125">Makros</span><span class="sxs-lookup"><span data-stu-id="40aea-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




