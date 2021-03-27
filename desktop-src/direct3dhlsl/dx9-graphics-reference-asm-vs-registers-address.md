---
title: Adress Register
description: Das a0-Register ist ein Adressregister.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856583"
---
# <a name="address-register"></a><span data-ttu-id="64ca0-103">Adress Register</span><span class="sxs-lookup"><span data-stu-id="64ca0-103">Address Register</span></span>

<span data-ttu-id="64ca0-104">Das a0-Register ist ein Adressregister.</span><span class="sxs-lookup"><span data-stu-id="64ca0-104">The a0 register is an address register.</span></span> <span data-ttu-id="64ca0-105">Ein einzelnes Register ist in Version vs \_ 1 \_ 1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64ca0-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="64ca0-106">Das Adressregister, das als a0. x in vs \_ 1 \_ 1 festgelegt ist, kann als Vorzeichen lose Ganzzahl mit Vorzeichen für die relative Adressierung in die Konstante Register Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64ca0-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="64ca0-107">Für Versionen im Vergleich zu \_ 2 \_ 0 und höher sind alle vier Komponenten (x, y,. z,. w) für die relative Adressierung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64ca0-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="64ca0-108">Das Adressregister kann nicht von einem Vertex-Shader gelesen werden, sondern kann nur für die relative Adressierung eines konstanten Registers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64ca0-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="64ca0-109">Beim Lesen von Werten außerhalb des zulässigen Bereichs wird (0,0, 0,0, 0,0, 0,0) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64ca0-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="64ca0-110">Das Adressregister kann nur ein Ziel für die [MOV-vs-](mov---vs.md) Anweisung sein.</span><span class="sxs-lookup"><span data-stu-id="64ca0-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="64ca0-111">Wenn eine Gleit Komma Zahl in ein ganzzahliges Register verschoben wird, wird eine roundTo-Next-Konvertierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="64ca0-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="64ca0-112">Alle Shader müssen das Adressregister initialisieren, bevor Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="64ca0-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="64ca0-113">Für Version vs \_ 2 \_ 0 und höher kann die [mova-vs-](mova---vs.md) Anweisung einen Gleit Komma Wert in ein Adressregister verschieben.</span><span class="sxs-lookup"><span data-stu-id="64ca0-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="64ca0-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="64ca0-114">Vertex shader versions</span></span> | <span data-ttu-id="64ca0-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="64ca0-115">1\_1</span></span> | <span data-ttu-id="64ca0-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ca0-116">2\_0</span></span> | <span data-ttu-id="64ca0-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="64ca0-117">2\_sw</span></span> | <span data-ttu-id="64ca0-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64ca0-118">2\_x</span></span> | <span data-ttu-id="64ca0-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ca0-119">3\_0</span></span> | <span data-ttu-id="64ca0-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="64ca0-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="64ca0-121">Adress Register</span><span class="sxs-lookup"><span data-stu-id="64ca0-121">Address Register</span></span>       | <span data-ttu-id="64ca0-122">x</span><span class="sxs-lookup"><span data-stu-id="64ca0-122">x</span></span>    | <span data-ttu-id="64ca0-123">x</span><span class="sxs-lookup"><span data-stu-id="64ca0-123">x</span></span>    | <span data-ttu-id="64ca0-124">x</span><span class="sxs-lookup"><span data-stu-id="64ca0-124">x</span></span>     | <span data-ttu-id="64ca0-125">x</span><span class="sxs-lookup"><span data-stu-id="64ca0-125">x</span></span>    | <span data-ttu-id="64ca0-126">x</span><span class="sxs-lookup"><span data-stu-id="64ca0-126">x</span></span>    | <span data-ttu-id="64ca0-127">x</span><span class="sxs-lookup"><span data-stu-id="64ca0-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="64ca0-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64ca0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ca0-129">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="64ca0-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




