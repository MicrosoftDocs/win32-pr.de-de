---
title: IMsRdpClientNonScriptable6 SendLocation3D-Methode
description: Sendet einen breiten-, Längen-und Höhen Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.
ms.tgt_platform: multiple
keywords:
- SendLocation3D-Methode Remotedesktopdienste
- SendLocation3D-Methode Remotedesktopdienste, IMsRdpClientNonScriptable6-Schnittstelle
- IMsRdpClientNonScriptable6-Schnittstelle Remotedesktopdienste, SendLocation3D-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480523"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a><span data-ttu-id="a0245-106">IMsRdpClientNonScriptable6:: SendLocation3D-Methode</span><span class="sxs-lookup"><span data-stu-id="a0245-106">IMsRdpClientNonScriptable6::SendLocation3D method</span></span>

<span data-ttu-id="a0245-107">Sendet einen breiten-, Längen-und Höhen Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0245-107">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0245-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0245-108">Syntax</span></span>

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a><span data-ttu-id="a0245-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0245-109">Parameters</span></span>

<span data-ttu-id="a0245-110">*Breitengrad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0245-110">*latitude* \[in\]</span></span>

<span data-ttu-id="a0245-111">Der Breitengrad eines geografischen Standorts.</span><span class="sxs-lookup"><span data-stu-id="a0245-111">The latitude of a geographic location.</span></span> <span data-ttu-id="a0245-112">Der gültige Bereich von breiten Werten liegt zwischen-90,0 und 90,0 Grad.</span><span class="sxs-lookup"><span data-stu-id="a0245-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="a0245-113">*Längengrad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0245-113">*longitude* \[in\]</span></span>

<span data-ttu-id="a0245-114">Der Längengrad eines geografischen Standorts.</span><span class="sxs-lookup"><span data-stu-id="a0245-114">The longitude of a geographic location.</span></span> <span data-ttu-id="a0245-115">Der gültige Bereich von breiten Werten liegt zwischen-180,0 und 180,0 Grad.</span><span class="sxs-lookup"><span data-stu-id="a0245-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

<span data-ttu-id="a0245-116">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0245-116">*altitude* \[in\]</span></span>

<span data-ttu-id="a0245-117">Die Höhe eines geografischen Standorts in Meter.</span><span class="sxs-lookup"><span data-stu-id="a0245-117">The altitude of a geographic location in meters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0245-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0245-118">Return value</span></span>

<span data-ttu-id="a0245-119">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a0245-119">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0245-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0245-120">Requirements</span></span>

| <span data-ttu-id="a0245-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0245-121">Requirement</span></span> | <span data-ttu-id="a0245-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a0245-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="a0245-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0245-123">Minimum supported client</span></span>| <span data-ttu-id="a0245-124">Windows 10, Version 1709 (Build 16299)</span><span class="sxs-lookup"><span data-stu-id="a0245-124">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="a0245-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a0245-125">Type library</span></span>            | <span data-ttu-id="a0245-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a0245-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="a0245-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a0245-127">DLL</span></span>                  | <span data-ttu-id="a0245-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a0245-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="a0245-129">IID</span><span class="sxs-lookup"><span data-stu-id="a0245-129">IID</span></span>                      | <span data-ttu-id="a0245-130">IID \_ IMsRdpClientNonScriptable6 ist als 05293249-B28B-4db8-BE64-1b2t496b910e definiert.</span><span class="sxs-lookup"><span data-stu-id="a0245-130">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="a0245-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0245-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0245-132">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="a0245-132">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
