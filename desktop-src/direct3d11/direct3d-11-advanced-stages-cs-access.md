---
title: Zugreifen auf Ressourcen
description: Es gibt mehrere Möglichkeiten, auf Ressourcen zuzugreifen.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993495"
---
# <a name="accessing-resources"></a><span data-ttu-id="adb15-103">Zugreifen auf Ressourcen</span><span class="sxs-lookup"><span data-stu-id="adb15-103">Accessing Resources</span></span>

<span data-ttu-id="adb15-104">Es gibt mehrere Möglichkeiten, auf [Ressourcen](overviews-direct3d-11-resources-types.md)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="adb15-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="adb15-105">Unabhängig davon garantiert Direct3D, dass NULL für alle Ressourcen zurückgegeben wird, auf die außerhalb der Grenzen zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="adb15-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="adb15-106">Zugriff nach Byte Offset</span><span class="sxs-lookup"><span data-stu-id="adb15-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="adb15-107">Zugriff nach Index</span><span class="sxs-lookup"><span data-stu-id="adb15-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="adb15-108">Zugriff über die MIPS-Methode</span><span class="sxs-lookup"><span data-stu-id="adb15-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="adb15-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adb15-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="adb15-110">Zugriff nach Byte Offset</span><span class="sxs-lookup"><span data-stu-id="adb15-110">Access By Byte Offset</span></span>

<span data-ttu-id="adb15-111">Auf zwei neue Puffer Typen kann mithilfe eines Byte Offsets zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="adb15-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="adb15-112">[**Byteaddressbuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) ist ein Schreib geschützter Puffer.</span><span class="sxs-lookup"><span data-stu-id="adb15-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="adb15-113">[**Rwbyteaddressbuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) ist ein Lese-oder Schreibpuffer.</span><span class="sxs-lookup"><span data-stu-id="adb15-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="adb15-114">Zugriff nach Index</span><span class="sxs-lookup"><span data-stu-id="adb15-114">Access By Index</span></span>

<span data-ttu-id="adb15-115">Ressourcentypen können einen Index verwenden, um auf eine bestimmte Position in der Ressource zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="adb15-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="adb15-116">Betrachten Sie das folgende Beispiel:</span><span class="sxs-lookup"><span data-stu-id="adb15-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="adb15-117">In diesem Beispiel werden die 4 float-Werte, die an der Position " *POS* " in der Textur Ressource " *MyTexture* 2D" gespeichert sind, der *myVar* -Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="adb15-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="adb15-118">Der Standardwert für den Zugriff auf eine Textur auf diese Weise ist MipMap Level Zero (die ausführlichste Ebene).</span><span class="sxs-lookup"><span data-stu-id="adb15-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="adb15-119">Die Zeile "float4 MyVar = MyTexture \[ POS \] ;" entspricht "float4 MyVar = MyTexture. Load (uint3 (POS, 0));".</span><span class="sxs-lookup"><span data-stu-id="adb15-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="adb15-120">Der Zugriff nach Index ist eine neue HLSL-Syntax Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="adb15-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="adb15-121">Mit dem Compiler in der Version vom Juni 2010 des DirectX SDK und höher können Sie alle Ressourcentypen außer für [Byte Adress Puffer](direct3d-11-advanced-stages-cs-resources.md)indizieren.</span><span class="sxs-lookup"><span data-stu-id="adb15-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="adb15-122">Mit dem Compiler vom Juni 2010 und höher können Sie lokale Ressourcenvariablen deklarieren.</span><span class="sxs-lookup"><span data-stu-id="adb15-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="adb15-123">Sie können diesen Variablen global definierte Ressourcen (z. b. *MyTexture*) zuweisen und Sie auf die gleiche Weise wie Ihre globalen Gegenstücke verwenden.</span><span class="sxs-lookup"><span data-stu-id="adb15-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="adb15-124">Zugriff über die MIPS-Methode</span><span class="sxs-lookup"><span data-stu-id="adb15-124">Access By Mips Method</span></span>

<span data-ttu-id="adb15-125">Textur Objekte verfügen über eine **MIPS** -Methode (z [**. b. Texture2D. mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), die Sie verwenden können, um die MipMap-Ebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="adb15-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="adb15-126">In diesem Beispiel wird die Farbe, die unter (7, 16) auf MipMap-Ebene 2 gespeichert ist, in einer 2D-Textur gelesen:</span><span class="sxs-lookup"><span data-stu-id="adb15-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="adb15-127">Dies ist eine Erweiterung des Compilers vom Juni 2010 und höher.</span><span class="sxs-lookup"><span data-stu-id="adb15-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="adb15-128">Der Ausdruck "MyTexture. mips \[ 2 \] \[ uint2 (x, y) \] " entspricht "MyTexture. Load (uint3 (x, y, 2))".</span><span class="sxs-lookup"><span data-stu-id="adb15-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="adb15-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adb15-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adb15-130">Übersicht über Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="adb15-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 