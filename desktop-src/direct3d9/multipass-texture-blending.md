---
description: Direct3D-Anwendungen können zahlreiche besondere Effekte erzielen, indem Sie im Verlauf mehrerer Renderingdurchläufen verschiedene Texturen auf ein primitiv anwenden.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Multipass-Textur Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124472"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="21afb-103">Multipass-Textur Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="21afb-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="21afb-104">Direct3D-Anwendungen können zahlreiche besondere Effekte erzielen, indem Sie im Verlauf mehrerer Renderingdurchläufen verschiedene Texturen auf ein primitiv anwenden.</span><span class="sxs-lookup"><span data-stu-id="21afb-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="21afb-105">Der allgemeine Begriff hierfür ist Multipass-Textur Mischung.</span><span class="sxs-lookup"><span data-stu-id="21afb-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="21afb-106">Eine typische Verwendung von Multipass-Textur Mischungs Modellen besteht darin, die Auswirkungen komplexer Beleuchtungs-und Schattierungs Modelle durch Anwenden mehrerer Farben aus verschiedenen Texturen zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="21afb-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="21afb-107">Eine solche Anwendung wird als "Light Mapping" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="21afb-107">One such application is called light mapping.</span></span> <span data-ttu-id="21afb-108">Weitere Informationen finden Sie unter [Light Mapping with Texturen (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="21afb-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="21afb-109">Einige Geräte können in einem einzigen Durchlauf mehrere Texturen auf primitive anwenden.</span><span class="sxs-lookup"><span data-stu-id="21afb-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="21afb-110">Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="21afb-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="21afb-111">Wenn die Hardware des Benutzers mehrere Textur Mischungs Möglichkeiten nicht unterstützt, kann die Anwendung Multipass-Textur blending verwenden, um die gleichen visuellen Effekte zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="21afb-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="21afb-112">Die Anwendung kann jedoch nicht die Frameraten unterstützen, die bei Verwendung mehrerer Textur Mischungs Möglichkeiten möglich sind.</span><span class="sxs-lookup"><span data-stu-id="21afb-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="21afb-113">Zum Durchführen einer Multipass-Textur Mischung in einer C/C++-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="21afb-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="21afb-114">Legen Sie eine Textur in Textur Phase 0 fest, indem Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21afb-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="21afb-115">Wählen Sie die gewünschte Farbe und Alpha Mischung aus Argumenten und Vorgängen mit der [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) -Methode aus.</span><span class="sxs-lookup"><span data-stu-id="21afb-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="21afb-116">Die Standardeinstellungen eignen sich gut für Multipass-Textur Mischungs.</span><span class="sxs-lookup"><span data-stu-id="21afb-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="21afb-117">Rendering der entsprechenden Objekte in der Szene.</span><span class="sxs-lookup"><span data-stu-id="21afb-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="21afb-118">Legen Sie die nächste Textur in der Textur Phase 0 fest.</span><span class="sxs-lookup"><span data-stu-id="21afb-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="21afb-119">Legen Sie die \_ Rendering-Zustände D3DRS srcblend und D3DRS \_ destblend so fest, dass die Quell-und Ziel-Mischungs Faktoren bei Bedarf angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="21afb-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="21afb-120">Das System kombiniert die neuen Texturen mit den vorhandenen Pixeln auf der renderzieloberfläche gemäß diesen Parametern.</span><span class="sxs-lookup"><span data-stu-id="21afb-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="21afb-121">Wiederholen Sie die Schritte 3, 4 und 5 mit beliebig vielen Texturen.</span><span class="sxs-lookup"><span data-stu-id="21afb-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21afb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21afb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21afb-123">Textur Mischung</span><span class="sxs-lookup"><span data-stu-id="21afb-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
