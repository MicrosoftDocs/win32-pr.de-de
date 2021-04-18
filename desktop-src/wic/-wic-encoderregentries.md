---
description: Registrierungseinträge Encoder-Specific
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Registrierungseinträge Encoder-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358577"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="094da-103">Registrierungseinträge Encoder-Specific</span><span class="sxs-lookup"><span data-stu-id="094da-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="094da-104">Zusätzlich zu den oben aufgeführten Einträgen für den Encoder müssen Sie auch ihren Encoder in der Kategorie der WIC-Encoder (Windows Imaging Component) registrieren, damit die Ermittlungs-Engine Sie finden kann.</span><span class="sxs-lookup"><span data-stu-id="094da-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="094da-105">Hierzu erstellen Sie die folgenden Registrierungseinträge.</span><span class="sxs-lookup"><span data-stu-id="094da-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="094da-106">Die erste GUID in den folgenden Einträgen ist die Kategoriekennung (CATID) für wicbitmapcoders.</span><span class="sxs-lookup"><span data-stu-id="094da-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="094da-107">Registrieren eines Container Formats mit metadatenwritern</span><span class="sxs-lookup"><span data-stu-id="094da-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="094da-108">Wenn Sie ein neues Containerformat für Ihren Codec erstellen, müssen Sie auch Registrierungseinträge erstellen, um metadatenwriter für die Metadatenblöcke in den Bildern zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="094da-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="094da-109">Die folgenden Einträge müssen unter der Klassen-ID (CLSID) des metadatenwriters für jedes Metadatenformat erstellt werden, das im Containerformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="094da-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="094da-110">Wenn Ihr Codec einen Tagged Image File Format (TIFF)-Container verwendet, befinden sich diese Informationen bereits in der Registrierung, und Sie müssen diese Einträge nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="094da-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="094da-111">Wenn Sie ein Containerformat im TIFF-oder JPEG-Format verwenden, müssen Sie eine Zuordnung zwischen Ihrem Container und diesem Containerformat registrieren.</span><span class="sxs-lookup"><span data-stu-id="094da-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="094da-112">Weitere Informationen finden Sie unter Einführung in die [Windows-Fotogalerie und Windows-Explorer](-wic-integrationregentries.md).</span><span class="sxs-lookup"><span data-stu-id="094da-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="094da-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="094da-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="094da-114">**Licher**</span><span class="sxs-lookup"><span data-stu-id="094da-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="094da-115">Allgemeine Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="094da-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="094da-116">Codierungs spezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="094da-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="094da-117">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="094da-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="094da-118">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="094da-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



