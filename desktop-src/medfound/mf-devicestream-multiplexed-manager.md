---
description: Stellt eine Instanz von imsmuxstreamattributesmanager bereit, die die imfattributes verwaltet, die die unter Ströme einer multiplext-Medienquelle beschreiben.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: MF_DEVICESTREAM_MULTIPLEXED_MANAGER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359971"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="9fcd7-103">MF- \_ Attribut "devicestream \_ multiplexed \_ Manager"</span><span class="sxs-lookup"><span data-stu-id="9fcd7-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="9fcd7-104">Stellt eine Instanz von [**imsmuxstreamattributesmanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) bereit, die die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) verwaltet, die die unter Ströme einer multiplext-Medienquelle beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9fcd7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9fcd7-105">Data type</span></span>

<span data-ttu-id="9fcd7-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="9fcd7-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="9fcd7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fcd7-107">Remarks</span></span>

<span data-ttu-id="9fcd7-108">Übergeben Sie diesen Wert an [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) , um zu bestimmen, ob die Medienquelle Multiplex Streams bereitstellt, und wenn dies der Fall ist, eine Instanz von [**imfmuxstreamattributesmanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9fcd7-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fcd7-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fcd7-109">Requirements</span></span>



| <span data-ttu-id="9fcd7-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fcd7-110">Requirement</span></span> | <span data-ttu-id="9fcd7-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9fcd7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcd7-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fcd7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9fcd7-113">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fcd7-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9fcd7-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fcd7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9fcd7-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9fcd7-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9fcd7-116">Header</span><span class="sxs-lookup"><span data-stu-id="9fcd7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fcd7-117"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fcd7-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
