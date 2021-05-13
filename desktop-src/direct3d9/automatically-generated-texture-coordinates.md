---
title: Automatisch generierte Texturkoordinaten (Direct3D 9)
description: Das System kann die transformierte Kameraraumposition oder die Normalität aus einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Elementvektoren berechnen, die zum Adressieren einer kubischen Umgebungskarte verwendet werden.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843291"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="0ee65-103">Automatisch generierte Texturkoordinaten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ee65-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="0ee65-104">Das System kann die transformierte Kameraraumposition oder die Normalität aus einem Scheitelpunkt als Texturkoordinaten verwenden oder die drei Elementvektoren berechnen, die zum Adressieren einer kubischen Umgebungskarte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ee65-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="0ee65-105">Wie Texturkoordinaten, die Sie explizit in einem Scheitelpunkt angeben, können Sie automatisch generierte Texturkoordinaten als Eingabe für Texturkoordinatentransformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ee65-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="0ee65-106">Automatisch generierte Texturkoordinaten können die für Geometriedaten erforderliche Bandbreite erheblich reduzieren, da keine expliziten Texturkoordinaten im Scheitelpunktformat erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0ee65-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="0ee65-107">In vielen Fällen können die Texturkoordinaten, die das System generiert, mit Transformationen verwendet werden, um spezielle Effekte zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="0ee65-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="0ee65-108">Dies ist natürlich ein spezielles Feature, und Sie verwenden in vielen Fällen explizite Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="0ee65-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="0ee65-109">Konfigurieren automatisch generierter Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="0ee65-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="0ee65-110">In C++ steuert der Texturphasenzustand D3DTSS \_ TEXCOORDINDEX (aus dem [**enumerationierten D3DTEXTURESTAGESTATETYPE-Typ),**](./d3dtexturestagestatetype.md) wie das System Texturkoordinaten generiert.</span><span class="sxs-lookup"><span data-stu-id="0ee65-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="0ee65-111">Normalerweise weist dieser Zustand das System an, einen bestimmten Satz von Texturkoordinaten zu verwenden, die im Scheitelpunktformat codiert sind.</span><span class="sxs-lookup"><span data-stu-id="0ee65-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="0ee65-112">Wenn Sie die TCI-Flags D3DTSS \_ \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION oder D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR in den Wert einschließen, den Sie diesem Zustand zuweisen, unterscheidet sich das Systemverhalten erheblich.</span><span class="sxs-lookup"><span data-stu-id="0ee65-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="0ee65-113">Wenn eines dieser Flags vorhanden ist, ignoriert die Texturphase die Texturkoordinaten im Scheitelpunktformat zugunsten von Koordinaten, die das System generiert.</span><span class="sxs-lookup"><span data-stu-id="0ee65-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="0ee65-114">Die Bedeutungen der einzelnen Flags werden in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ee65-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="0ee65-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="0ee65-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="0ee65-116">Verwenden Sie den Scheitelpunkt normal, transformiert in den Kameraraum, als Eingabetexturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="0ee65-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="0ee65-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="0ee65-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="0ee65-118">Verwenden Sie die Scheitelpunktposition, transformiert in den Kameraraum, als Eingabetexturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="0ee65-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="0ee65-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="0ee65-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="0ee65-120">Verwenden Sie den Reflektionsvektor, der in den Kameraraum transformiert wird, als Eingabetexturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="0ee65-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="0ee65-121">Der Reflektionsvektor wird aus der Position des Eingabe-Scheitelpunkts und dem normalen Vektor berechnet.</span><span class="sxs-lookup"><span data-stu-id="0ee65-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="0ee65-122">Die Texturkoordinatenindexflags schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="0ee65-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="0ee65-123">In diesem Beispiel wird Folgendes verwendet:</span><span class="sxs-lookup"><span data-stu-id="0ee65-123">This example uses:</span></span>

-   <span data-ttu-id="0ee65-124">Die Scheitelpunktposition (im Kameraraum) als Eingabetexturkoordinaten für diese Texturphase</span><span class="sxs-lookup"><span data-stu-id="0ee65-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="0ee65-125">Der im D3DRENDERSTATE WRAP1-Renderzustand festgelegte \_ Wrap-Modus</span><span class="sxs-lookup"><span data-stu-id="0ee65-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="0ee65-126">Automatisch generierte Texturkoordinaten sind am nützlichsten als Eingabewerte für eine Texturkoordinatentransformation oder um zu vermeiden, dass Ihre Anwendung dreielementige Vektoren für kubische Umgebungszuordnungen berechnen muss.</span><span class="sxs-lookup"><span data-stu-id="0ee65-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="0ee65-127">Bei der Kugelzuordnung wird eine vorbesetzte Texturzuordnung (zur Modellzeit) verwendet, die die gesamte Umgebung enthält, wie durch eine Chrome-Kugel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0ee65-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="0ee65-128">Direct3D verfügt über ein Texturkoordinatengenerierungsfeature unter Verwendung des Renderzustands D3DTSS \_ TCI CAMERASPACENORMAL, das den Normalwert des Scheitelpunkts im Kameraraum übernimmt und durch eine Texturtransformation versetzt, um Texturkoordinaten zu \_ generieren.</span><span class="sxs-lookup"><span data-stu-id="0ee65-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ee65-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ee65-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ee65-130">Texturkoordinatenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="0ee65-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="0ee65-131">Texturkoordinatentransformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ee65-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="0ee65-132">Kubische Umgebungszuordnung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ee65-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
