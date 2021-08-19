---
description: In diesem Abschnitt wird beschrieben, wie VBR-Streams konfiguriert werden.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Verwenden der VBR-Codierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a9e1a61baf0539c0597e68f24dfad1496918012e52f778a1b7a64de27e5faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871229"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Verwenden der VBR-Codierung (Microsoft Media Foundation)

Wie im Thema [Codierungsmethoden](encodingmethods.md) beschrieben, wird die Codierung mit variabler Bitrate (VBR) verwendet, um die Konsistenz der Inhaltsqualität zu verbessern. Sie konfigurieren VBR-Streams auf die gleiche Weise wie CBR-Datenströme (Constant Bit Rate), mit Ausnahme der Pufferparameter (Bitrate und Pufferfenster). In diesem Abschnitt wird beschrieben, wie VBR-Streams konfiguriert werden.

## <a name="configuring-quality-based-vbr"></a>Konfigurieren der qualitätsbasierten VBR

Für die Codierung mit der qualitätsbasierten VBR-Methode sind keine vordefinierten Pufferparameter erforderlich. Stattdessen geben Sie eine Qualitätsstufe (von 0 bis 100) an, die der Encoder verwendet, um die entsprechenden Pufferparameter dynamisch zu bestimmen. Dieser Codierungsmodus verwendet nur einen Codierungsdurchlauf.

Sie können die unterstützten qualitätsbasierten VBR-Ausgabetypen für die Audiocodecs aufzählen. Sie müssen einen der Typen verwenden, die vom DMO zurückgegeben werden, wenn Sie den Ausgabetyp festlegen. Weitere Informationen finden Sie unter [Aufzählen von Audiotypen für bestimmte Codierungsmodi.](enumeratingaudiotypesforspecificencodingmodes.md)

Zum Konfigurieren eines qualitätsbasierten VBR-Videostreams müssen Sie die in der folgenden Tabelle aufgeführten Eigenschaften festlegen.



| Eigenschaft                                            | Beschreibung                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Legen Sie auf VARIANT \_ TRUE fest.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | Legen Sie auf den gewünschten Qualitätswert von 0 bis 100 fest. Nicht alle Qualitätswerte stellen diskrete Einstellungen dar. Weitere Informationen finden Sie in der Eigenschaftenbeschreibung. |



 

## <a name="configuring-unconstrained-vbr"></a>Konfigurieren einer uneingeschränkten VBR

Mit der uneingeschränkten VBR-Codierung kann der Encoder die Größe einzelner Stichproben ohne explizite Pufferlimits variieren. Die durchschnittliche Bitrate für die Dauer des resultierenden Inhalts muss jedoch kleiner oder gleich dem angegebenen Wert sein. Eine uneingeschränkte VBR erfordert zwei Codierungsdurchläufe.

Sie können die unterstützten VBR-Ausgabetypen mit zwei Durchläufen für die Audiocodecs aufzählen. Sie müssen einen der Typen verwenden, die vom DMO zurückgegeben werden, wenn Sie den Ausgabetyp festlegen. Weitere Informationen finden Sie unter [Aufzählen von Audiotypen für bestimmte Codierungsmodi.](enumeratingaudiotypesforspecificencodingmodes.md)

Um einen uneingeschränkten VBR-Videostream zu konfigurieren, müssen Sie die in der folgenden Tabelle aufgeführten Eigenschaften festlegen.



| Eigenschaft                                            | Beschreibung                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Legen Sie auf VARIANT \_ TRUE fest.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Legen Sie auf 2 fest.                            |
| [\_MFPKEY-MAUSG](mfpkey-ravgproperty.md)             | Legen Sie auf die gewünschte durchschnittliche Bitrate fest. |



 

## <a name="configuring-peak-constrained-vbr"></a>Konfigurieren Peak-Constrained VBR

VbR mit maximaler Auslastung ähnelt der uneingeschränkten VBR, da sie während der Dauer des Streams auf eine durchschnittliche Bitrate beschränkt ist. Darüber hinaus entspricht die VBR mit maximaler Auslastung einem Spitzenpuffer. Dieser Puffer wird mithilfe einer Spitzenbitrate und eines Spitzenpufferfensters beschrieben, genau wie ein CBR-Puffer durch eine durchschnittliche Bitrate und ein Pufferfenster beschrieben wird. Dieser Modus bietet dem Encoder Flexibilität beim Codieren einzelner Stichproben bei gleichzeitiger Einhaltung der Maximalen Einschränkungen. Dies ist besonders nützlich, wenn die Decodierung von einem Chip auf einem Gerät durchgeführt wird, z. B. einem DVD-Player, bei dem Hardwareeinschränkungen berücksichtigt werden müssen.

Die unterstützten Ausgabetypen des VBR-Audioencoders mit maximaler Auslastung sind die gleichen Typen, die für eine uneingeschränkte VBR aufzählt werden. Legen Sie die Spitzenwerte auf dem DMO fest, und verwenden Sie den übermittelten Typ. Weitere Informationen finden Sie unter [Aufzählen von Audiotypen für bestimmte Codierungsmodi.](enumeratingaudiotypesforspecificencodingmodes.md)

Zum Konfigurieren eines VBR-Videostreams mit maximaler Auslastung müssen Sie die in der folgenden Tabelle aufgeführten Eigenschaften mithilfe der **IPropertyBag::Write-Methode** festlegen.



| Eigenschaft                                            | Beschreibung                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Legen Sie auf VARIANT \_ TRUE fest.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Legen Sie auf 2 fest.                                                       |
| [\_MFPKEY-MAUSG](mfpkey-ravgproperty.md)             | Legen Sie auf die gewünschte durchschnittliche Bitrate fest.                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | Legen Sie auf die gewünschte Spitzenbitrate fest.                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | Legen Sie auf das Pufferfenster fest, das der Spitzenbitrate entspricht. |



 

> [!Note]  
> Es wird empfohlen, die Spitzenbitrate auf mindestens das Doppelte der durchschnittlichen Bitrate festzulegen. Das Festlegen der Spitzenrate auf einen niedrigeren Wert kann dazu führen, dass der Codec den Inhalt als CBR mit zwei Durchlauf anstelle von VBR mit maximaler Auslastung codiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> <dt>

[Verwenden von Two-Pass Encoding](usingtwoencodingpasses.md)
</dt> <dt>

[Arbeiten mit Audio](workingwithaudio.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



