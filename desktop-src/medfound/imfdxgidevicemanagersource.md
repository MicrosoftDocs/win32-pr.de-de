---
description: Stellt Funktionen zum erhalten von imsdxgidevicemanager aus der Microsoft Media Foundation Video Rendering-Senke bereit.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: IMF dxgiabvicemanagersource-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753192"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="21208-103">IMF dxgiabvicemanagersource-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="21208-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="21208-104">Stellt Funktionen zum erhalten von [**imsdxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) aus der Microsoft Media Foundation Video Rendering-Senke bereit.</span><span class="sxs-lookup"><span data-stu-id="21208-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="21208-105">Member</span><span class="sxs-lookup"><span data-stu-id="21208-105">Members</span></span>

<span data-ttu-id="21208-106">Die **IMF** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="21208-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="21208-107">**Imfdxgiabvicemanagersource** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="21208-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="21208-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="21208-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21208-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="21208-109">Methods</span></span>

<span data-ttu-id="21208-110">Die **IMF dxgidevicemanagersource** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="21208-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="21208-111">Methode</span><span class="sxs-lookup"><span data-stu-id="21208-111">Method</span></span>                                                      | <span data-ttu-id="21208-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21208-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21208-113">**GetManager**</span><span class="sxs-lookup"><span data-stu-id="21208-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="21208-114">Ruft den [**imsdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) aus der Media Foundation Video Rendering-Senke ab.</span><span class="sxs-lookup"><span data-stu-id="21208-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21208-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21208-115">Requirements</span></span>



| <span data-ttu-id="21208-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21208-116">Requirement</span></span> | <span data-ttu-id="21208-117">Wert</span><span class="sxs-lookup"><span data-stu-id="21208-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21208-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21208-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21208-119">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="21208-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="21208-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21208-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21208-121">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="21208-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="21208-122">IDL</span><span class="sxs-lookup"><span data-stu-id="21208-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21208-123"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21208-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21208-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21208-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21208-125">Media Foundation Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="21208-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
