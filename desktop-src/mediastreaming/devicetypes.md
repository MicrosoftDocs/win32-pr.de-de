---
title: Debug Type-Enumeration
description: Beschreibt die DLNA-Gerätetypen, die von der Media Streaming-API unterstützt werden.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Geräte-Streaming-API der Geräte-Enumeration
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361262"
---
# <a name="devicetypes-enumeration"></a><span data-ttu-id="68ae7-104">Debug Type-Enumeration</span><span class="sxs-lookup"><span data-stu-id="68ae7-104">DeviceTypes enumeration</span></span>

<span data-ttu-id="68ae7-105">Beschreibt die DLNA-Gerätetypen, die von der Media Streaming-API unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="68ae7-105">Describes the DLNA device types that are supported by the Media Streaming API.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ae7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ae7-106">Syntax</span></span>


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a><span data-ttu-id="68ae7-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="68ae7-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="68ae7-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="68ae7-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="68ae7-109">Unbekannter Gerätetyp.</span><span class="sxs-lookup"><span data-stu-id="68ae7-109">Unknown device type.</span></span>

</dd> <dt>

<span data-ttu-id="68ae7-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**Digitalmediarenderer**</span><span class="sxs-lookup"><span data-stu-id="68ae7-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span></span>
</dt> <dd>

<span data-ttu-id="68ae7-111">DLNA Digital Media-Renderer (DMR).</span><span class="sxs-lookup"><span data-stu-id="68ae7-111">DLNA Digital Media Renderer (DMR).</span></span> <span data-ttu-id="68ae7-112">Der Wert entspricht dem Gerätetyp **urn: Schemas-UPnP-org: Device: MediaRenderer: 1**.</span><span class="sxs-lookup"><span data-stu-id="68ae7-112">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaRenderer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="68ae7-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**Digitalmediaserver**</span><span class="sxs-lookup"><span data-stu-id="68ae7-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span></span>
</dt> <dd>

<span data-ttu-id="68ae7-114">DLNA Digital Media-Server (DMS).</span><span class="sxs-lookup"><span data-stu-id="68ae7-114">DLNA Digital Media Server (DMS).</span></span> <span data-ttu-id="68ae7-115">Der Wert entspricht dem Gerätetyp **urn: Schemas-UPnP-org: Device: Mediaserver: 1**.</span><span class="sxs-lookup"><span data-stu-id="68ae7-115">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaServer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="68ae7-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**Digitalmediaplayer**</span><span class="sxs-lookup"><span data-stu-id="68ae7-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span></span>
</dt> <dd>

<span data-ttu-id="68ae7-117">Digitaler DLNA-Media Player</span><span class="sxs-lookup"><span data-stu-id="68ae7-117">DLNA Digital Media Player</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68ae7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68ae7-118">Requirements</span></span>



| <span data-ttu-id="68ae7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68ae7-119">Requirement</span></span> | <span data-ttu-id="68ae7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="68ae7-120">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ae7-121">IDL</span><span class="sxs-lookup"><span data-stu-id="68ae7-121">IDL</span></span><br/> | <dl> <span data-ttu-id="68ae7-122"><dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="68ae7-122"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





