---
title: IMsRdpClientNonScriptable7 Clipboard-Eigenschaft
description: Ruft den Zwischenablage Controller ab, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste der Zwischenablage
- Eigenschaften Remotedesktopdienste der Zwischenablage, IMsRdpClientNonScriptable7-Schnittstelle
- IMsRdpClientNonScriptable7 Interface-Remotedesktopdienste, Clipboard-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103957689"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="fccf9-106">IMsRdpClientNonScriptable7:: Clipboard (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fccf9-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="fccf9-107">Ruft den Zwischenablage Controller ab, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert</span><span class="sxs-lookup"><span data-stu-id="fccf9-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="fccf9-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fccf9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fccf9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fccf9-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="fccf9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fccf9-110">Property value</span></span>

<span data-ttu-id="fccf9-111">Eine [imsrdpclipboard](imsrdpclipboard.md) , die den Zwischenablage Controller darstellt, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert ist (d. h., der [manualclipboardsyncenabled](imsrdpextendedsettings-property.md) -Eigenschafts Wert ist auf **true** festgelegt</span><span class="sxs-lookup"><span data-stu-id="fccf9-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="fccf9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fccf9-112">Requirements</span></span>

| <span data-ttu-id="fccf9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fccf9-113">Requirement</span></span> | <span data-ttu-id="fccf9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fccf9-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fccf9-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fccf9-115">Minimum supported client</span></span>| <span data-ttu-id="fccf9-116">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="fccf9-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fccf9-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fccf9-117">Type library</span></span>            | <span data-ttu-id="fccf9-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fccf9-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fccf9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fccf9-119">DLL</span></span>                  | <span data-ttu-id="fccf9-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fccf9-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fccf9-121">IID</span><span class="sxs-lookup"><span data-stu-id="fccf9-121">IID</span></span>                      | <span data-ttu-id="fccf9-122">IID \_ IMsRdpClientNonScriptable7 ist als 71b4a60a-fe21-46d8-a39b-8e32ba0c5ecc definiert.</span><span class="sxs-lookup"><span data-stu-id="fccf9-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="fccf9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fccf9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fccf9-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="fccf9-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>