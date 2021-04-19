---
title: Transportstatus-Enumeration
description: Definiert den verfügbaren Transport Status gemäß den UPnP-Richtlinien.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- Transportstatus-Enumeration Medien Streaming-API
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362129"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="2ef00-104">Transportstatus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2ef00-104">TransportStatus enumeration</span></span>

<span data-ttu-id="2ef00-105">Definiert den verfügbaren Transport Status gemäß den UPnP-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="2ef00-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef00-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ef00-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="2ef00-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2ef00-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2ef00-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="2ef00-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="2ef00-109">Fehlerhafter Gerätestatus.</span><span class="sxs-lookup"><span data-stu-id="2ef00-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="2ef00-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Okay**</span><span class="sxs-lookup"><span data-stu-id="2ef00-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="2ef00-111">Das Gerät befindet sich in einem guten Status.</span><span class="sxs-lookup"><span data-stu-id="2ef00-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="2ef00-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**Fehler aufgetreten**</span><span class="sxs-lookup"><span data-stu-id="2ef00-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="2ef00-113">Auf dem Gerät ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2ef00-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="2ef00-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Letzten**</span><span class="sxs-lookup"><span data-stu-id="2ef00-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="2ef00-115">Der vorherige Status des Geräts zum aktuellen Transport Status.</span><span class="sxs-lookup"><span data-stu-id="2ef00-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ef00-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ef00-116">Requirements</span></span>



| <span data-ttu-id="2ef00-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ef00-117">Requirement</span></span> | <span data-ttu-id="2ef00-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2ef00-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef00-119">IDL</span><span class="sxs-lookup"><span data-stu-id="2ef00-119">IDL</span></span><br/> | <dl> <span data-ttu-id="2ef00-120"><dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="2ef00-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





