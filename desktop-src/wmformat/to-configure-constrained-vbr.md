---
title: So konfigurieren Sie eingeschränkte VBR
description: So konfigurieren Sie eingeschränkte VBR
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, Konfigurieren von eingeschränkten VBR
- variablenbitrate (VBR), Konfigurieren von eingeschränkten
- VBR (Variable Bitrate), Konfigurieren von eingeschränkten
- Profile, Konfigurieren von eingeschränkten VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038678"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="f28e5-111">So konfigurieren Sie eingeschränkte VBR</span><span class="sxs-lookup"><span data-stu-id="f28e5-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="f28e5-112">Mit eingeschränkter VBR-Codierung (Variable Bitrate) können Sie eine durchschnittliche Bitrate angeben, die im codierten Inhalt beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="f28e5-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="f28e5-113">Außerdem geben Sie die maximale Bitrate des Streams und das maximal erforderliche Puffer Fenster an.</span><span class="sxs-lookup"><span data-stu-id="f28e5-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="f28e5-114">Sie können nicht wissen, was die durchschnittliche Bitrate für einen eingeschränkten VBR-Stream vor der Codierung ist, aber Sie können eine grobe Schätzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f28e5-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="f28e5-115">Als allgemeine Regel gilt, dass die von Ihnen angegebene maximale Bitrate das zwei-bis Dreifache der durchschnittlichen Bitrate ist.</span><span class="sxs-lookup"><span data-stu-id="f28e5-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="f28e5-116">Eingeschränkter VBR muss in Verbindung mit der zwei-Pass-Codierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f28e5-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="f28e5-117">Die zwei-Pass-Codierung ist nicht im Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f28e5-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="f28e5-118">Sie müssen den Writer so konfigurieren, dass vor dem Schreiben des Streams ein Vorverarbeitungs Durchlauf durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f28e5-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="f28e5-119">Weitere Informationen zur Verwendung von zwei-Pass-Codierungen finden [Sie unter using Two-Pass Encoding](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="f28e5-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="f28e5-120">Führen Sie die folgenden Schritte aus, um einen Datenstrom in einem Profil für die Verwendung eingeschränkter VBR-Codierung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f28e5-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="f28e5-121">Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f28e5-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="f28e5-122">Öffnen Sie ein vorhandenes Profil, dem Sie die VBR-Unterstützung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f28e5-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="f28e5-123">Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="f28e5-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="f28e5-124">Rufen Sie ein streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie entweder [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f28e5-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="f28e5-125">Abrufen eines Zeigers auf die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f28e5-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="f28e5-126">Aktivieren Sie die VBR-Codierung für den Datenstrom, indem Sie [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die **g \_ wszvbrenabled** -Eigenschaft aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f28e5-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="f28e5-127">Verwenden Sie Aufrufe von **iwmpropertyvault:: SetProperty** , um die gewünschten maximalen Werte für die Eigenschaften " **g \_ wszvbrbitratemax** " und " **g \_ wszvbrbufferwindowmax** " festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f28e5-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="f28e5-128">Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f28e5-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="f28e5-129">Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f28e5-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="f28e5-130">Konfigurieren Sie den Writer, um einen Vorverarbeitungs Durchlauf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f28e5-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f28e5-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f28e5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f28e5-132">**Konfigurieren von VBR-Streams**</span><span class="sxs-lookup"><span data-stu-id="f28e5-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




