---
description: Der Windows Media Video 9-Bildschirm Encoder ist für das Codieren sequenzieller Screenshots von Computermonitoren optimiert.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Windows Media Video 9-Bildschirm Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370755"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="935c7-103">Windows Media Video 9-Bildschirm Encoder</span><span class="sxs-lookup"><span data-stu-id="935c7-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="935c7-104">Der Windows Media Video 9-Bildschirm Encoder ist für das Codieren sequenzieller Screenshots von Computermonitoren optimiert.</span><span class="sxs-lookup"><span data-stu-id="935c7-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="935c7-105">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="935c7-105">Class Identifier</span></span>

<span data-ttu-id="935c7-106">Der Klassen Bezeichner (CLSID) für den Windows Media Video 9-Bildschirm Encoder wird durch die Konstante **CLSID \_ CMSSCEncMediaObject2** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="935c7-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="935c7-107">Sie können eine Instanz des Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="935c7-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="935c7-108">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="935c7-108">Input Types</span></span>

<span data-ttu-id="935c7-109">Die folgenden Eingabetypen werden vom Bildschirm Encoder der Version 9 unterstützt, wenn dieser als DirectX-Medienobjekt (DMO) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="935c7-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="935c7-110">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="935c7-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="935c7-111">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="935c7-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="935c7-112">Mediasubtype \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="935c7-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="935c7-113">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="935c7-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="935c7-114">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="935c7-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="935c7-115">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="935c7-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="935c7-116">Die folgenden Eingabetypen werden vom Bildschirm Encoder der Version 9 unterstützt, wenn dieser als Media Foundation Transformation (MFT) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="935c7-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="935c7-117">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="935c7-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="935c7-118">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="935c7-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="935c7-119">MF-Format \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="935c7-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="935c7-120">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="935c7-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="935c7-121">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="935c7-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="935c7-122">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="935c7-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="935c7-123">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="935c7-123">Output Types</span></span>

<span data-ttu-id="935c7-124">Der aus vier Zeichen bestehende Code (FourCC) für Windows Media Video Bildschirm codierten Inhalt der Version 9 ist "MSS2".</span><span class="sxs-lookup"><span data-stu-id="935c7-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="935c7-125">Die folgenden Ausgabetypen werden vom Bildschirm Encoder der Version 9 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="935c7-126">Mediasubtype \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="935c7-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="935c7-127">Codierungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="935c7-127">Encoder Properties</span></span>

