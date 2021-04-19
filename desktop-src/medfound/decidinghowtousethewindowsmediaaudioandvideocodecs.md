---
description: Verwenden der Codec-und DSP-Objekte
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Verwenden der Codec-und DSP-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363888"
---
# <a name="using-the-codec-and-dsp-objects"></a>Verwenden der Codec-und DSP-Objekte

Es gibt mehrere Möglichkeiten, die Windows Media Audio-und Video Codecs und die DSPs zu verwenden, um den Inhalt digitaler Medien zu codieren, zu decodieren oder zu transformieren. Der Windows Media Audio und der Videocodec und die DSP-API sind für Benutzer gedacht, die Codec-und DSP-Objekte manuell konfigurieren müssen, oder Sie können Sie außerhalb des Kontexts eines der Windows Media SDKs verwenden, wie z. b. das Windows Media-Format-SDK oder Media Foundation SDK.

Inhalts Ersteller und Endbenutzer können mit einer Vielzahl von Tools und Anwendungen Inhalte in Windows Media Audio oder Windows Media Video Streams codieren. Windows Media Encoder ist beispielsweise speziell dafür konzipiert, den Codierungsprozess zu vereinfachen. Ebenso wurde Windows Media Player speziell für die Verwendung von digitalen Mediendaten entwickelt, die in Windows Media-Formaten codiert sind. Für viele Anwendungen ist nur die Verwendung des Windows Media Encoder SDK oder des Windows Media Player SDK erforderlich. Insbesondere sind diese beiden Technologien für Szenarien geeignet, die der Funktionalität der von Ihnen automatisierten Tools ähneln.

Wenn Sie eine bessere Kontrolle über den Codierungs-oder Decodierungs Prozess benötigen, aber trotzdem beabsichtigen, das Advanced Systems Format (ASF) als Container für Ihre Mediendaten zu verwenden, ist das Windows Media-Format-SDK möglicherweise eine gute Wahl. Die Objekte des SDK für den Windows Media-Format bieten ein flexibles Framework zum Erstellen von ASF-Dateien und bieten integrierte Unterstützung für die Windows Media Audio-und Video Codecs.

Das Media Foundation SDK, das neu für Windows Vista ist, vereinfacht das Codieren und decodieren erheblich, indem es eine anpassbare Medien Pipeline bereitstellt. Sie können die Eigenschaften für die Eingabe-und Ausgabemedien festlegen, und der Media Foundation topologielader konfiguriert die erforderlichen Codecs und DSPs für Sie.

Der Hauptgrund für die direkte Verwendung der Codec-Objekte ist die Verwendung des Windows Media Audio und der Video Codecs außerhalb des ASF-Containers. Die Verwendung der Codec-und DSP-Objekte bietet auch eine Steuerungsebene, die mit einer der abstrahierten Technologien nicht verfügbar ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



