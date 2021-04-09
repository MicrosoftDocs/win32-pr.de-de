---
title: Konfigurieren von VBR-Streams
description: Konfigurieren von VBR-Streams
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, iwmpropertyvault-Schnittstelle
- Iwmpropertyvault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948426"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="43247-109">Konfigurieren von VBR-Streams</span><span class="sxs-lookup"><span data-stu-id="43247-109">Configuring VBR Streams</span></span>

<span data-ttu-id="43247-110">Mit der VBR-Codierung (Variable Bitrate) können Sie qualitativ hochwertige Streams für lokale Dateien oder für das herunterladen und Wiedergeben von Daten liefern.</span><span class="sxs-lookup"><span data-stu-id="43247-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="43247-111">Es gibt drei Optionen für VBR: Quality-based (One-Pass), uneingeschränkter (zweipass) und eingeschränkt (Two-Pass).</span><span class="sxs-lookup"><span data-stu-id="43247-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="43247-112">Weitere Informationen zu den Typen der VBR-Codierung finden Sie unter [Variable Bitrate (VBR)-Codierung](variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="43247-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="43247-113">Sie können die VBR-Codierung in einem Profil konfigurieren, indem Sie Eigenschaften mit der [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="43247-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="43247-114">In der folgenden Tabelle werden die Eigenschaften zum Konfigurieren der VBR-Codierung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="43247-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="43247-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="43247-115">Property</span></span>                     | <span data-ttu-id="43247-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43247-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43247-117">**g \_ wszvbrenabled**</span><span class="sxs-lookup"><span data-stu-id="43247-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="43247-118">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="43247-118">Boolean value.</span></span> <span data-ttu-id="43247-119">Legen Sie true fest, um die VBR-Codierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="43247-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="43247-120">**g \_ wszvbrquality**</span><span class="sxs-lookup"><span data-stu-id="43247-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="43247-121">**DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="43247-121">**DWORD** value.</span></span> <span data-ttu-id="43247-122">Legen Sie auf die gewünschte Qualitätsstufe (1 bis 100) für die Qualitäts basierte VBR-Codierung fest.</span><span class="sxs-lookup"><span data-stu-id="43247-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="43247-123">**g \_ wszvbrbitratemax**</span><span class="sxs-lookup"><span data-stu-id="43247-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="43247-124">**DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="43247-124">**DWORD** value.</span></span> <span data-ttu-id="43247-125">Legen Sie die maximale Bitrate in Bits pro Sekunde für die eingeschränkte VBR-Codierung fest.</span><span class="sxs-lookup"><span data-stu-id="43247-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="43247-126">**g \_ wszvbrbufferwindowmax**</span><span class="sxs-lookup"><span data-stu-id="43247-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="43247-127">**DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="43247-127">**DWORD** value.</span></span> <span data-ttu-id="43247-128">Legen Sie auf das maximale Puffer Fenster (in Millisekunden) für die eingeschränkte VBR-Codierung fest.</span><span class="sxs-lookup"><span data-stu-id="43247-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="43247-129">In den folgenden Abschnitten wird beschrieben, wie die verschiedenen Typen der Variablen Bitrate-Codierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43247-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="43247-130">`Section`</span><span class="sxs-lookup"><span data-stu-id="43247-130">Section</span></span>                                                              | <span data-ttu-id="43247-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43247-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43247-132">So konfigurieren Sie Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="43247-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="43247-133">Beschreibt, wie die variablenbitrate-Codierung basierend auf einer statischen Qualitätsstufe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43247-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="43247-134">So konfigurieren Sie einen nicht eingeschränkten VBR</span><span class="sxs-lookup"><span data-stu-id="43247-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="43247-135">Beschreibt die Verwendung der variablenbitrate-Codierung basierend auf einer durchschnittlichen Zielbitrate ohne einen expliziten Spitzenwert.</span><span class="sxs-lookup"><span data-stu-id="43247-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="43247-136">So konfigurieren Sie eingeschränkte VBR</span><span class="sxs-lookup"><span data-stu-id="43247-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="43247-137">Beschreibt die Verwendung der variablenbitrate-Codierung basierend auf der durchschnittlichen Bitrate des Ziels und einem expliziten Spitzenwert.</span><span class="sxs-lookup"><span data-stu-id="43247-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="43247-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43247-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43247-139">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="43247-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




