---
description: Encoder-Specific Registrierungseinträge
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d5d91d917be3940bcece4bed7c224e0f281dbb1cade5d0dc2c25872f89af93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711229"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific Registrierungseinträge


Zusätzlich zu den oben aufgeführten Einträgen für den Encoder müssen Sie Ihren Encoder auch unter der Kategorie Windows Imaging Component (WIC)-Encoder registrieren, damit die Ermittlungs-Engine ihn finden kann. Hierzu erstellen Sie die folgenden Registrierungseinträge. Die erste GUID in den folgenden Einträgen ist der Kategoriebezeichner (CATID) für WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registrieren eines Containerformats bei Metadatenautoren

Wenn Sie ein neues Containerformat für Ihren Codec erstellen, müssen Sie auch Registrierungseinträge erstellen, um Metadatenautoren für die Metadatenblöcke in Ihren Images zu unterstützen. Die folgenden Einträge müssen unter dem Klassenbezeichner (CLSID) des Metadatenwriters für jedes Metadatenformat erstellt werden, das in Ihrem Containerformat unterstützt wird. Wenn Ihr Codec einen TIFF-Container (Tagged Image File Format) verwendet, befinden sich diese Informationen bereits in der Registrierung, und Sie müssen diese Einträge nicht erstellen.

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

Wenn Sie ein Containerformat im TIFF- oder JPEG-Format verwenden, müssen Sie eine Zuordnung zwischen Ihrem Container und diesem Containerformat registrieren. Weitere Informationen finden Sie in der Einführung in [Integration mit Windows Fotogalerie und Windows Explorer.](-wic-integrationregentries.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Registrierungseinträge](-wic-generalregentries.md)
</dt> <dt>

[Encoderspezifische Registrierungseinträge](-wic-decoderregentries.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



