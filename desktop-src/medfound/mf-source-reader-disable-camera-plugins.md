---
description: Deaktiviert die Verwendung von Postprocessing-Kamera-Plug-ins durch den Quell Reader.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218116"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="e7bd7-103">MF- \_ Quell \_ Leser Deaktivieren von \_ \_ Kamera \_ -Plug-ins</span><span class="sxs-lookup"><span data-stu-id="e7bd7-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="e7bd7-104">Deaktiviert die Verwendung von Postprocessing-Kamera-Plug-ins durch den [Quell Reader](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="e7bd7-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="e7bd7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e7bd7-105">Data type</span></span>

<span data-ttu-id="e7bd7-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7bd7-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7bd7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7bd7-107">Remarks</span></span>

<span data-ttu-id="e7bd7-108">Dieses Attribut gilt, wenn der Quell Leser mit einer Video Erfassungs Quelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="e7bd7-109">Wenn dieses Attribut **true** ist, wird verhindert, dass der Quell Leser nach Verarbeitungs-Plug-ins lädt, die die Kamera möglicherweise bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="e7bd7-110">Andernfalls lädt der Quell Leser Sie standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="e7bd7-111">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="e7bd7-112">Legen Sie beim Erstellen des Quell Readers das-Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bd7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7bd7-113">Requirements</span></span>



| <span data-ttu-id="e7bd7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7bd7-114">Requirement</span></span> | <span data-ttu-id="e7bd7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e7bd7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bd7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7bd7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bd7-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e7bd7-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e7bd7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7bd7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bd7-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e7bd7-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e7bd7-120">Header</span><span class="sxs-lookup"><span data-stu-id="e7bd7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7bd7-121"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e7bd7-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7bd7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7bd7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bd7-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e7bd7-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7bd7-124">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="e7bd7-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




