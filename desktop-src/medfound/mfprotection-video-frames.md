---
description: Gibt an, ob einer Anwendung der Zugriff auf nicht komprimierte Video Frames gestattet wird.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: MFPROTECTION_VIDEO_FRAMES-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350583"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="01bd7-103">MF Protection- \_ Video \_ Rahmen Attribut</span><span class="sxs-lookup"><span data-stu-id="01bd7-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="01bd7-104">Gibt an, ob einer Anwendung der Zugriff auf nicht komprimierte Video Frames gestattet wird.</span><span class="sxs-lookup"><span data-stu-id="01bd7-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="01bd7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="01bd7-105">Data type</span></span>

<span data-ttu-id="01bd7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="01bd7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="01bd7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01bd7-107">Remarks</span></span>

<span data-ttu-id="01bd7-108">Der Wert 0 gibt an, dass der Anwendung der Zugriff auf die Frames gestattet ist.</span><span class="sxs-lookup"><span data-stu-id="01bd7-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="01bd7-109">Dies kann als Ergebnis einer privaten Vereinbarung zwischen der Anwendung und dem jeweiligen verwendeten Inhalts Schutzsystem festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="01bd7-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="01bd7-110">Der Wert 1 gibt an, dass der Anwendung der Zugriff auf Frames gestattet wird, wenn ein gültiges Anwendungs Zertifikat von der Anwendung bereitgestellt wird (siehe [**imfmediaengineprotectedcontent:: setapplicationcertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span><span class="sxs-lookup"><span data-stu-id="01bd7-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="01bd7-111">Ein Wert von 0xFFFFFFFF, der der Standardwert ist, bedeutet, dass keinen Anwendungen der Zugriff auf unkomprimierte Frames gestattet wird.</span><span class="sxs-lookup"><span data-stu-id="01bd7-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="01bd7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01bd7-112">Requirements</span></span>



| <span data-ttu-id="01bd7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01bd7-113">Requirement</span></span> | <span data-ttu-id="01bd7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="01bd7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01bd7-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01bd7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01bd7-116">Nur Windows 8 \[ UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="01bd7-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="01bd7-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01bd7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01bd7-118">Windows Server 2012 \[ UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="01bd7-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01bd7-119">Header</span><span class="sxs-lookup"><span data-stu-id="01bd7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="01bd7-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01bd7-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01bd7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01bd7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01bd7-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="01bd7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01bd7-123">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="01bd7-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




