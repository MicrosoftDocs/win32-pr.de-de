---
description: Verwenden der Bump-Zuordnung (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Verwenden der Bump-Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482675"
---
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="c2f97-103">Verwenden der Bump-Zuordnung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c2f97-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="c2f97-104">Unterstützung für die Zuordnung von Bump</span><span class="sxs-lookup"><span data-stu-id="c2f97-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="c2f97-105">Ein Gerät kann eine Zuordnungs Zuordnung durchführen, wenn es entweder den D3DTOP \_ bumpenvmap-oder D3DTOP \_ bumpenvmapluminance-Textur Mischungs Vorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f97-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="c2f97-106">Verwenden Sie [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ Query \_ legacybumpmap, um festzustellen, ob ein Format für die Bump-Zuordnung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f97-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="c2f97-107">Darüber hinaus sollten die Anwendungen die Gerätefunktionen überprüfen, um sicherzustellen, dass das Gerät eine geeignete Anzahl von Mischungs Stufen unterstützt (in der Regel mindestens drei) und mindestens ein "Bump-Mapping"-Pixel Format verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="c2f97-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="c2f97-108">Im folgenden Codebeispiel werden die Gerätefunktionen zum Erkennen der Unterstützung für die Bump-Zuordnung auf dem aktuellen Gerät mithilfe der angegebenen Kriterien überprüft.</span><span class="sxs-lookup"><span data-stu-id="c2f97-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="c2f97-109">Erstellen einer Bump-Karten Textur</span><span class="sxs-lookup"><span data-stu-id="c2f97-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="c2f97-110">Sie erstellen eine Stoß Karten Textur wie jede andere Textur.</span><span class="sxs-lookup"><span data-stu-id="c2f97-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="c2f97-111">Die Anwendung überprüft die Unterstützung für die Zuordnung von Bump und ruft ein gültiges Pixel Format ab, wie unter Erkennen der Unterstützung für die Bump-Zuordnung erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2f97-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="c2f97-112">Nachdem die Oberfläche erstellt wurde, können Sie jedes Pixel mit den entsprechenden Delta Werten und der Leuchtkraft laden, wenn das Oberflächen Format eine Leuchtkraft enthält.</span><span class="sxs-lookup"><span data-stu-id="c2f97-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="c2f97-113">Die Werte für die einzelnen Pixel Komponenten werden in [Bump Map-Pixel Formaten (Direct3D 9)](bump-map-pixel-formats.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2f97-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="c2f97-114">Konfigurieren von Parameter der Bump-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c2f97-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="c2f97-115">Wenn Ihre Anwendung eine Bump Map erstellt und den Inhalt der einzelnen Pixel festgelegt hat, können Sie das Rendering vorbereiten, indem Sie die Parameter für die Bump-Zuordnung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c2f97-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="c2f97-116">Zu den Bump-Zuordnungs Parametern zählen das Festlegen der erforderlichen Texturen und ihrer Mischungs Vorgänge sowie die Transformations-und Leuchtkraft Steuerelemente für die Bump-Karte selbst.</span><span class="sxs-lookup"><span data-stu-id="c2f97-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="c2f97-117">Legen Sie die Basis Textur Map bei Verwendung, Bump Map und Umgebungskarten Texturen in Textur Mischungs Stufen fest.</span><span class="sxs-lookup"><span data-stu-id="c2f97-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="c2f97-118">Legen Sie die Farb-und Alpha Mischungs Vorgänge für jede Textur Phase fest.</span><span class="sxs-lookup"><span data-stu-id="c2f97-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="c2f97-119">Legen Sie die Transformationsmatrix der Bump Map fest.</span><span class="sxs-lookup"><span data-stu-id="c2f97-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="c2f97-120">Legen Sie die Werte für die Glanz Skala und den Offset nach Bedarf fest.</span><span class="sxs-lookup"><span data-stu-id="c2f97-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="c2f97-121">Im folgenden Codebeispiel werden drei Texturen (die Basis Textur Zuordnung, die Bump Map und eine Glanz Umgebungs Zuordnung) zu den entsprechenden Textur Mischungs Stufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2f97-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="c2f97-122">Nachdem Sie die Texturen auf Ihre Mischungs Stufen festgelegt haben, bereitet das folgende Codebeispiel die Mischungs Vorgänge und Argumente für jede Stufe vor.</span><span class="sxs-lookup"><span data-stu-id="c2f97-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



<span data-ttu-id="c2f97-123">Wenn die Mischungs Vorgänge und-Argumente festgelegt sind, wird im folgenden Codebeispiel die 2 x 2-Bump-Zuordnungsmatrix auf die Identitätsmatrix festgelegt, indem die D3DTSS \_ BUMPENVMAPMAT00-und D3DTSS BUMPENVMAPMAT11-Member \_ von [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) auf 1,0 festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="c2f97-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="c2f97-124">Das Festlegen der Matrix auf die Identität bewirkt, dass das System die Delta Werte in der Bump Map unverändert verwendet, dies ist jedoch nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2f97-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



<span data-ttu-id="c2f97-125">Wenn Sie den Vorgang für die Bump-Zuordnung so einrichten, dass Sie "Leuchtkraft (D3DTOP \_ bumpenvmapluminance)" enthält, müssen Sie die Leuchtkraft Steuerelemente festlegen.</span><span class="sxs-lookup"><span data-stu-id="c2f97-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="c2f97-126">Die Beleuchtungs Steuerelemente konfigurieren, wie das System die Leuchtkraft berechnet, bevor Sie die Farbe aus der Textur in der nächsten Phase modulieren.</span><span class="sxs-lookup"><span data-stu-id="c2f97-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="c2f97-127">Weitere Informationen finden Sie unter [Bump Mapping-Formeln (Direct3D 9)](bump-mapping-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="c2f97-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



<span data-ttu-id="c2f97-128">Nachdem die Anwendung die Parameter für die Bump-Zuordnung konfiguriert hat, kann Sie wie gewohnt gerendert werden, und die gerenderten Polygone empfangen die Auswirkungen auf die</span><span class="sxs-lookup"><span data-stu-id="c2f97-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="c2f97-129">Beachten Sie, dass im vorangehenden Beispiel Parameter für die Glanz Umgebungs Zuordnung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c2f97-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="c2f97-130">Beim Durchführen der diffuses Licht Zuordnung legen Anwendungen den Textur Mischungs Vorgang für die letzte Stufe auf D3DTOP \_ modulate fest.</span><span class="sxs-lookup"><span data-stu-id="c2f97-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="c2f97-131">Weitere Informationen finden Sie unter [diffuses Light Maps (Direct3D 9)](diffuse-light-maps.md).</span><span class="sxs-lookup"><span data-stu-id="c2f97-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2f97-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2f97-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2f97-133">Bump-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c2f97-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 
