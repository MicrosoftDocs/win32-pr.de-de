---
title: Controlreconnectstatus-Enumeration
description: Gibt das Ergebnis der IMsRdpClient8 Reconnect-Methode an.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Controlreconnectstatus-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340981"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="8af94-104">Controlreconnectstatus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8af94-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="8af94-105">Gibt das Ergebnis der [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="8af94-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af94-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af94-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="8af94-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8af94-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8af94-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlreconnectstarted**</span><span class="sxs-lookup"><span data-stu-id="8af94-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="8af94-109">Der Vorgang zum erneuten Verbinden wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="8af94-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="8af94-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlreconnectblockierte**</span><span class="sxs-lookup"><span data-stu-id="8af94-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="8af94-111">Der Vorgang zum erneuten Verbinden konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="8af94-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8af94-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8af94-112">Requirements</span></span>



| <span data-ttu-id="8af94-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8af94-113">Requirement</span></span> | <span data-ttu-id="8af94-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8af94-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8af94-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8af94-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8af94-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8af94-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="8af94-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8af94-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8af94-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8af94-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="8af94-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8af94-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="8af94-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8af94-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af94-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8af94-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af94-122">**IMsRdpClient8:: Reconnect**</span><span class="sxs-lookup"><span data-stu-id="8af94-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





