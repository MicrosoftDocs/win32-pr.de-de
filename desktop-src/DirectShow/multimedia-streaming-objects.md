---
description: Multimedia-Streaming-Objekte
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Multimedia-Streaming-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351688"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="ff147-103">Multimedia-Streaming-Objekte</span><span class="sxs-lookup"><span data-stu-id="ff147-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="ff147-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ff147-104">This API is deprecated.</span></span> <span data-ttu-id="ff147-105">Diese sollten von neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff147-105">New applications should not use it.</span></span>

 

<span data-ttu-id="ff147-106">In der folgenden Tabelle werden die multimediastreaming-Objekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff147-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff147-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="ff147-107">CLSID</span></span></th>
<th><span data-ttu-id="ff147-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff147-108">Description</span></span></th>
<th><span data-ttu-id="ff147-109">Unterstützte Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ff147-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff147-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="ff147-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="ff147-111">Kann für jeden von DirectShow unterstützten Datentyp Medien Beispiele erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff147-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>Iammediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="ff147-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>Imediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="ff147-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="ff147-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff147-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="ff147-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="ff147-117">Implementierung des <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>iaudiodata</strong></a> -audiocontainerobjekts.</span><span class="sxs-lookup"><span data-stu-id="ff147-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>Iaudiodata</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff147-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="ff147-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="ff147-120">DirectDraw-Mediendaten Strom, der einem DirectShow Multimedia-Stream hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff147-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>Iammediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="ff147-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>Imediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="ff147-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>Idirectdrawmediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="ff147-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="ff147-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff147-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="ff147-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="ff147-127">DirectShow-Implementierung von Multimedia-Stream.</span><span class="sxs-lookup"><span data-stu-id="ff147-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>Iammultimediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="ff147-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>Imultimediastream</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff147-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="ff147-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="ff147-131">Stellt über die <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>iammultimediastream</strong></a> -Schnittstelle multimediastreaming-Funktionen für das CLSID_AMMultiMediaStream Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="ff147-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff147-133">–</span><span class="sxs-lookup"><span data-stu-id="ff147-133">N/A</span></span></td>
<td><span data-ttu-id="ff147-134">Beispiele, die vom CLSID_AMMediaTypeStream-Objekt erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ff147-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>Istreamsample</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="ff147-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>Imediasample</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="ff147-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff147-138">–</span><span class="sxs-lookup"><span data-stu-id="ff147-138">N/A</span></span></td>
<td><span data-ttu-id="ff147-139">Beispiele, die vom DirectDraw-Stream erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ff147-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff147-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>Istreamsample</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="ff147-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>Idirectdrawstreamsample</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="ff147-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>Imediasample</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff147-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



