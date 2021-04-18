---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession-Methode
description: Gibt an, ob die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann.
ms.tgt_platform: multiple
keywords:
- Cansynkremoteclipboardtolocalsession-Methode Remotedesktopdienste
- Cansynkremoteclipboardtolocalsession-Methode Remotedesktopdienste, imsrdpclipboard-Schnittstelle
- Imsrdpclipboard Interface Remotedesktopdienste, cansynkremoteclipboardtolocalsession-Methode
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106344153"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="9eacb-106">Imsrdpclipboard:: cansynkremoteclipboardtolocalsession-Methode</span><span class="sxs-lookup"><span data-stu-id="9eacb-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="9eacb-107">Gibt an, ob die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9eacb-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eacb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eacb-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="9eacb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eacb-109">Parameters</span></span>

<span data-ttu-id="9eacb-110">**True** , wenn die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="9eacb-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="9eacb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9eacb-111">Return value</span></span>

<span data-ttu-id="9eacb-112">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9eacb-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eacb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9eacb-113">Requirements</span></span>

| <span data-ttu-id="9eacb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9eacb-114">Requirement</span></span> | <span data-ttu-id="9eacb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9eacb-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9eacb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9eacb-116">Minimum supported client</span></span>| <span data-ttu-id="9eacb-117">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="9eacb-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9eacb-118">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9eacb-118">Type library</span></span>            | <span data-ttu-id="9eacb-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9eacb-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9eacb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9eacb-120">DLL</span></span>                  | <span data-ttu-id="9eacb-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9eacb-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9eacb-122">IID</span><span class="sxs-lookup"><span data-stu-id="9eacb-122">IID</span></span>                      | <span data-ttu-id="9eacb-123">IID \_ imsrdpclipboard ist als 2e769ee8-00c7-43dc-afd9-235d75b72a40 definiert.</span><span class="sxs-lookup"><span data-stu-id="9eacb-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="9eacb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9eacb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eacb-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="9eacb-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>