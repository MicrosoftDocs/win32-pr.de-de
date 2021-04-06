---
title: Bitrate
description: Bitrate
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- SDK für Windows Media-Format, Bitraten
- Advanced Systems Format (ASF), Bitraten
- ASF (Advanced Systems Format), Bitraten
- Bitraten, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713710"
---
# <a name="bit-rate"></a>Bitrate

Die Bitrate bezieht sich auf die Menge der Daten, die pro Sekunde von einer ASF-Datei übermittelt werden. Bitraten Messungen liegen in Bits pro Sekunde (Bit/s) oder kbit pro Sekunde (Kbit/s) vor. Die Bitrate wird häufig mit der Bandbreite verwechselt, bei der es sich um eine Messung der Datenübertragungs Kapazität eines Netzwerks handelt. Bandbreite wird auch in Bit/s und Kbit/s gemessen.

Das Windows Media-Format-SDK kann zum Erstellen von Anwendungen verwendet werden, die das Streaming von Windows Media-basierten Inhalten aus Internet-oder Intranetstandorten ermöglichen. Wenn Sie Daten über ein Netzwerk oder das Internet streamen, ist die Bitrate von entscheidender Bedeutung für den Endbenutzer. Wenn die für das Netzwerk verfügbare Bandbreite kleiner ist als die Bitrate der ASF-Datei, wird die Wiedergabe der Datei auf irgendeine Weise unterbrochen. In der Regel werden bei unzureichender Bandbreite entweder Stichproben übersprungen oder eine Pause in der Wiedergabe angezeigt, während mehr Daten gepuffert werden.

Jeder ASF-Datei wird zum Zeitpunkt der Erstellung ein Bitrate-Wert zugewiesen, basierend auf dem Typ und der Anzahl der Streams, die im verwendeten Profil enthalten sind. Einzelne Streams verfügen über eigene Bitraten. Die Bitraten können konstant sein (die ursprünglichen Daten werden auf eine Weise komprimiert, um einen konstanten Datenfluss mit ungefähr derselben Geschwindigkeit aufrechtzuerhalten) oder eine Variable (die ursprünglichen Daten werden so komprimiert, dass Sie die gleiche Qualität erhalten, obwohl dies einen ungleichen Datenfluss bedeuten kann). Verschiedene Bitrate-Typen können auf verschiedene Datenströme innerhalb derselben Datei angewendet werden.

Sie können denselben Inhalt in mehrere unterschiedliche Streams codieren, von denen jeder eine andere Bitrate hat. Anschließend können Sie die Datenströme so konfigurieren, dass Sie sich gegenseitig ausschließen. Dies ermöglicht es Ihnen, eine einzelne Datei zu erstellen, die an Benutzer mit unterschiedlichen Bandbreiten gestreamt werden kann. Diese Funktion wird als mehrfache Bitrate oder MBR bezeichnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Codierung mit konstanter Bitrate (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> <dt>

[**Codierung der Variablen Bitrate (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




