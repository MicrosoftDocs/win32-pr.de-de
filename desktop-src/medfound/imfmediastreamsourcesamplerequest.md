---
description: Stellt eine Anforderung für ein Beispiel aus einem MediaStreamSource-Element dar.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Imfmediastreamsourcesamplerequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351509"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="bb145-103">Imfmediastreamsourcesamplerequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bb145-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="bb145-104">Stellt eine Anforderung für ein Beispiel aus einem MediaStreamSource-Element dar.</span><span class="sxs-lookup"><span data-stu-id="bb145-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="bb145-105">Member</span><span class="sxs-lookup"><span data-stu-id="bb145-105">Members</span></span>

<span data-ttu-id="bb145-106">Die **imfmediastreamsourcesamplerequest** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bb145-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bb145-107">**Imfmediastreamsourcesamplerequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bb145-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="bb145-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="bb145-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bb145-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="bb145-109">Methods</span></span>

<span data-ttu-id="bb145-110">Die **imfmediastreamsourcesamplerequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bb145-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="bb145-111">Methode</span><span class="sxs-lookup"><span data-stu-id="bb145-111">Method</span></span>                                                           | <span data-ttu-id="bb145-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb145-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="bb145-113">**SetSample**</span><span class="sxs-lookup"><span data-stu-id="bb145-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="bb145-114">Legt das Beispiel für die Medienstrom Quelle fest.</span><span class="sxs-lookup"><span data-stu-id="bb145-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb145-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb145-115">Remarks</span></span>

<span data-ttu-id="bb145-116">**Mfmediastreamsourcesamplerequest** wird von der [**Windows. Media. Core. mediastreamsourcesamplerequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) -Lauf Zeit Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="bb145-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb145-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb145-117">Requirements</span></span>



| <span data-ttu-id="bb145-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb145-118">Requirement</span></span> | <span data-ttu-id="bb145-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bb145-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb145-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb145-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb145-121">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb145-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bb145-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb145-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb145-123">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb145-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="bb145-124">IDL</span><span class="sxs-lookup"><span data-stu-id="bb145-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb145-125"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb145-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb145-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb145-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb145-127">Media Foundation Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bb145-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
