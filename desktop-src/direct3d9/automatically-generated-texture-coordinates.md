---
title: Automatisch generierte Texturkoordinaten (Direct3D 9)
description: Das System kann die transformierte Position des Kamera Raums oder das normale von einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Element Vektoren berechnen, die zum Adressieren einer kubischen Umgebungs Zuordnung verwendet werden.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338924"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="f988a-103">Automatisch generierte Texturkoordinaten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f988a-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="f988a-104">Das System kann die transformierte Position des Kamera Raums oder das normale von einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Element Vektoren berechnen, die zum Adressieren einer kubischen Umgebungs Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f988a-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="f988a-105">Wie bei Texturkoordinaten, die Sie explizit in einem Scheitelpunkt angeben, können Sie automatisch generierte Texturkoordinaten als Eingabe für Texturkoordinaten Transformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f988a-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="f988a-106">Automatisch generierte Texturkoordinaten können die für Geometriedaten erforderliche Bandbreite erheblich reduzieren, da explizite Texturkoordinaten im Scheitelpunkt Format vermieden werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f988a-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="f988a-107">In vielen Fällen können die vom System generierten Texturkoordinaten mit Transformationen verwendet werden, um besondere Effekte zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="f988a-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="f988a-108">Natürlich handelt es sich hierbei um ein spezielles Feature, das Sie in vielen Fällen explizite Texturkoordinaten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f988a-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="f988a-109">Konfigurieren automatisch generierter Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="f988a-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="f988a-110">In C++ steuert der D3DTSS \_ texcoordindex Texture-Stage State (aus dem [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) -Enumerationstyp), wie das System Texturkoordinaten generiert.</span><span class="sxs-lookup"><span data-stu-id="f988a-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="f988a-111">Normalerweise weist dieser Zustand das System an, einen bestimmten Satz von Texturkoordinaten zu verwenden, die im Scheitelpunkt Format codiert sind.</span><span class="sxs-lookup"><span data-stu-id="f988a-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="f988a-112">Wenn Sie die Flags D3DTSS \_ TCI \_ cameraspacenormal, D3DTSS \_ TCI \_ cameraspaceposition oder D3DTSS \_ TCI \_ cameraspacereflectionvector in den Wert einschließen, den Sie diesem Zustand zuweisen, ist das Systemverhalten sehr unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="f988a-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="f988a-113">Wenn eines dieser Flags vorhanden ist, ignoriert die Textur Phase die Texturkoordinaten innerhalb des Vertex-Formats zugunsten der vom System generierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="f988a-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="f988a-114">Die Bedeutung für jedes Flag ist in der folgenden Liste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f988a-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="f988a-115">D3DTSS \_ TCI \_ cameraspacenormal</span><span class="sxs-lookup"><span data-stu-id="f988a-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="f988a-116">Verwenden Sie den Vertex normal als Eingabe Texturkoordinaten, der in den Kamerabereich transformiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f988a-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="f988a-117">D3DTSS \_ TCI \_ cameraspaceposition</span><span class="sxs-lookup"><span data-stu-id="f988a-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="f988a-118">Verwenden Sie die Vertex-Position, die in den Kamerabereich transformiert wird, als Eingabe Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f988a-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="f988a-119">D3DTSS \_ TCI \_ cameraspacereflectionvector</span><span class="sxs-lookup"><span data-stu-id="f988a-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="f988a-120">Verwenden Sie den reflektionvektor, transformiert in den Kamera Raum, als Eingabe Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f988a-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="f988a-121">Der reflektionvektor wird aus der eintexposition der Eingabe und dem normalen Vektor berechnet.</span><span class="sxs-lookup"><span data-stu-id="f988a-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="f988a-122">Die Flags für Texturkoordinaten Indizes schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="f988a-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="f988a-123">In diesem Beispiel wird Folgendes verwendet:</span><span class="sxs-lookup"><span data-stu-id="f988a-123">This example uses:</span></span>

-   <span data-ttu-id="f988a-124">Die Scheitelpunkt Position (im Kamera Zeichen) als Eingabe Texturkoordinaten für diese Textur Phase.</span><span class="sxs-lookup"><span data-stu-id="f988a-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="f988a-125">Der im D3DRENDERSTATE WRAP1-renderzustand festgelegte Wrap-Modus. \_</span><span class="sxs-lookup"><span data-stu-id="f988a-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="f988a-126">Automatisch generierte Texturkoordinaten sind besonders nützlich als Eingabewerte für eine Texturkoordinaten Transformation oder, um zu vermeiden, dass Ihre Anwendung drei-Element-Vektoren für kubische Umgebungs Zuordnungen berechnen muss.</span><span class="sxs-lookup"><span data-stu-id="f988a-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="f988a-127">Kugel Zuordnung verwendet eine vorberechnete Textur Zuordnung (zur Modell Zeit), die die gesamte Umgebung enthält, wie Sie von einer Chrome-Kugel reflektiert wird.</span><span class="sxs-lookup"><span data-stu-id="f988a-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="f988a-128">Direct3D verfügt über eine Textur Koordinate-Generierungs Funktion, die den renderzustand D3DTSS \_ TCI \_ cameraspacenormal verwendet, der die normale des Scheitel Punkts im Kamerabereich einnimmt und eine Textur Transformation zum Generieren von Texturkoordinaten einfügt.</span><span class="sxs-lookup"><span data-stu-id="f988a-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f988a-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f988a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f988a-130">Verarbeitung von Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="f988a-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="f988a-131">Transformationen für Texturkoordinaten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f988a-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="f988a-132">Kubische Umgebungs Zuordnung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f988a-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
