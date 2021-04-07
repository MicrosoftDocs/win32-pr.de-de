---
description: Anforderung für eine gekachelte Textur, die als DDS-Datei geschrieben werden soll.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Itilerequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746801"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span data-ttu-id="f436d-103"><span id="vspixengine.itilerequest"></span>Itilerequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f436d-103"><span id="vspixengine.itilerequest"></span>ITileRequest interface</span></span>

<span data-ttu-id="f436d-104">Anforderung für eine gekachelte Textur, die als DDS-Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f436d-104">Request for a tiled texture to be written as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="f436d-105">Member</span><span class="sxs-lookup"><span data-stu-id="f436d-105">Members</span></span>

<span data-ttu-id="f436d-106">Die **itilerequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f436d-106">The **ITileRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f436d-107">**Itilerequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f436d-107">**ITileRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="f436d-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f436d-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f436d-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="f436d-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f436d-110">Die **itilerequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f436d-110">The **ITileRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f436d-111">Methode</span><span class="sxs-lookup"><span data-stu-id="f436d-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f436d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f436d-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f436d-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>Requestbuffertileasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="f436d-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f436d-114">Fordert an, den Rohinhalt einer Kachel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f436d-114">Requests to get the raw contents of a tile.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f436d-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>Requesttexturetileasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="f436d-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f436d-116">Fordert an, den Inhalt einer gekachelten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="f436d-116">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f436d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f436d-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f436d-118">Header</span><span class="sxs-lookup"><span data-stu-id="f436d-118">Header</span></span></p></td><td><span data-ttu-id="f436d-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f436d-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
