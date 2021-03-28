---
title: Eingabe Farb Register
description: Ein Pixel-Shader-Eingabe Register, das Vertexfarbe enthält.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388793"
---
# <a name="input-color-register"></a><span data-ttu-id="ea9a7-103">Eingabe Farb Register</span><span class="sxs-lookup"><span data-stu-id="ea9a7-103">Input Color Register</span></span>

<span data-ttu-id="ea9a7-104">Ein Pixel-Shader-Eingabe Register, das Vertexfarbe enthält.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea9a7-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="ea9a7-106">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="ea9a7-106">where:</span></span>

-   <span data-ttu-id="ea9a7-107">[DCL-(SM2, SM3-PS ASM)](dcl---ps.md) ist eine Register Deklarations Anweisung.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="ea9a7-108">v ist ein Eingabe Register und \# ist die Registernummer.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="ea9a7-109">Die Anzahl der zulässigen Register wird durch die Shader-Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="ea9a7-110">der Schreibzugriff bestimmt, welche Komponenten (bis zu vier) geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="ea9a7-111">Gültige Komponenten sind: (x, y, z, w) oder (r, g, b, a).</span><span class="sxs-lookup"><span data-stu-id="ea9a7-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9a7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea9a7-112">Remarks</span></span>

<span data-ttu-id="ea9a7-113">Farbregister sind schreibgeschützte Register.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-113">Color registers are read-only registers.</span></span> <span data-ttu-id="ea9a7-114">Jedes Register enthält aus Eingabe Scheitel Punkten durch Iterierte RGBA-Werte mit vier Komponenten.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="ea9a7-115">Sie haben niedrigere Genauigkeit als die meisten Register, und es sind garantiert 8 Bits unsignierter Daten im Bereich (0, + 1) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="ea9a7-116">Sie können nicht mehr als eine Anweisung in einer einzigen Anweisung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea9a7-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea9a7-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea9a7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea9a7-118">Register</span><span class="sxs-lookup"><span data-stu-id="ea9a7-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="ea9a7-119">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register</span><span class="sxs-lookup"><span data-stu-id="ea9a7-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="ea9a7-120">PS \_ 2 \_ 0-Register</span><span class="sxs-lookup"><span data-stu-id="ea9a7-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="ea9a7-121">PS \_ 2 \_ x-Register</span><span class="sxs-lookup"><span data-stu-id="ea9a7-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="ea9a7-122">PS \_ 3 \_ 0-Register</span><span class="sxs-lookup"><span data-stu-id="ea9a7-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




