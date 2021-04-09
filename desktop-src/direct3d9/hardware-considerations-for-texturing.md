---
description: Die aktuelle Hardware implementiert nicht notwendigerweise alle Funktionen, die von der Direct3D-Schnittstelle aktiviert werden. Die Anwendung muss die Benutzer Hardware testen und die renderingstrategien entsprechend anpassen.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Überlegungen zur Hardware für die Texturierung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859942"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="9c9d2-104">Überlegungen zur Hardware für die Texturierung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9c9d2-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="9c9d2-105">Die aktuelle Hardware implementiert nicht notwendigerweise alle Funktionen, die von der Direct3D-Schnittstelle aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="9c9d2-106">Die Anwendung muss die Benutzer Hardware testen und die renderingstrategien entsprechend anpassen.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="9c9d2-107">Viele 3D-Zugriffstasten bieten keine Unterstützung für diffuse Iterierte Werte als Argumente für das Mischen von Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="9c9d2-108">Die Anwendung kann jedoch Iterierte Farbdaten einführen, wenn Sie Textur Mischungs Vorgänge durchführt.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="9c9d2-109">Bei einigen 3D-Hardware ist möglicherweise keine Mischungs Stufe mit der ersten Textur verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="9c9d2-110">Auf diesen Adaptern muss Ihre Anwendung in den zweiten und dritten Textur Stufen in der Menge der aktuellen Texturen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="9c9d2-111">Aufgrund von Einschränkungen in der heutigen Hardware können einige Anzeige Adapter eine drei lineare MipMap-interpolung durch die von [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)angebotene Schnittstelle für mehrere Textur blending ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="9c9d2-112">Die Anwendung kann Multipass-Textur Mischungs Zeichen verwenden, um die gleichen Effekte zu erzielen, oder Sie wird auf den D3DTEXF \_ Point Mipmap-Filter Modus herabgestuft, der häufig unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9c9d2-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c9d2-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c9d2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c9d2-114">Direct3D-Texturen</span><span class="sxs-lookup"><span data-stu-id="9c9d2-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
