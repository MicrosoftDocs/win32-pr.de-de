---
title: Direct3D 11 auf downlevelhardware
description: In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware (von DirectX 9 bis DirectX 11) konzipiert ist.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104568430"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="c92db-103">Direct3D 11 auf downlevelhardware</span><span class="sxs-lookup"><span data-stu-id="c92db-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="c92db-104">In diesem Abschnitt wird erläutert, wie Direct3D 11 für die Unterstützung neuer und vorhandener Hardware (von DirectX 9 bis DirectX 11) konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="c92db-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="c92db-105">Dieses Diagramm zeigt, wie Direct3D 11 neue und vorhandene Hardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c92db-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![Diagramm der Hardware, die von Direct3D 11 unterstützt wird](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="c92db-107">Mit Direct3D 11 wird ein neues Paradigma namens Funktionsebenen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c92db-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="c92db-108">Eine Featureebene ist ein gut definierter Satz von GPU-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c92db-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="c92db-109">Mithilfe einer Featureebene können Sie eine Direct3D-Anwendung auf eine downlevelversion von Direct3D-Hardware anwenden.</span><span class="sxs-lookup"><span data-stu-id="c92db-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="c92db-110">Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen</span><span class="sxs-lookup"><span data-stu-id="c92db-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="c92db-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c92db-111">In this section</span></span>



| <span data-ttu-id="c92db-112">Thema</span><span class="sxs-lookup"><span data-stu-id="c92db-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="c92db-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c92db-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c92db-114">Direct3D-Featureebenen</span><span class="sxs-lookup"><span data-stu-id="c92db-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="c92db-115">In diesem Thema werden Direct3D Funktionsebenen erläutert.</span><span class="sxs-lookup"><span data-stu-id="c92db-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="c92db-116">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c92db-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="c92db-117">In diesem Thema werden Ausnahmen bei der Verwendung von Direct3D 11 auf downlevelhardware beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c92db-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="c92db-118">Compute-Shader auf downlevelhardware</span><span class="sxs-lookup"><span data-stu-id="c92db-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="c92db-119">In diesem Thema wird die Verwendung von [Compute-Shadern](direct3d-11-advanced-stages-compute-shader.md) in einer Direct3D 11-App auf Direct3D 10-Hardware erläutert.</span><span class="sxs-lookup"><span data-stu-id="c92db-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="c92db-120">Verhindern unerwünschter NULL-Pixel-Shader-Srvs</span><span class="sxs-lookup"><span data-stu-id="c92db-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="c92db-121">In diesem Thema wird erläutert, wie Sie den Treiber umgehen, der **null** -Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn nicht-**null** -Srvs an die Pixel-Shader-Phase gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="c92db-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="c92db-122">Themen zur Vorgehensweise bei Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="c92db-122">How to topics about feature levels</span></span>



| <span data-ttu-id="c92db-123">Thema</span><span class="sxs-lookup"><span data-stu-id="c92db-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="c92db-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c92db-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c92db-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Gewusst wie: erhalten der Geräte Funktionsebene](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="c92db-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="c92db-126">Erfahren Sie, wie Sie eine Featureebene erhalten.</span><span class="sxs-lookup"><span data-stu-id="c92db-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c92db-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c92db-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c92db-128">Geräte</span><span class="sxs-lookup"><span data-stu-id="c92db-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





