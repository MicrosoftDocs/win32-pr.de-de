---
title: WM/MediaClassSecondaryID
description: Das WM/MediaClassSecondaryID-Attribut enthält die GUID der sekundären Medienklasse.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- WM/MediaClassSecondaryID Windows Media-Format
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389270"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="10d80-104">WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="10d80-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="10d80-105">Das **WM/MediaClassSecondaryID-** Attribut enthält die GUID der sekundären Medienklasse.</span><span class="sxs-lookup"><span data-stu-id="10d80-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="10d80-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="10d80-106">Global Constant</span></span>

<span data-ttu-id="10d80-107">g \_ wszwmmediaclasssecondaryid</span><span class="sxs-lookup"><span data-stu-id="10d80-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="10d80-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="10d80-108">Data Type</span></span>

<span data-ttu-id="10d80-109">**WMT- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="10d80-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="10d80-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10d80-110">Remarks</span></span>

<span data-ttu-id="10d80-111">Dieses Attribut sollte auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="10d80-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="10d80-112">GUID der sekundären Klasse</span><span class="sxs-lookup"><span data-stu-id="10d80-112">Secondary class GUID</span></span>                   | <span data-ttu-id="10d80-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10d80-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d80-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="10d80-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="10d80-115">Verwenden Sie für audiobookdateien.</span><span class="sxs-lookup"><span data-stu-id="10d80-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="10d80-116">"3a172 A13-2bd9-4831-835b-114b f"</span><span class="sxs-lookup"><span data-stu-id="10d80-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="10d80-117">Verwendung für Audiodateien, die gesprochene Wörter enthalten, aber keine Audiobücher sind.</span><span class="sxs-lookup"><span data-stu-id="10d80-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="10d80-118">Beispielsweise sind die-Beispiel-Comedy-Routinen.</span><span class="sxs-lookup"><span data-stu-id="10d80-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="10d80-119">"6677db9b-e5a0-4063-a1ad-aceb52840cf1"</span><span class="sxs-lookup"><span data-stu-id="10d80-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="10d80-120">Verwenden Sie für Audiodateien, die sich auf Neuigkeiten beziehen.</span><span class="sxs-lookup"><span data-stu-id="10d80-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="10d80-121">"1b824a67-3s80-4e3e-9cde-f 7361b0s5f 1B"</span><span class="sxs-lookup"><span data-stu-id="10d80-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="10d80-122">Verwenden Sie für Audiodateien mit dem Inhalt von Talk anzeigen.</span><span class="sxs-lookup"><span data-stu-id="10d80-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="10d80-123">"1fe2e091-4E1E-40ce-b22d-348c732e0b10"</span><span class="sxs-lookup"><span data-stu-id="10d80-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="10d80-124">Verwenden Sie dies für Videodateien im Zusammenhang mit Neuigkeiten.</span><span class="sxs-lookup"><span data-stu-id="10d80-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="10d80-125">"D6DE1D88-C77C-4593-BF-9c61e8c373e3"</span><span class="sxs-lookup"><span data-stu-id="10d80-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="10d80-126">Verwenden Sie dies für Videodateien mit webbasierten anzeigen, kurzen Filmen, Film Anhängern usw.</span><span class="sxs-lookup"><span data-stu-id="10d80-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="10d80-127">Dies ist der allgemeine Bezeichner für Video Unterhaltung, der nicht in eine andere Kategorie passt.</span><span class="sxs-lookup"><span data-stu-id="10d80-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="10d80-128">"00033368-5009-4ac3-A820-5d2d09a4e7c1"</span><span class="sxs-lookup"><span data-stu-id="10d80-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="10d80-129">Verwenden Sie für Audiodateien, die Soundclips von spielen enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="10d80-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="10d80-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="10d80-131">Verwenden Sie dies für Audiodateien, die vollständige Lieder aus Spiel Sound Spuren enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="10d80-132">Wenn nur ein Teil eines Liedes in der Datei codiert ist, verwenden Sie stattdessen den Bezeichner für Game Soundclips.</span><span class="sxs-lookup"><span data-stu-id="10d80-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="10d80-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="10d80-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="10d80-134">Verwenden Sie dies für Videodateien, die Musikvideos enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="10d80-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="10d80-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="10d80-136">Verwenden Sie dies für Videodateien mit dem allgemeinen Home-Video.</span><span class="sxs-lookup"><span data-stu-id="10d80-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="10d80-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="10d80-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="10d80-138">Verwenden Sie für Videodateien, die Featurefilme enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="10d80-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="10d80-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="10d80-140">Verwendung für Videodateien, die Fernsehsendungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-140">Use for video files containing television shows.</span></span> <span data-ttu-id="10d80-141">Verwenden Sie für webbasiertes anzeigen den allgemeineren Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="10d80-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="10d80-142">"44051b5b-B103-4b5c-92ab-93060a9463f"</span><span class="sxs-lookup"><span data-stu-id="10d80-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="10d80-143">Verwenden Sie dies für Videodateien, die Firmenvideos enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="10d80-144">Beispielsweise aufgezeichnete Besprechungen oder Schulungsvideos.</span><span class="sxs-lookup"><span data-stu-id="10d80-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="10d80-145">"0b710218-8c0c-475E-af73-4c41c0c8f"</span><span class="sxs-lookup"><span data-stu-id="10d80-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="10d80-146">Verwenden Sie dies für Videodateien mit Start Videos aus Fotos.</span><span class="sxs-lookup"><span data-stu-id="10d80-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="10d80-147">Wenn Sie einen Bezeichner der sekundären Klasse angeben, sollte die Datei auch ein primäres klassenbezeichnerattribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="10d80-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="10d80-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10d80-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d80-149">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="10d80-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="10d80-150">**WM/mediaclassprimaryid**</span><span class="sxs-lookup"><span data-stu-id="10d80-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 




