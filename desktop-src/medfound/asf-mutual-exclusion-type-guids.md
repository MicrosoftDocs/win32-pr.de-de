---
description: Die folgenden GUIDs definieren die Typen für das gegenseitige Ausschluss Objekt für ASF-Streams (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: Gegenseitige ASF-Ausschluss Typen-GUIDs (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214345"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="50cf6-103">Gegenseitige ASF-Ausschluss Typen-GUIDs</span><span class="sxs-lookup"><span data-stu-id="50cf6-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="50cf6-104">Die folgenden GUIDs definieren die Typen für das gegenseitige Ausschluss Objekt für ASF-Streams (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="50cf6-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="50cf6-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="50cf6-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="50cf6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50cf6-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="50cf6-107"><dt>**Mfasf mutextype- \_ Sprache**</dt></span><span class="sxs-lookup"><span data-stu-id="50cf6-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="50cf6-108">Die Streams schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="50cf6-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="50cf6-109">Diese Art des gegenseitigen Ausschlusses ähnelt den Audiospuren auf einer DVD.</span><span class="sxs-lookup"><span data-stu-id="50cf6-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="50cf6-110"><dt>**Mfasf mutextype- \_ Bitrate**</dt></span><span class="sxs-lookup"><span data-stu-id="50cf6-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="50cf6-111">Die Streams schließen sich durch die Bitrate gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="50cf6-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="50cf6-112">Diese Art des gegenseitigen Ausschlusses wird auch als MBR-Ausschluss (Multiple Bitrate) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="50cf6-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="50cf6-113"><dt>**Mfasf mutextype- \_ Präsentation**</dt></span><span class="sxs-lookup"><span data-stu-id="50cf6-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="50cf6-114">Die Streams schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="50cf6-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="50cf6-115">Dieser Typ kann für viele Szenarien verwendet werden, sollte jedoch nur verwendet werden, wenn der Inhalt identisch ist, aber eine andere Form hat.</span><span class="sxs-lookup"><span data-stu-id="50cf6-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="50cf6-116">Beispielsweise sollten zwei Datenströme, die das gleiche Video enthalten, eine formatiert, um den Bildschirm zu füllen, und die andere Datenströme, die das ursprüngliche Widescreen-Seitenverhältnis behalten, mithilfe dieses Typs gegenseitig ausschließen werden.</span><span class="sxs-lookup"><span data-stu-id="50cf6-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="50cf6-117">Ein weiteres Beispiel sind Datenströme, die Videos aus unterschiedlichen Winkeln mit dem gleichen Szenenfoto enthalten.</span><span class="sxs-lookup"><span data-stu-id="50cf6-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="50cf6-118"><dt>**Mfasf mutextype \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="50cf6-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="50cf6-119">Die Streams schließen sich basierend auf den benutzerdefinierten Kriterien gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="50cf6-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="50cf6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50cf6-120">Requirements</span></span>



| <span data-ttu-id="50cf6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50cf6-121">Requirement</span></span> | <span data-ttu-id="50cf6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="50cf6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50cf6-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50cf6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="50cf6-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50cf6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50cf6-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50cf6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="50cf6-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50cf6-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="50cf6-127">Header</span><span class="sxs-lookup"><span data-stu-id="50cf6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="50cf6-128"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="50cf6-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50cf6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50cf6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cf6-130">**Imfassmutualexclusion:: GetType**</span><span class="sxs-lookup"><span data-stu-id="50cf6-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="50cf6-131">**Imfassmutualexclusion:: settype**</span><span class="sxs-lookup"><span data-stu-id="50cf6-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="50cf6-132">Media Foundation Konstanten</span><span class="sxs-lookup"><span data-stu-id="50cf6-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




