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
# <a name="decoder-specific-registry-entries"></a>Registrierungseinträge Decoder-Specific


Zusätzlich zu den Registrierungs Einträgen, die für alle Encoder und Decoder erforderlich sind, sind die folgenden Registrierungseinträge speziell für Decoder erforderlich.

Diese Einträge registrieren den Decoder in der Kategorie der WIC-Decoders (Windows Imaging Component). Die erste GUID in diesen Einträgen ist die Kategoriekennung (CATID) für [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

Wie im Abschnitt Ermittlung [und Schiedsgerichtsbarkeit](-wic-howwicworks.md) der Funktionsweise der Windows-Abbild Erstellungs Komponente erwähnt, basiert der Mechanismus, mit dem ein geeigneter Decoder für ein bestimmtes Abbild zur Laufzeit ermittelt werden kann, auf dem Abgleich eines in der Bilddatei eingebetteten identifizierenden Musters mit einem Muster, das im Registrierungs Eintrag des Decoders angegeben ist. Um die Lauf Zeit Ermittlung von Decodern zu aktivieren, müssen Sie das eindeutige identifizierende Muster für Ihr Bildformat wie folgt registrieren. Alle diese Registrierungseinträge sind erforderlich, ausgenommen den **EndOfStream** -Eintrag, der optional ist, wie in der folgenden Tabelle beschrieben.

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



| Wert       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Position    | Der Offset in der Datei, in der das Muster gefunden werden kann.                                                                                                                                                                                                                                                                        |
| Länge      | Die Länge des Musters.                                                                                                                                                                                                                                                                                                      |
| Muster     | Die eigentlichen Bits, die das Muster bilden. Dabei handelt es sich um die Bits, die bei der Ermittlung mit dem identifizierenden Muster in einer Bilddatei verglichen werden.                                                                                                                                                                                |
| Mask        | Ermöglicht Platzhalter Werte in Mustern. Die Maske wird durch Ausführen einer logischen and-Operation für das Muster und die Maske angewendet. Jedes Bit im Muster, das einem Bit in der Maske entspricht, das den Wert 0 (null) hat, wird ignoriert.                                                                                                       |
| EndOfStream | Der Offset des identifizierenden Musters sollte nicht mit dem Anfang, sondern vom Ende des Streams berechnet werden. Einige Bildformate platzieren das Erkennungsmuster an oder am Ende der Datei. Da der Standardwert für die Suche von Anfang an ist, können Sie diesen Eintrag weglassen, es sei denn, Ihr Muster befindet sich am Ende der Datei. |



 

Ein Codec kann mehr als ein identifizierendes Muster unterstützen. In diesem Fall würden Sie alle Schlüssel unter **HKEY \_ Classes \_ root \\ CLSID \\ {Decoder CLSID} \\ Patterns** wiederholen und den numerischen Schlüssel (0 im Beispiel) verwenden, um zwischen den verschiedenen Mustern zu unterscheiden. Sie müssen jeden der vier Werte unter dem Schlüssel für jedes Muster einschließen.

## <a name="registering-a-container-format-with-metadata-readers"></a>Registrieren eines Container Formats mit metadatenlesern

Wenn Sie ein neues Containerformat für Ihren Codec erstellen, müssen Sie auch Registrierungseinträge erstellen, um die Ermittlung von metadatenlesern für die Metadatenblöcke in den Bildern zu unterstützen, genauso wie bei den metadatenwritern. Die folgenden Einträge müssen unter dem Klassen Bezeichner (CLSID) des metadatenreaders für jedes Metadatenformat erstellt werden, das im Containerformat unterstützt wird. (Beachten Sie Folgendes: Wenn Ihr Codec einen Tagged Image File Format (TIFF)-Container verwendet, befinden sich diese Informationen bereits in der Registrierung.)

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

Da die Einträge für metadatenleser ebenfalls für die Ermittlung verwendet werden, ähneln sie sehr den Einträgen für Decoders. Diese Einträge werden von der komponentenfactory verwendet, um nach den von Ihrem Container unterstützten metadatenlesern zu suchen und die geeignete auszuwählen, wenn die [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Implementierung einen metadatenleser anfordert.



| Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Position   | Der Offset im Container des Metadatenblocks, in dem der Metadatenheader gefunden werden kann. Für Metadatenblöcke der obersten Ebene ist dies der Offset im Dateistream. Für Metadatenblöcke, die in anderen metadatenblöcken eingefügt werden, ist dies der Offset relativ zum enthaltenden Metadatenblock. |
| Muster    | Die eigentlichen Bits, die das Muster bilden. Dabei handelt es sich um die Bits, die bei der Ermittlung mit dem identifizierenden Muster in einer Bilddatei verglichen werden.                                                                                                                            |
| Mask       | Der Metadatenheader wird im Allgemeinen vom Metadatenhandler definiert. Sie sollten den standardmetadatenheader für jeden Leser verwenden, es sei denn, das Muster muss aus irgendeinem Grund ein anderes Format in Ihrem Container aufweisen.                                                          |
| DataOffset | Der Offset vom Anfang des metadatenheaders, bei dem die eigentlichen Daten beginnen. In Fällen, in denen sich die Metadaten nicht an einem bestimmten Offset aus dem Header befinden, kann dieser Eintrag ausgelassen werden.                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Codierungs spezifische Registrierungseinträge](-wic-encoderregentries.md)
</dt> <dt>

[Integration in Windows Photo Gallery und Windows-Explorer](-wic-integrationregentries.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



