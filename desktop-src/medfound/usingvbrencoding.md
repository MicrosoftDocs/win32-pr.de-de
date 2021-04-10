---
description: In diesem Abschnitt wird beschrieben, wie VBR-Streams konfiguriert werden.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Verwenden der VBR-Codierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215002"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Verwenden der VBR-Codierung (Microsoft Media Foundation)

Wie im Thema [Codierungs Methoden](encodingmethods.md) ausführlich beschrieben, wird die Codierung der Variablen Bitrate (VBR) verwendet, um die Konsistenz der Inhaltsqualität zu verbessern. Sie konfigurieren VBR-Streams auf die gleiche Weise, wie Sie die konstanten Bitrate (CBR)-Streams mit Ausnahme der Puffer Parameter (Bitrate und Puffer Fenster) codieren. In diesem Abschnitt wird beschrieben, wie VBR-Streams konfiguriert werden.

## <a name="configuring-quality-based-vbr"></a>Konfigurieren von Qualitäts basierter VBR

Bei der Codierung mit der Qualitäts basierten VBR-Methode sind keine vordefinierten Puffer Parameter erforderlich. Stattdessen geben Sie eine Qualitätsstufe (von 0 bis 100) an, die der Encoder verwendet, um die entsprechenden Puffer Parameter dynamisch zu bestimmen. Dieser Codierungs Modus verwendet nur einen Codierungs Durchlauf.

Sie können die unterstützten Qualitäts basierten VBR-Ausgabetypen für die Audiocodecs auflisten. Sie müssen einen der Typen verwenden, die vom DMO beim Festlegen des Ausgabe Typs zurückgegeben werden. Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).

Um einen Qualitäts basierten VBR-Videostream zu konfigurieren, müssen Sie die Eigenschaften festlegen, die in der folgenden Tabelle aufgeführt sind.



| Eigenschaft                                            | BESCHREIBUNG                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [mfpkey \_ vbrenabled](mfpkey-vbrenabledproperty.md) | Auf Variant true festgelegt \_ .                                                                                                                                   |
| [mfpkey \_ vbrquality](mfpkey-vbrqualityproperty.md) | Legen Sie auf den gewünschten Qualitäts Wert von 0 bis 100 fest. Nicht alle Qualitätswerte stellen diskrete Einstellungen dar. Weitere Informationen finden Sie in der Eigenschafts Beschreibung. |



 

## <a name="configuring-unconstrained-vbr"></a>Konfigurieren von nicht eingeschränktem VBR

Bei der nicht eingeschränkten VBR-Codierung kann der Encoder die Größe einzelner Stichproben ohne explizite Puffer Limits variieren. Die durchschnittliche Bitrate für die Dauer des resultierenden Inhalts muss jedoch kleiner oder gleich dem angegebenen Wert sein. Für den uneingeschränkten VBR sind zwei Codierungs Überläufen erforderlich.

Sie können die unterstützten zwei-Pass-VBR-Ausgabetypen für die Audiocodecs auflisten. Sie müssen einen der Typen verwenden, die vom DMO beim Festlegen des Ausgabe Typs zurückgegeben werden. Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).

Um einen unbeschränkten VBR-Videostream zu konfigurieren, müssen Sie die Eigenschaften festlegen, die in der folgenden Tabelle aufgeführt sind.



| Eigenschaft                                            | BESCHREIBUNG                          |
|-----------------------------------------------------|--------------------------------------|
| [mfpkey \_ vbrenabled](mfpkey-vbrenabledproperty.md) | Auf Variant true festgelegt \_ .                |
| [mfpkey- \_ passesused](mfpkey-passesusedproperty.md) | Legen Sie auf 2 fest.                            |
| [mfpkey \_ Ravg](mfpkey-ravgproperty.md)             | Legen Sie auf die gewünschte durchschnittliche Bitrate fest. |



 

## <a name="configuring-peak-constrained-vbr"></a>Konfigurieren von Peak-Constrained VBR

VBR mit hoher Einschränkung ist so ähnlich wie der eingeschränkte VBR, da es sich auf eine durchschnittliche Bitrate während der Dauer des Streams beschränkt. Darüber hinaus entspricht VBR mit hoher Einschränkung einem Spitzen Puffer. Dieser Puffer wird mit einer Spitzen Bitrate und einem Spitzen Puffer Fenster beschrieben, ebenso wie ein CBR-Puffer durch eine durchschnittliche Bitrate und ein Puffer Fenster beschrieben wird. Dieser Modus bietet dem Encoder Flexibilität bei der Codierung einzelner Beispiele, während die Spitzen Grenzen einhalten. Dies ist besonders nützlich, wenn die Decodierung von einem Chip in einem Gerät durchgeführt wird, wie z. b. bei einem DVD-Player, bei dem Hardware Einschränkungen berücksichtigt werden müssen.

Die unterstützten leistungsstarken VBR-Audioencoder-Ausgabetypen sind dieselben Typen, die für den nicht eingeschränkten VBR aufgelistet sind. Legen Sie die Spitzenwerte für den DMO fest, und verwenden Sie den übermittelten Typ. Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).

Zum Konfigurieren eines VBR-Videostreams mit hoher Größe müssen Sie die in der folgenden Tabelle aufgeführten Eigenschaften mithilfe der **IPropertyBag:: Write** -Methode festlegen.



| Eigenschaft                                            | BESCHREIBUNG                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [mfpkey \_ vbrenabled](mfpkey-vbrenabledproperty.md) | Auf Variant true festgelegt \_ .                                           |
| [mfpkey- \_ passesused](mfpkey-passesusedproperty.md) | Legen Sie auf 2 fest.                                                       |
| [mfpkey \_ Ravg](mfpkey-ravgproperty.md)             | Legen Sie auf die gewünschte durchschnittliche Bitrate fest.                            |
| [mfpkey- \_ Rmax](mfpkey-rmaxproperty.md)             | Legen Sie auf die gewünschte Spitzen Bitrate fest.                               |
| [mfpkey ( \_ bmax)](mfpkey-bmaxproperty.md)             | Wird auf das Puffer Fenster festgelegt, das der Spitzen Bitrate entspricht. |



 

> [!Note]  
> Es wird empfohlen, die Spitzen Bitrate auf mindestens doppelte die durchschnittliche Bitrate festzulegen. Das Festlegen der Spitzen Rate auf einen niedrigeren Wert kann bewirken, dass der Codec den Inhalt als zwei-Pass-CBR anstelle von VBR mit eingeschränkter Spitzen Codierung codiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> <dt>

[Verwenden von Two-Pass Codierung](usingtwoencodingpasses.md)
</dt> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