<span data-ttu-id="935c7-128">Der Windows Media Video 9-Bildschirm Encoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="935c7-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="935c7-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="935c7-129">Property</span></span></th>
<th><span data-ttu-id="935c7-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="935c7-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="935c7-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="935c7-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="935c7-132">Gibt den Aufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern der komprimierten Inhalte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="935c7-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="935c7-133">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-133">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-134">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="935c7-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="935c7-136">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="935c7-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="935c7-137">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-137">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-138">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="935c7-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="935c7-140">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="935c7-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="935c7-141">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-141">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-142">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="935c7-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="935c7-144">Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.</span><span class="sxs-lookup"><span data-stu-id="935c7-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="935c7-145">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-145">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-146">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="935c7-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="935c7-148">Gibt die Anzahl der vom Codec codierten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="935c7-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="935c7-149">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-149">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-150">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="935c7-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="935c7-152">Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="935c7-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="935c7-153">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-153">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-154">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="935c7-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="935c7-156">Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>abgelöst.</span><span class="sxs-lookup"><span data-stu-id="935c7-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="935c7-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="935c7-158">Gibt die Komplexität des Encoder-Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="935c7-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="935c7-159">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="935c7-160">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="935c7-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="935c7-162">Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="935c7-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="935c7-163">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-163">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-164">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="935c7-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="935c7-166">Gibt die Anzahl der während der Codierung gelöschten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="935c7-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="935c7-167">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-167">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-168">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="935c7-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="935c7-170">Gibt das Ende eines Codierungs Durchlaufs an.</span><span class="sxs-lookup"><span data-stu-id="935c7-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="935c7-171">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-171">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-172">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="935c7-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="935c7-174">Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="935c7-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="935c7-175">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-175">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-176">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="935c7-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="935c7-178">Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="935c7-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="935c7-179">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-179">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-180">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="935c7-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="935c7-182">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="935c7-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="935c7-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="935c7-184">Gibt die maximale Anzahl von durch den Codec unterstützten Durchläufen an.</span><span class="sxs-lookup"><span data-stu-id="935c7-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="935c7-185">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-185">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-186">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="935c7-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="935c7-188">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-188">Windows XP and later.</span></span> <span data-ttu-id="935c7-189">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-189">Read/write.</span></span><br/> <span data-ttu-id="935c7-190">Gibt die Anzahl von Durchläufen an, die vom Codec zum Codieren des Inhalts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="935c7-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="935c7-191">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-191">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-192">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="935c7-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="935c7-194">Gibt QP an.</span><span class="sxs-lookup"><span data-stu-id="935c7-194">Specifies QP.</span></span> <span data-ttu-id="935c7-195">Mögliche Werte sind 1,0 bis 31,0.</span><span class="sxs-lookup"><span data-stu-id="935c7-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="935c7-196">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="935c7-197">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="935c7-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="935c7-199">Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="935c7-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="935c7-200">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-200">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-201">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="935c7-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="935c7-203">Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="935c7-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="935c7-204">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-204">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-205">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="935c7-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="935c7-207">Gibt die Anzahl der Videorahmen an, die während des Codierungs Vorgangs an den Encoder übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="935c7-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="935c7-208">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-208">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-209">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="935c7-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="935c7-211">Gibt an, ob der Codec die VBR-Codierung (Variable-Bit-Rate) verwendet.</span><span class="sxs-lookup"><span data-stu-id="935c7-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="935c7-212">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-212">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-213">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="935c7-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="935c7-215">Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.</span><span class="sxs-lookup"><span data-stu-id="935c7-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="935c7-216">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-216">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-217">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="935c7-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="935c7-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="935c7-219">Die Menge an Inhalt in Millisekunden, die in den Modell Puffer passen kann.</span><span class="sxs-lookup"><span data-stu-id="935c7-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="935c7-220">Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="935c7-220">Windows XP and later,</span></span><br />
<span data-ttu-id="935c7-221">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="935c7-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="935c7-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="935c7-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="935c7-223">Gibt die Anzahl der Videorahmen an, die übersprungen wurden, weil Sie Duplikate vorheriger Frames waren.</span><span class="sxs-lookup"><span data-stu-id="935c7-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="935c7-224">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="935c7-224">Windows XP and later.</span></span><br />
<span data-ttu-id="935c7-225">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="935c7-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="935c7-226">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="935c7-226">Remarks</span></span>

<span data-ttu-id="935c7-227">Ein Bildschirm Codierungs Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als MFT (Media Foundation Transform) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="935c7-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="935c7-228">Ein Bildschirm Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="935c7-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="935c7-229">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Bildschirm Encoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="935c7-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="935c7-230">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="935c7-230">Operating system</span></span>            | <span data-ttu-id="935c7-231">Codierungs Verhalten</span><span class="sxs-lookup"><span data-stu-id="935c7-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935c7-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="935c7-232">Windows XP</span></span>                  | <span data-ttu-id="935c7-233">Ein Windows Media-Bildschirm Encoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="935c7-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="935c7-234">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="935c7-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="935c7-235">Standardmäßig verhält sich ein Windows Media-Bildschirm Encoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="935c7-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="935c7-236">Wenn Sie eine **imftransform** -Schnittstelle auf einem Bildschirm Encoder abrufen, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="935c7-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="935c7-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="935c7-237">Requirements</span></span>



| <span data-ttu-id="935c7-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="935c7-238">Requirement</span></span> | <span data-ttu-id="935c7-239">Wert</span><span class="sxs-lookup"><span data-stu-id="935c7-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="935c7-240">Client</span><span class="sxs-lookup"><span data-stu-id="935c7-240">Client</span></span><br/> | <span data-ttu-id="935c7-241">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="935c7-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="935c7-242">Header</span><span class="sxs-lookup"><span data-stu-id="935c7-242">Header</span></span><br/> | <dl> <span data-ttu-id="935c7-243"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="935c7-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="935c7-244">DLL</span><span class="sxs-lookup"><span data-stu-id="935c7-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="935c7-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935c7-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935c7-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="935c7-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935c7-247">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="935c7-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="935c7-248">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="935c7-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="935c7-249">Verwenden des Windows Media Video 9-Bildschirm Codecs</span><span class="sxs-lookup"><span data-stu-id="935c7-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="935c7-250">Windows Media Video 9-Bildschirm Decoder</span><span class="sxs-lookup"><span data-stu-id="935c7-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




