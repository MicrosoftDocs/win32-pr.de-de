---
title: IMsRdpCameraRedirConfig DeviceExists-Eigenschaft
description: Gibt an, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).
ms.tgt_platform: multiple
keywords:
- Deviceist-Eigenschaft Remotedesktopdienste
- Deviceexistiert-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, deviceist-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480563"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="31a3d-106">Imsrdpcameraredirconfig::D eviceist-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31a3d-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="31a3d-107">Gibt an, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).</span><span class="sxs-lookup"><span data-stu-id="31a3d-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="31a3d-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="31a3d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a3d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a3d-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="31a3d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="31a3d-110">Property value</span></span>

<span data-ttu-id="31a3d-111">Ein Wert, der angibt, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).</span><span class="sxs-lookup"><span data-stu-id="31a3d-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="31a3d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a3d-112">Requirements</span></span>

| <span data-ttu-id="31a3d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a3d-113">Requirement</span></span> | <span data-ttu-id="31a3d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="31a3d-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="31a3d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31a3d-115">Minimum supported client</span></span>| <span data-ttu-id="31a3d-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="31a3d-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="31a3d-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="31a3d-117">Type library</span></span>            | <span data-ttu-id="31a3d-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="31a3d-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="31a3d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="31a3d-119">DLL</span></span>                  | <span data-ttu-id="31a3d-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="31a3d-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="31a3d-121">IID</span><span class="sxs-lookup"><span data-stu-id="31a3d-121">IID</span></span>                      | <span data-ttu-id="31a3d-122">IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.</span><span class="sxs-lookup"><span data-stu-id="31a3d-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="31a3d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31a3d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a3d-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="31a3d-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>