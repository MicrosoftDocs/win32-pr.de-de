---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession-Methode
description: Gibt an, ob die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann.
ms.tgt_platform: multiple
keywords:
- Cansynclocalclipboardtoremotesession-Methode Remotedesktopdienste
- Cansynclocalclipboardtoremotesession-Methode Remotedesktopdienste, imsrdpclipboard-Schnittstelle
- Imsrdpclipboard Interface Remotedesktopdienste, cansynclocalclipboardtoremotesession-Methode
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106344152"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="9925f-106">Imsrdpclipboard:: cansynclocalclipboardtoremotesession-Methode</span><span class="sxs-lookup"><span data-stu-id="9925f-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="9925f-107">Gibt an, ob die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9925f-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9925f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9925f-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="9925f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9925f-109">Parameters</span></span>

<span data-ttu-id="9925f-110">**True** , wenn die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="9925f-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="9925f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9925f-111">Return value</span></span>

<span data-ttu-id="9925f-112">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9925f-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="9925f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9925f-113">Requirements</span></span>

| <span data-ttu-id="9925f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9925f-114">Requirement</span></span> | <span data-ttu-id="9925f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9925f-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9925f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9925f-116">Minimum supported client</span></span>| <span data-ttu-id="9925f-117">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="9925f-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9925f-118">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9925f-118">Type library</span></span>            | <span data-ttu-id="9925f-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9925f-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9925f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9925f-120">DLL</span></span>                  | <span data-ttu-id="9925f-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9925f-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9925f-122">IID</span><span class="sxs-lookup"><span data-stu-id="9925f-122">IID</span></span>                      | <span data-ttu-id="9925f-123">IID \_ imsrdpclipboard ist als 2e769ee8-00c7-43dc-afd9-235d75b72a40 definiert.</span><span class="sxs-lookup"><span data-stu-id="9925f-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="9925f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9925f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9925f-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="9925f-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>