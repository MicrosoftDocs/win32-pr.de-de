---
title: IMsRdpCameraRedirConfigCollection AddConfig-Methode
description: Fügt der Auflistung ein imsrdpcameraredirconfig-Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).
ms.tgt_platform: multiple
keywords:
- AddConfig-Methode Remotedesktopdienste
- AddConfig-Methode Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, AddConfig-Methode
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520304"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="ea31b-106">Imsrdpcameraredirconfigcollection:: AddConfig-Methode</span><span class="sxs-lookup"><span data-stu-id="ea31b-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="ea31b-107">Fügt der Auflistung ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).</span><span class="sxs-lookup"><span data-stu-id="ea31b-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea31b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea31b-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="ea31b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea31b-109">Parameters</span></span>

<span data-ttu-id="ea31b-110">*SymbolicLink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea31b-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="ea31b-111">Die symbolische Verknüpfung für das neue [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ea31b-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="ea31b-112">*frei geleitet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea31b-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="ea31b-113">Gibt an, ob die neue Kamera standardmäßig umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ea31b-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea31b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea31b-114">Return value</span></span>

<span data-ttu-id="ea31b-115">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ea31b-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea31b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea31b-116">Requirements</span></span>

| <span data-ttu-id="ea31b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea31b-117">Requirement</span></span> | <span data-ttu-id="ea31b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ea31b-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="ea31b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea31b-119">Minimum supported client</span></span>| <span data-ttu-id="ea31b-120">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="ea31b-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="ea31b-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ea31b-121">Type library</span></span>            | <span data-ttu-id="ea31b-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ea31b-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="ea31b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ea31b-123">DLL</span></span>                  | <span data-ttu-id="ea31b-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ea31b-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="ea31b-125">IID</span><span class="sxs-lookup"><span data-stu-id="ea31b-125">IID</span></span>                      | <span data-ttu-id="ea31b-126">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="ea31b-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="ea31b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea31b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea31b-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="ea31b-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>