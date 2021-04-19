---
description: Registrierungseinträge Decoder-Specific
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Registrierungseinträge Decoder-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362990"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="dde54-103">Registrierungseinträge Decoder-Specific</span><span class="sxs-lookup"><span data-stu-id="dde54-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="dde54-104">Zusätzlich zu den Registrierungs Einträgen, die für alle Encoder und Decoder erforderlich sind, sind die folgenden Registrierungseinträge speziell für Decoder erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dde54-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="dde54-105">Diese Einträge registrieren den Decoder in der Kategorie der WIC-Decoders (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="dde54-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="dde54-106">Die erste GUID in diesen Einträgen ist die Kategoriekennung (CATID) für [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="dde54-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="dde54-107">Wie im Abschnitt Ermittlung [und Schiedsgerichtsbarkeit](-wic-howwicworks.md) der Funktionsweise der Windows-Abbild Erstellungs Komponente erwähnt, basiert der Mechanismus, mit dem ein geeigneter Decoder für ein bestimmtes Abbild zur Laufzeit ermittelt werden kann, auf dem Abgleich eines in der Bilddatei eingebetteten identifizierenden Musters mit einem Muster, das im Registrierungs Eintrag des Decoders angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dde54-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="dde54-108">Um die Lauf Zeit Ermittlung von Decodern zu aktivieren, müssen Sie das eindeutige identifizierende Muster für Ihr Bildformat wie folgt registrieren.</span><span class="sxs-lookup"><span data-stu-id="dde54-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="dde54-109">Alle diese Registrierungseinträge sind erforderlich, ausgenommen den **EndOfStream** -Eintrag, der optional ist, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dde54-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="dde54-110">Wert</span><span class="sxs-lookup"><span data-stu-id="dde54-110">Value</span></span>       | <span data-ttu-id="dde54-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dde54-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde54-112">Position</span><span class="sxs-lookup"><span data-stu-id="dde54-112">Position</span></span>    | <span data-ttu-id="dde54-113">Der Offset in der Datei, in der das Muster gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="dde54-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="dde54-114">Länge</span><span class="sxs-lookup"><span data-stu-id="dde54-114">Length</span></span>      | <span data-ttu-id="dde54-115">Die Länge des Musters.</span><span class="sxs-lookup"><span data-stu-id="dde54-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="dde54-116">Muster</span><span class="sxs-lookup"><span data-stu-id="dde54-116">Pattern</span></span>     | <span data-ttu-id="dde54-117">Die eigentlichen Bits, die das Muster bilden.</span><span class="sxs-lookup"><span data-stu-id="dde54-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="dde54-118">Dabei handelt es sich um die Bits, die bei der Ermittlung mit dem identifizierenden Muster in einer Bilddatei verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="dde54-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="dde54-119">Mask</span><span class="sxs-lookup"><span data-stu-id="dde54-119">Mask</span></span>        | <span data-ttu-id="dde54-120">Ermöglicht Platzhalter Werte in Mustern.</span><span class="sxs-lookup"><span data-stu-id="dde54-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="dde54-121">Die Maske wird durch Ausführen einer logischen and-Operation für das Muster und die Maske angewendet.</span><span class="sxs-lookup"><span data-stu-id="dde54-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="dde54-122">Jedes Bit im Muster, das einem Bit in der Maske entspricht, das den Wert 0 (null) hat, wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dde54-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="dde54-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="dde54-123">EndOfStream</span></span> | <span data-ttu-id="dde54-124">Der Offset des identifizierenden Musters sollte nicht mit dem Anfang, sondern vom Ende des Streams berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="dde54-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="dde54-125">Einige Bildformate platzieren das Erkennungsmuster an oder am Ende der Datei.</span><span class="sxs-lookup"><span data-stu-id="dde54-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="dde54-126">Da der Standardwert für die Suche von Anfang an ist, können Sie diesen Eintrag weglassen, es sei denn, Ihr Muster befindet sich am Ende der Datei.</span><span class="sxs-lookup"><span data-stu-id="dde54-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="dde54-127">Ein Codec kann mehr als ein identifizierendes Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dde54-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="dde54-128">In diesem Fall würden Sie alle Schlüssel unter **HKEY \_ Classes \_ root \\ CLSID \\ {Decoder CLSID} \\ Patterns** wiederholen und den numerischen Schlüssel (0 im Beispiel) verwenden, um zwischen den verschiedenen Mustern zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="dde54-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="dde54-129">Sie müssen jeden der vier Werte unter dem Schlüssel für jedes Muster einschließen.</span><span class="sxs-lookup"><span data-stu-id="dde54-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="dde54-130">Registrieren eines Container Formats mit metadatenlesern</span><span class="sxs-lookup"><span data-stu-id="dde54-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="dde54-131">Wenn Sie ein neues Containerformat für Ihren Codec erstellen, müssen Sie auch Registrierungseinträge erstellen, um die Ermittlung von metadatenlesern für die Metadatenblöcke in den Bildern zu unterstützen, genauso wie bei den metadatenwritern.</span><span class="sxs-lookup"><span data-stu-id="dde54-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="dde54-132">Die folgenden Einträge müssen unter dem Klassen Bezeichner (CLSID) des metadatenreaders für jedes Metadatenformat erstellt werden, das im Containerformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dde54-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="dde54-133">(Beachten Sie Folgendes: Wenn Ihr Codec einen Tagged Image File Format (TIFF)-Container verwendet, befinden sich diese Informationen bereits in der Registrierung.)</span><span class="sxs-lookup"><span data-stu-id="dde54-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="dde54-134">Da die Einträge für metadatenleser ebenfalls für die Ermittlung verwendet werden, ähneln sie sehr den Einträgen für Decoders.</span><span class="sxs-lookup"><span data-stu-id="dde54-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="dde54-135">Diese Einträge werden von der komponentenfactory verwendet, um nach den von Ihrem Container unterstützten metadatenlesern zu suchen und die geeignete auszuwählen, wenn die [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Implementierung einen metadatenleser anfordert.</span><span class="sxs-lookup"><span data-stu-id="dde54-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="dde54-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dde54-136">Value</span></span>      | <span data-ttu-id="dde54-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dde54-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde54-138">Position</span><span class="sxs-lookup"><span data-stu-id="dde54-138">Position</span></span>   | <span data-ttu-id="dde54-139">Der Offset im Container des Metadatenblocks, in dem der Metadatenheader gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="dde54-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="dde54-140">Für Metadatenblöcke der obersten Ebene ist dies der Offset im Dateistream.</span><span class="sxs-lookup"><span data-stu-id="dde54-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="dde54-141">Für Metadatenblöcke, die in anderen metadatenblöcken eingefügt werden, ist dies der Offset relativ zum enthaltenden Metadatenblock.</span><span class="sxs-lookup"><span data-stu-id="dde54-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="dde54-142">Muster</span><span class="sxs-lookup"><span data-stu-id="dde54-142">Pattern</span></span>    | <span data-ttu-id="dde54-143">Die eigentlichen Bits, die das Muster bilden.</span><span class="sxs-lookup"><span data-stu-id="dde54-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="dde54-144">Dabei handelt es sich um die Bits, die bei der Ermittlung mit dem identifizierenden Muster in einer Bilddatei verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="dde54-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="dde54-145">Mask</span><span class="sxs-lookup"><span data-stu-id="dde54-145">Mask</span></span>       | <span data-ttu-id="dde54-146">Der Metadatenheader wird im Allgemeinen vom Metadatenhandler definiert.</span><span class="sxs-lookup"><span data-stu-id="dde54-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="dde54-147">Sie sollten den standardmetadatenheader für jeden Leser verwenden, es sei denn, das Muster muss aus irgendeinem Grund ein anderes Format in Ihrem Container aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dde54-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="dde54-148">DataOffset</span><span class="sxs-lookup"><span data-stu-id="dde54-148">DataOffset</span></span> | <span data-ttu-id="dde54-149">Der Offset vom Anfang des metadatenheaders, bei dem die eigentlichen Daten beginnen.</span><span class="sxs-lookup"><span data-stu-id="dde54-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="dde54-150">In Fällen, in denen sich die Metadaten nicht an einem bestimmten Offset aus dem Header befinden, kann dieser Eintrag ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="dde54-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="dde54-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dde54-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dde54-152">**Licher**</span><span class="sxs-lookup"><span data-stu-id="dde54-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dde54-153">Codierungs spezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="dde54-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="dde54-154">Integration in Windows Photo Gallery und Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="dde54-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="dde54-155">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="dde54-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="dde54-156">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="dde54-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



