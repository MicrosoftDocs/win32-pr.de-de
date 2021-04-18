---
description: Die ikeyframecontrol-Schnittstelle wird von h. 323 MSP implementiert und ist nur für h. 323-Streamobjekte verfügbar.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Ikeyframecontrol-Schnittstelle (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368482"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="abb38-103">Ikeyframecontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="abb38-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="abb38-104">\[**Ikeyframecontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="abb38-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="abb38-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="abb38-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="abb38-106">Die **ikeyframecontrol** -Schnittstelle wird von [h. 323 MSP](h323-msp.md) implementiert und ist nur für h. 323-Streamobjekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="abb38-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="abb38-107">Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="abb38-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="abb38-108">Sie verfügt über zwei Methoden, mit denen die Anwendung den Remote Endpunkt auffordern kann, das Video Bild mit einem Keyframe zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abb38-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="abb38-109">Member</span><span class="sxs-lookup"><span data-stu-id="abb38-109">Members</span></span>

<span data-ttu-id="abb38-110">Die **ikeyframecontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="abb38-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="abb38-111">**Ikeyframecontrol** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="abb38-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="abb38-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="abb38-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="abb38-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="abb38-113">Methods</span></span>

<span data-ttu-id="abb38-114">Die **ikeyframecontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="abb38-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="abb38-115">Methode</span><span class="sxs-lookup"><span data-stu-id="abb38-115">Method</span></span>                                                                  | <span data-ttu-id="abb38-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abb38-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abb38-117">**Periodicupdatepicture**</span><span class="sxs-lookup"><span data-stu-id="abb38-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="abb38-118">Konfiguriert einen Timer im Stream, der regelmäßig Bildaktualisierungen anfordert.</span><span class="sxs-lookup"><span data-stu-id="abb38-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="abb38-119">**Updatepicture**</span><span class="sxs-lookup"><span data-stu-id="abb38-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="abb38-120">Fordert den Absender des Videos auf, das Bild zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abb38-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="abb38-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abb38-121">Requirements</span></span>



| <span data-ttu-id="abb38-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abb38-122">Requirement</span></span> | <span data-ttu-id="abb38-123">Wert</span><span class="sxs-lookup"><span data-stu-id="abb38-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abb38-124">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="abb38-124">TAPI version</span></span><br/> | <span data-ttu-id="abb38-125">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="abb38-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="abb38-126">Header</span><span class="sxs-lookup"><span data-stu-id="abb38-126">Header</span></span><br/>       | <dl> <span data-ttu-id="abb38-127"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="abb38-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="abb38-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abb38-128">Library</span></span><br/>      | <dl> <span data-ttu-id="abb38-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abb38-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="abb38-130">DLL</span><span class="sxs-lookup"><span data-stu-id="abb38-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="abb38-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abb38-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="abb38-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abb38-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb38-133">H323-msp</span><span class="sxs-lookup"><span data-stu-id="abb38-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

