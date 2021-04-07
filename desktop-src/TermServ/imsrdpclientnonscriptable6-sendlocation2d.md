---
title: IMsRdpClientNonScriptable6 SendLocation2D-Methode
description: Sendet einen breiten-und Längengrad Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.
ms.tgt_platform: multiple
keywords:
- SendLocation2D-Methode Remotedesktopdienste
- SendLocation2D-Methode Remotedesktopdienste, IMsRdpClientNonScriptable6-Schnittstelle
- IMsRdpClientNonScriptable6-Schnittstelle Remotedesktopdienste, SendLocation2D-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745344"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="4d92d-106">IMsRdpClientNonScriptable6:: SendLocation2D-Methode</span><span class="sxs-lookup"><span data-stu-id="4d92d-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="4d92d-107">Sendet einen breiten-und Längengrad Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d92d-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d92d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d92d-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="4d92d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d92d-109">Parameters</span></span>

<span data-ttu-id="4d92d-110">*Breitengrad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d92d-110">*latitude* \[in\]</span></span>

<span data-ttu-id="4d92d-111">Der Breitengrad eines geografischen Standorts.</span><span class="sxs-lookup"><span data-stu-id="4d92d-111">The latitude of a geographic location.</span></span> <span data-ttu-id="4d92d-112">Der gültige Bereich von breiten Werten liegt zwischen-90,0 und 90,0 Grad.</span><span class="sxs-lookup"><span data-stu-id="4d92d-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="4d92d-113">*Längengrad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d92d-113">*longitude* \[in\]</span></span>

<span data-ttu-id="4d92d-114">Der Längengrad eines geografischen Standorts.</span><span class="sxs-lookup"><span data-stu-id="4d92d-114">The longitude of a geographic location.</span></span> <span data-ttu-id="4d92d-115">Der gültige Bereich von breiten Werten liegt zwischen-180,0 und 180,0 Grad.</span><span class="sxs-lookup"><span data-stu-id="4d92d-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d92d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d92d-116">Return value</span></span>

<span data-ttu-id="4d92d-117">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4d92d-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d92d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d92d-118">Requirements</span></span>

| <span data-ttu-id="4d92d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d92d-119">Requirement</span></span> | <span data-ttu-id="4d92d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4d92d-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="4d92d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d92d-121">Minimum supported client</span></span>| <span data-ttu-id="4d92d-122">Windows 10, Version 1709 (Build 16299)</span><span class="sxs-lookup"><span data-stu-id="4d92d-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="4d92d-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4d92d-123">Type library</span></span>            | <span data-ttu-id="4d92d-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="4d92d-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="4d92d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4d92d-125">DLL</span></span>                  | <span data-ttu-id="4d92d-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="4d92d-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="4d92d-127">IID</span><span class="sxs-lookup"><span data-stu-id="4d92d-127">IID</span></span>                      | <span data-ttu-id="4d92d-128">IID \_ IMsRdpClientNonScriptable6 ist als 05293249-B28B-4db8-BE64-1b2t496b910e definiert.</span><span class="sxs-lookup"><span data-stu-id="4d92d-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="4d92d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d92d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d92d-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="4d92d-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
