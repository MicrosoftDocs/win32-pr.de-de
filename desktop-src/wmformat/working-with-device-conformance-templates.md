---
title: Arbeiten mit Geräte Konformitäts Vorlagen
description: Arbeiten mit Geräte Konformitäts Vorlagen
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- Profile, Vorlagen für Geräte Konformität
- Profile, Konformitäts Vorlagen
- Codecs, Geräte Konformitäts Vorlagen
- Codecs, Konformitäts Vorlagen
- Geräte Konformitäts Vorlagen, Informationen zu
- Konformitäts Vorlagen
- Vorlagen, Geräte Konformitäts Vorlagen
- Advanced Systems Format (ASF), Geräte Konformitäts Vorlagen
- ASF (Advanced Systems Format), Geräte Konformitäts Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101250"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="cce3e-112">Arbeiten mit Geräte Konformitäts Vorlagen</span><span class="sxs-lookup"><span data-stu-id="cce3e-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="cce3e-113">Aufgrund der großen Flexibilität von ASF-Dateien ist es häufig schwierig, zu bestimmen, ob eine Datei für die Wiedergabe auf einem bestimmten Gerät geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="cce3e-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="cce3e-114">Beispielsweise sind Dateien, die für die lokale Wiedergabe auf Desktop Computern geschrieben wurden, nicht optimal für die Verwendung auf handgehaltenen Geräten geeignet.</span><span class="sxs-lookup"><span data-stu-id="cce3e-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="cce3e-115">Mit Geräte Konformitäts Vorlagen können Anwendungen schnell den Typ des Wiedergabe Geräts identifizieren, für das eine Datei vorgesehen war.</span><span class="sxs-lookup"><span data-stu-id="cce3e-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="cce3e-116">Wenn die Vorlage für die Geräte Konformität nicht mit dem Gerät übereinstimmt, kann die Anwendung den Benutzer darüber informieren, dass die Datei für das Gerät ungeeignet ist.</span><span class="sxs-lookup"><span data-stu-id="cce3e-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="cce3e-117">Auf diese Weise kann der Benutzer sicher sein, dass er eine bessere Wiedergabefunktion hat.</span><span class="sxs-lookup"><span data-stu-id="cce3e-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="cce3e-118">Wenn Sie Dateien exklusiv für die Verwendung auf PCs schreiben, sind die Geräte Konformitäts Vorlagen nicht so groß wie beim Erstellen von Profilen.</span><span class="sxs-lookup"><span data-stu-id="cce3e-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="cce3e-119">Der Hauptzweck dieser Vorlagen besteht darin sicherzustellen, dass Dateien, die für die Verwendung mit spezieller Hardware erstellt werden, mit einer Vielzahl von Geräten und nicht nur mit einem einzigen Gerät kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="cce3e-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="cce3e-120">Eine Vorlage für die Geräte Konformität ist eine Behauptung, dass eine ASF-Datei Daten enthält, die in bestimmten Parametern codiert sind.</span><span class="sxs-lookup"><span data-stu-id="cce3e-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="cce3e-121">Weitere Informationen zu den Einstellungen, die für die einzelnen Vorlagen geeignet sind, finden Sie unter Geräte Übereinstimmungs- [Vorlagen Parameter](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cce3e-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="cce3e-122">Die folgenden Codecs unterstützen Geräte Konformitäts Vorlagen:</span><span class="sxs-lookup"><span data-stu-id="cce3e-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="cce3e-123">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="cce3e-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="cce3e-124">Windows Media Audio 9 und höher</span><span class="sxs-lookup"><span data-stu-id="cce3e-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="cce3e-125">Windows Media Audio 9 Professional und höher</span><span class="sxs-lookup"><span data-stu-id="cce3e-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="cce3e-126">Windows Media Audio 9-Stimme</span><span class="sxs-lookup"><span data-stu-id="cce3e-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="cce3e-127">Sie müssen keine besonderen Schritte ausführen, um die Geräte Konformitäts Vorlagen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cce3e-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="cce3e-128">Der Codec schreibt automatisch eine Vorlagen Zeichenfolge für jeden entsprechenden Stream in der Datei.</span><span class="sxs-lookup"><span data-stu-id="cce3e-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="cce3e-129">Der Codec entscheidet basierend auf den Datenstrom-Konfigurationseinstellungen im Profil, welche Vorlage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cce3e-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="cce3e-130">Es gibt einige Überschneidungen in den Vorlagen Parametern der Geräte Übereinstimmung, sodass Sie eine bestimmte Vorlage anfordern möchten, anstatt dem Codec eine Zuweisung für Sie zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cce3e-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="cce3e-131">Sie können angeben, welche Vorlage Sie möchten, indem Sie die \_ Eigenschaft g wszdecodercomplexityangeforderten mit den Methoden der [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des entsprechenden Datenstrom-Konfigurations Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="cce3e-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="cce3e-132">Wenn eine ASF-Datei geschrieben wird, wird die tatsächliche Geräte Konformitäts Vorlage für jeden Stream auf den Wert festgelegt, der vom Codec an den Writer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="cce3e-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="cce3e-133">Beim Öffnen einer Datei zum lesen können Sie mithilfe der Methoden der [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle ermitteln, welcher Vorlage die Streams der Datei entsprechen, um das g \_ wszdeviceconformancetemplate-Attribut auf Streamebene abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cce3e-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="cce3e-134">Weitere Informationen zu Attributen finden Sie unter [Arbeiten mit Metadaten](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="cce3e-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cce3e-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cce3e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce3e-136">**Entwerfen von Profilen**</span><span class="sxs-lookup"><span data-stu-id="cce3e-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="cce3e-137">**Parameter für die Geräte Konformitäts Vorlage**</span><span class="sxs-lookup"><span data-stu-id="cce3e-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




