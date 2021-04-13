---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection-Eigenschaft
description: Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.
ms.tgt_platform: multiple
keywords:
- Cameraredirconfigcollection-Eigenschaft Remotedesktopdienste
- Cameraredirconfigcollection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable7-Schnittstelle
- IMsRdpClientNonScriptable7 Interface Remotedesktopdienste, cameraredirconfigcollection (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341398"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="03cde-106">IMsRdpClientNonScriptable7:: cameraredirconfigcollection (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03cde-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="03cde-107">Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="03cde-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="03cde-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="03cde-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cde-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="03cde-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="03cde-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="03cde-110">Property value</span></span>

<span data-ttu-id="03cde-111">Eine [imsrdpcameraredirconfigcollection](imsrdpcameraredirconfigcollection.md) , die die Sammlung der Kameras (und der zugehörigen Konfigurationen) darstellt, die für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="03cde-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="03cde-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03cde-112">Requirements</span></span>

| <span data-ttu-id="03cde-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03cde-113">Requirement</span></span> | <span data-ttu-id="03cde-114">Wert</span><span class="sxs-lookup"><span data-stu-id="03cde-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="03cde-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03cde-115">Minimum supported client</span></span>| <span data-ttu-id="03cde-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="03cde-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="03cde-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="03cde-117">Type library</span></span>            | <span data-ttu-id="03cde-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="03cde-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="03cde-119">DLL</span><span class="sxs-lookup"><span data-stu-id="03cde-119">DLL</span></span>                  | <span data-ttu-id="03cde-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="03cde-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="03cde-121">IID</span><span class="sxs-lookup"><span data-stu-id="03cde-121">IID</span></span>                      | <span data-ttu-id="03cde-122">IID \_ IMsRdpClientNonScriptable7 ist als 71b4a60a-fe21-46d8-a39b-8e32ba0c5ecc definiert.</span><span class="sxs-lookup"><span data-stu-id="03cde-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="03cde-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03cde-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cde-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="03cde-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>