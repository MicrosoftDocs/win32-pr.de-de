---
title: Transportstate-Enumeration
description: Definiert die verfügbaren Transport Zustände gemäß den UPnP-Richtlinien.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- Transportstate-Enumeration Medien Streaming-API
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358769"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="8df06-104">Transportstate-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8df06-104">TransportState enumeration</span></span>

<span data-ttu-id="8df06-105">Definiert die verfügbaren Transport Zustände gemäß den UPnP-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="8df06-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df06-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8df06-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="8df06-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8df06-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8df06-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="8df06-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-109">Fehlerhafter Gerätezustand.</span><span class="sxs-lookup"><span data-stu-id="8df06-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Abgeh**</span><span class="sxs-lookup"><span data-stu-id="8df06-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-111">Der Transport des Geräts wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="8df06-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Ens**</span><span class="sxs-lookup"><span data-stu-id="8df06-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-113">Der Transport des Geräts befindet sich im Zustand "Wiedergabe".</span><span class="sxs-lookup"><span data-stu-id="8df06-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang**</span><span class="sxs-lookup"><span data-stu-id="8df06-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-115">Der Transport des Geräts befindet sich in einem Übergangszustand, der zu einem anderen Statuswert führt.</span><span class="sxs-lookup"><span data-stu-id="8df06-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten**</span><span class="sxs-lookup"><span data-stu-id="8df06-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-117">Der Transport des Geräts befindet sich im angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="8df06-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Verzeichnet**</span><span class="sxs-lookup"><span data-stu-id="8df06-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-119">Der Transport des Geräts ist in einem Aufzeichnungs Zustand.</span><span class="sxs-lookup"><span data-stu-id="8df06-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**Nomediapresent**</span><span class="sxs-lookup"><span data-stu-id="8df06-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-121">Für den Transport des Geräts ist kein URI für die Wiedergabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8df06-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="8df06-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Letzten**</span><span class="sxs-lookup"><span data-stu-id="8df06-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="8df06-123">Der vorherige Zustand des Geräts zum aktuellen Transportzustand.</span><span class="sxs-lookup"><span data-stu-id="8df06-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8df06-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df06-124">Requirements</span></span>



| <span data-ttu-id="8df06-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8df06-125">Requirement</span></span> | <span data-ttu-id="8df06-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8df06-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df06-127">IDL</span><span class="sxs-lookup"><span data-stu-id="8df06-127">IDL</span></span><br/> | <dl> <span data-ttu-id="8df06-128"><dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="8df06-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





