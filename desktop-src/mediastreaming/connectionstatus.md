---
title: ConnectionStatus-Enumeration
description: Stellt den Status des Geräts im Netzwerk als zuletzt angezeigt dar.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- ConnectionStatus-Enumeration Medien Streaming-API
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357687"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="31a39-104">ConnectionStatus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="31a39-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="31a39-105">Stellt den Status des Geräts im Netzwerk als zuletzt angezeigt dar.</span><span class="sxs-lookup"><span data-stu-id="31a39-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a39-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a39-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="31a39-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="31a39-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31a39-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Internet**</span><span class="sxs-lookup"><span data-stu-id="31a39-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="31a39-109">Das Gerät ist online und im Netzwerk aktiv.</span><span class="sxs-lookup"><span data-stu-id="31a39-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="31a39-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Aufzu**</span><span class="sxs-lookup"><span data-stu-id="31a39-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="31a39-111">Gerät ist offline.</span><span class="sxs-lookup"><span data-stu-id="31a39-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="31a39-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Geschlafen**</span><span class="sxs-lookup"><span data-stu-id="31a39-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="31a39-113">Das Gerät ist zurzeit offline, wird jedoch möglicherweise automatisch aktiviert, wenn versucht wird, damit zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="31a39-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31a39-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a39-114">Requirements</span></span>



| <span data-ttu-id="31a39-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a39-115">Requirement</span></span> | <span data-ttu-id="31a39-116">Wert</span><span class="sxs-lookup"><span data-stu-id="31a39-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a39-117">IDL</span><span class="sxs-lookup"><span data-stu-id="31a39-117">IDL</span></span><br/> | <dl> <span data-ttu-id="31a39-118"><dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="31a39-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





