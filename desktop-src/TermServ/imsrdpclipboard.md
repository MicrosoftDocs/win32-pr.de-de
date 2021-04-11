---
title: IMsRdpClipboard-Schnittstelle
description: Stellt den Zwischenablage Controller dar, mit dem die lokalen und Remote-zwischen Ablagen synchronisiert werden, wenn die manuelle Synchronisierung der Zwischenablage aktiviert
ms.tgt_platform: multiple
keywords:
- Imsrdpclipboard-Schnittstelle Remotedesktopdienste
- Imsrdpclipboard-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123301"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="0b8c3-105">IMsRdpClipboard-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0b8c3-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="0b8c3-106">Stellt den Zwischenablage Controller dar, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Synchronisierung der Zwischenablage aktiviert ist (d. h., der [manualclipboardsyncenabled](imsrdpextendedsettings-property.md) -Eigenschafts Wert ist auf **true**</span><span class="sxs-lookup"><span data-stu-id="0b8c3-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="0b8c3-107">Member</span><span class="sxs-lookup"><span data-stu-id="0b8c3-107">Members</span></span>

<span data-ttu-id="0b8c3-108">Die **imsrdpclipboard** -Schnittstelle erbt von **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="0b8c3-109">**Imsrdpclipboard** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0b8c3-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="0b8c3-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b8c3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b8c3-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b8c3-111">Methods</span></span>

<span data-ttu-id="0b8c3-112">Die **imsrdpclipboard** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="0b8c3-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0b8c3-113">Method</span></span>        | <span data-ttu-id="0b8c3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b8c3-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="0b8c3-115">**Cansynclocalclipboardtor emotesession**</span><span class="sxs-lookup"><span data-stu-id="0b8c3-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="0b8c3-116">Gibt an, ob die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="0b8c3-117">**Cansynkremoteclipboardtolocalsession**</span><span class="sxs-lookup"><span data-stu-id="0b8c3-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="0b8c3-118">Gibt an, ob die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="0b8c3-119">**Synclocalclipboardtor emotesession**</span><span class="sxs-lookup"><span data-stu-id="0b8c3-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="0b8c3-120">Synchronisiert die lokale Zwischenablage mit der Remote Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="0b8c3-121">**Synkremoteclipboardtolocalsession**</span><span class="sxs-lookup"><span data-stu-id="0b8c3-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="0b8c3-122">Synchronisiert die Remote Zwischenablage mit der lokalen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="0b8c3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b8c3-123">Requirements</span></span>

| <span data-ttu-id="0b8c3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b8c3-124">Requirement</span></span> | <span data-ttu-id="0b8c3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0b8c3-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="0b8c3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b8c3-126">Minimum supported client</span></span>| <span data-ttu-id="0b8c3-127">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="0b8c3-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="0b8c3-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0b8c3-128">Type library</span></span>            | <span data-ttu-id="0b8c3-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0b8c3-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="0b8c3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0b8c3-130">DLL</span></span>                  | <span data-ttu-id="0b8c3-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0b8c3-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="0b8c3-132">IID</span><span class="sxs-lookup"><span data-stu-id="0b8c3-132">IID</span></span>                      | <span data-ttu-id="0b8c3-133">IID \_ imsrdpclipboard ist als 2e769ee8-00c7-43dc-afd9-235d75b72a40 definiert.</span><span class="sxs-lookup"><span data-stu-id="0b8c3-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="0b8c3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b8c3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8c3-135">**IMsRdpClientNonScriptable7:: Zwischenablage**</span><span class="sxs-lookup"><span data-stu-id="0b8c3-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
