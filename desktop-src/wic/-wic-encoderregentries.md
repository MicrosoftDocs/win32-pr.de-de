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
# <a name="encoder-specific-registry-entries"></a>Registrierungseinträge Encoder-Specific


Zusätzlich zu den oben aufgeführten Einträgen für den Encoder müssen Sie auch ihren Encoder in der Kategorie der WIC-Encoder (Windows Imaging Component) registrieren, damit die Ermittlungs-Engine Sie finden kann. Hierzu erstellen Sie die folgenden Registrierungseinträge. Die erste GUID in den folgenden Einträgen ist die Kategoriekennung (CATID) für wicbitmapcoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registrieren eines Container Formats mit metadatenwritern

Wenn Sie ein neues Containerformat für Ihren Codec erstellen, müssen Sie auch Registrierungseinträge erstellen, um metadatenwriter für die Metadatenblöcke in den Bildern zu unterstützen. Die folgenden Einträge müssen unter der Klassen-ID (CLSID) des metadatenwriters für jedes Metadatenformat erstellt werden, das im Containerformat unterstützt wird. Wenn Ihr Codec einen Tagged Image File Format (TIFF)-Container verwendet, befinden sich diese Informationen bereits in der Registrierung, und Sie müssen diese Einträge nicht erstellen.

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

Wenn Sie ein Containerformat im TIFF-oder JPEG-Format verwenden, müssen Sie eine Zuordnung zwischen Ihrem Container und diesem Containerformat registrieren. Weitere Informationen finden Sie unter Einführung in die [Windows-Fotogalerie und Windows-Explorer](-wic-integrationregentries.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Allgemeine Registrierungseinträge](-wic-generalregentries.md)
</dt> <dt>

[Codierungs spezifische Registrierungseinträge](-wic-decoderregentries.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



