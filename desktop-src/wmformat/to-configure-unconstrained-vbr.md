---
title: So konfigurieren Sie einen nicht eingeschränkten VBR
description: So konfigurieren Sie einen nicht eingeschränkten VBR
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, Konfigurieren von nicht eingeschränktem VBR
- variablenbitrate (VBR), Konfigurieren der nicht eingeschränkten
- VBR (variablenbitrate), Konfiguration nicht eingeschränkt
- Profile, Konfigurieren von nicht eingeschränktem VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101339"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="061b9-111">So konfigurieren Sie einen nicht eingeschränkten VBR</span><span class="sxs-lookup"><span data-stu-id="061b9-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="061b9-112">Sie können die unbeschränkte VBR-Codierung (Variable Bitrate) für einen Stream verwenden, um eine durchschnittliche Bitrate anzugeben, die im codierten Inhalt beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="061b9-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="061b9-113">Der uneingeschränkte VBR unterscheidet sich insofern von der normalen CBR, dass die Varianz der Bitrate im gesamten Datenstrom größer sein kann.</span><span class="sxs-lookup"><span data-stu-id="061b9-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="061b9-114">Die Bitrate des Datenstroms, der mit [**iwmstreamconfig:: setbitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)festgelegt wird, wird als die gewünschte durchschnittliche Bitrate verwendet.</span><span class="sxs-lookup"><span data-stu-id="061b9-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="061b9-115">Wenn die Codierung des Streams beendet ist, können Sie mit [**iwmpropertyvault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) zwei zusätzliche Eigenschaften abrufen: **g \_ wszvbrpeak** und **g \_ wszbufferaverage**.</span><span class="sxs-lookup"><span data-stu-id="061b9-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="061b9-116">Diese Eigenschaften beschreiben die Spitzen Bitrate des codierten Inhalts und das durchschnittliche Puffer Fenster des Inhalts bzw.</span><span class="sxs-lookup"><span data-stu-id="061b9-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="061b9-117">Nicht eingeschränkter VBR muss in Verbindung mit der zwei-Pass-Codierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="061b9-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="061b9-118">Die zwei-Pass-Codierung ist nicht im Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="061b9-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="061b9-119">Sie müssen den Writer so konfigurieren, dass vor dem Schreiben des Streams ein Vorverarbeitungs Durchlauf durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="061b9-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="061b9-120">Weitere Informationen zur Verwendung von zwei-Pass-Codierungen finden [Sie unter using Two-Pass Encoding](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="061b9-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="061b9-121">Führen Sie die folgenden Schritte aus, um einen Datenstrom in einem Profil zu konfigurieren, der mit unbeschränkter VBR codiert werden soll:</span><span class="sxs-lookup"><span data-stu-id="061b9-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="061b9-122">Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="061b9-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="061b9-123">Öffnen Sie ein vorhandenes Profil, dem Sie die VBR-Unterstützung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="061b9-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="061b9-124">Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="061b9-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="061b9-125">Rufen Sie ein streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie entweder [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="061b9-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="061b9-126">Abrufen eines Zeigers auf die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="061b9-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="061b9-127">Aktivieren Sie die VBR-Codierung für den Datenstrom, indem Sie [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die **g \_ wszvbrenabled** -Eigenschaft aufrufen.</span><span class="sxs-lookup"><span data-stu-id="061b9-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="061b9-128">Legen Sie **g \_ wszvbrbitratemax** und **g \_ wszvbrbufferwindowmax** mit **iwmpropertyvault:: SetProperty** auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="061b9-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="061b9-129">Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="061b9-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="061b9-130">Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="061b9-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="061b9-131">Konfigurieren Sie den Writer, um einen Vorverarbeitungs Durchlauf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="061b9-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="061b9-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="061b9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="061b9-133">**Konfigurieren von VBR-Streams**</span><span class="sxs-lookup"><span data-stu-id="061b9-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




