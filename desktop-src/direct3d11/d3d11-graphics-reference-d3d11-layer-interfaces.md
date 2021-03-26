---
title: Ebenenschnittstellen
description: Dieser Abschnitt enthält Informationen zu den ebenenschnittstellen.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- Schnittstellen, Direct3D 11-Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993638"
---
# <a name="layer-interfaces"></a><span data-ttu-id="14771-104">Ebenenschnittstellen</span><span class="sxs-lookup"><span data-stu-id="14771-104">Layer Interfaces</span></span>

<span data-ttu-id="14771-105">Dieser Abschnitt enthält Informationen zu den ebenenschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="14771-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="14771-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="14771-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14771-107">Thema</span><span class="sxs-lookup"><span data-stu-id="14771-107">Topic</span></span></th>
<th><span data-ttu-id="14771-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14771-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14771-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="14771-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="14771-110">Eine Debug-Schnittstelle steuert Debugeinstellungen und überprüft den Pipeline Status und kann nur verwendet werden, wenn die debugschicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="14771-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14771-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="14771-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="14771-112">Eine Informations Warteschlangen Schnittstelle speichert, ruft Debugmeldungen ab und filtert sie.</span><span class="sxs-lookup"><span data-stu-id="14771-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="14771-113">Die Warteschlange besteht aus einer Nachrichten Warteschlange, einem optionalen Speicher Filter Stapel und einem optionalen Abruf Filter Stapel.</span><span class="sxs-lookup"><span data-stu-id="14771-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14771-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="14771-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="14771-115">Die Standard-nach Verfolgungs Schnittstelle legt Standard Überwachungs Optionen für Verweise fest.</span><span class="sxs-lookup"><span data-stu-id="14771-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14771-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="14771-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="14771-117">Die nach Verfolgungs Schnittstelle legt Optionen für die Verweis Verfolgung fest.</span><span class="sxs-lookup"><span data-stu-id="14771-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14771-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="14771-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="14771-119">Die <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> -Schnittstelle und ihre Methoden werden in Direct3D 11 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14771-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14771-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="14771-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="14771-121">Die Ablaufverfolgungs-Geräteschnittstelle legt Shader-Überwachungsinformationen fest, die eine genaue Protokollierung und Wiedergabe der shaderausführung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="14771-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="14771-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14771-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14771-123">Ebenenverweis</span><span class="sxs-lookup"><span data-stu-id="14771-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





