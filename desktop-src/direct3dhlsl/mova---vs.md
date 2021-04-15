---
title: vs
description: Verschieben Sie Daten aus einer Gleit Komma Registrierung in das Adressregister a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976473"
---
# <a name="mova---vs"></a><span data-ttu-id="d305e-103">vs</span><span class="sxs-lookup"><span data-stu-id="d305e-103">mova - vs</span></span>

<span data-ttu-id="d305e-104">Verschieben Sie Daten aus einer Gleit Komma Registrierung in das [Adressregister](dx9-graphics-reference-asm-vs-registers-address.md)a0.</span><span class="sxs-lookup"><span data-stu-id="d305e-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="d305e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d305e-105">Syntax</span></span>



| <span data-ttu-id="d305e-106">MUVA DST, src</span><span class="sxs-lookup"><span data-stu-id="d305e-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="d305e-107">where</span><span class="sxs-lookup"><span data-stu-id="d305e-107">where</span></span>

-   <span data-ttu-id="d305e-108">DST muss das [Adress Register](dx9-graphics-reference-asm-vs-registers-address.md)(a0) sein.</span><span class="sxs-lookup"><span data-stu-id="d305e-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="d305e-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="d305e-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d305e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d305e-110">Remarks</span></span>



| <span data-ttu-id="d305e-111">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="d305e-111">Vertex shader versions</span></span> | <span data-ttu-id="d305e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="d305e-112">1\_1</span></span> | <span data-ttu-id="d305e-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d305e-113">2\_0</span></span> | <span data-ttu-id="d305e-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d305e-114">2\_x</span></span> | <span data-ttu-id="d305e-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d305e-115">2\_sw</span></span> | <span data-ttu-id="d305e-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d305e-116">3\_0</span></span> | <span data-ttu-id="d305e-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d305e-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d305e-118">der ANWA</span><span class="sxs-lookup"><span data-stu-id="d305e-118">mova</span></span>                   |      | <span data-ttu-id="d305e-119">x</span><span class="sxs-lookup"><span data-stu-id="d305e-119">x</span></span>    | <span data-ttu-id="d305e-120">x</span><span class="sxs-lookup"><span data-stu-id="d305e-120">x</span></span>    | <span data-ttu-id="d305e-121">x</span><span class="sxs-lookup"><span data-stu-id="d305e-121">x</span></span>     | <span data-ttu-id="d305e-122">x</span><span class="sxs-lookup"><span data-stu-id="d305e-122">x</span></span>    | <span data-ttu-id="d305e-123">x</span><span class="sxs-lookup"><span data-stu-id="d305e-123">x</span></span>     |



 

<span data-ttu-id="d305e-124">Verschiebt Gleit Komma Daten in ein ganzzahliges Register.</span><span class="sxs-lookup"><span data-stu-id="d305e-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="d305e-125">Die Werte werden von Gleit Komma Zahlen mit Rundung zum nächsten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d305e-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="d305e-126">Das Adressregister ist das einzige zulässige Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="d305e-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="d305e-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d305e-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="d305e-128">Bei den Versionen 2 \_ x und höher ist das Adressregister ein Komponenten Vektor.</span><span class="sxs-lookup"><span data-stu-id="d305e-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="d305e-129">Daher ist jede Schreib Maske zulässig.</span><span class="sxs-lookup"><span data-stu-id="d305e-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="d305e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d305e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d305e-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="d305e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




