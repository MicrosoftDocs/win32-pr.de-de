---
description: Der MPEG-2-Video Decoder ist eine Media Foundation Transformation, die MPEG-1-und MPEG-2-Videos decodiert.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: MPEG-2-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527902"
---
# <a name="mpeg-2-video-decoder"></a>MPEG-2-Video Decoder

Der MPEG-2-Video Decoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die MPEG-1-und MPEG-2-Videos decodiert. Der Decoder unterstützt MPEG-2-Videos mit einfachem und einem Hauptprofil (H. 262, ISO/IEC 13818-2) und MPEG-1-Video (ISO/IEC 11172-2).

## <a name="input-types"></a>Eingabetypen

Der Decoder unterstützt die folgenden Eingabemedien Typen.

| Attribut                                                 | BESCHREIBUNG                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md) | **MF MediaType- \_ Video**                                                  |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)        | **MF-Format- \_ MPEG1**<br/> **MF-Format ( \_ MPEG2)**<br/> |



 

## <a name="output-types"></a>Ausgabetypen

Der Decoder unterstützt die folgenden Ausgabetypen.

| Attribut                                                 | BESCHREIBUNG                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md) | **MF MediaType- \_ Video**                                                                                                                                                         |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)        | **MF-Format \_ I420**<br/> **MF-Format ( \_ IYUV)**<br/> **MF-Format \_ NV12**<br/> **MF-Format \_ im YUY2**<br/> **MF-Format \_ YV12**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der MPEG-2-Video Decoder macht die folgenden Schnittstellen verfügbar:

-   [**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**Imfrealtimeclient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Die Eingabe für den Decoder muss ein elementaren Stream sein. Die maximal unterstützte Auflösung beträgt 1920 × 1088 Pixel.

Der Decoder unterstützt die DirectX-Video Beschleunigung (DXVA) mithilfe von Microsoft Direct3D 9 oder Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Besondere Decodierungs Modi

-   **Modus mit niedriger Latenz.** Dieser Modus eignet sich für Szenarien wie z. b. die Echtzeitkommunikation. Dies reduziert die Start Latenz, sodass der Decoder das erste Ausgabe Beispiel früher erzeugt. Der Decoder puffert jedoch weniger Beispiele in diesem Modus, was potenziell zu einem Fehler führen kann, da der Decoder nicht so viele Frames im Voraus decodiert. Um den Modus mit niedriger Latenz zu aktivieren, legen Sie das Attribut [codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md) fest.
-   **Diejenigen.** Zum exakten suchen müssen Sie die [**imftransform:: setoutputbounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) -Methode aufrufen. Wenn diese Methode aufgerufen wird, gibt der Decoder nur Frames aus, die innerhalb des vom Aufrufer angegebenen Zeitstempels liegen.
-   **Miniatur Generierungs Modus**. Dieser Modus ist für die schnelle Generierung von Miniaturbildern vorgesehen. In diesem Modus decodiert der Decoder anfänglich nur I-Frames. Wenn innerhalb einer bestimmten Anzahl von Frames kein Frame gefunden wird, startet der Decoder die Decodierung von P-Frames und gibt nicht-– I-Frames in einem festgelegten Intervall (einer pro *N* Bilder) aus, bis ein I-Frame erreicht wird. Legen Sie die [codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md) -Eigenschaft fest, um den Modus für die Miniatur Generierung zu aktivieren.
-   **Trick Wiedergabe.** Der Decoder kann bei Raten schneller als in Echtzeit decodieren. Bei höheren Wiedergabe Raten schaltet der Decoder zum Decodieren von I-Frames um. Bei umgekehrter Wiedergabe werden nur I-Frames decodiert.

### <a name="codec-properties"></a>Codec-Eigenschaften

Der Decoder unterstützt die folgenden Eigenschaften durch die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.



| Eigenschaft                                                                                                      | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.                                                             |
| [Codecapi \_ avdecvideoacceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Aktiviert oder deaktiviert die hardwarebeschleunigte Decodierung.                                                         |
| [Codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md)                                                   | Aktiviert oder deaktiviert den Modus mit niedriger Latenz.                                                                      |
| [MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen \_ in \_ nativer \_ Reihenfolge verfügbar.](mft-decoder-expose-output-types-in-native-order.md) | Gibt an, ob der Decoder Ausgabetypen verfügbar macht, die für die Transcodierung vor anderen Formaten geeignet sind. |



 

Die folgenden Eigenschaften können auch über die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle festgelegt werden:

-   [Codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [Codecapi \_ avdecvideoacceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [Codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Einschränkungen

-   Der Decoder wird auf IA-64 – basierten Plattformen nicht unterstützt.
-   Der Decoder unterstützt keine CSS-Entschlüsselung oder Wiedergabe verschlüsselter DVDs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
