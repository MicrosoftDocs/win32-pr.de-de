---
title: Bitrate
description: Bitrate
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Medienformat-SDK, Bitraten
- Advanced Systems Format (ASF), Bitraten
- ASF (Advanced Systems Format), Bitraten
- Bitraten, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a15332e18d47a72974098ad38c6a942ceaf4780e1b79dffacd49382e3416ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809870"
---
# <a name="bit-rate"></a>Bitrate

Bitrate bezieht sich auf die Datenmenge pro Sekunde, die von einer ASF-Datei übermittelt wird. Bitratenmessungen erfolgen in Bits pro Sekunde (Bps) oder Kilobits pro Sekunde (KBit/s). Die Bitrate wird häufig mit der Bandbreite verwechselt. Dies ist eine Messung der Datenübertragungskapazität eines Netzwerks. Die Bandbreite wird auch in Bps und KBit/s gemessen.

Das Windows Media Format SDK kann verwendet werden, um Anwendungen zu erstellen, die Streaming Windows medienbasierte Inhalte von Internet- oder Intranetspeicherorten bereitstellen. Wenn Sie Daten über ein Netzwerk oder das Internet streamen, ist die Bitrate von entscheidender Bedeutung für die Endbenutzererfahrung. Wenn die für das Netzwerk verfügbare Bandbreite kleiner als die Bitrate der ASF-Datei ist, wird die Wiedergabe der Datei in irgendeiner Weise unterbrochen. In der Regel führt unzureichende Bandbreite dazu, dass entweder Samplings übersprungen werden oder die Wiedergabe angehalten wird, während mehr Daten gepuffert werden.

Jeder ASF-Datei wird zum Zeitpunkt der Erstellung ein Bitratenwert zugewiesen, der auf dem Typ und der Anzahl der Streams basiert, die im verwendeten Profil enthalten sind. Einzelne Datenströme verfügen über eigene Bitraten. Bitraten können konstant sein (die ursprünglichen Daten werden so komprimiert, dass ein konstanter Datenfluss mit ungefähr derselben Rate beibehalten wird) oder variabel (die ursprünglichen Daten werden so komprimiert, dass die gleiche Qualität beibehalten wird, obwohl dies zu ungleichmäßigen Datenflüssen führen kann). Verschiedene Bitratentypen können auf verschiedene Datenströme innerhalb derselben Datei angewendet werden.

Sie können denselben Inhalt in mehreren verschiedenen Datenströmen codieren, die jeweils eine andere Bitrate aufweisen. Anschließend können Sie die Streams so konfigurieren, dass sie sich gegenseitig ausschließen. Dadurch können Sie eine einzelne Datei erstellen, die an Benutzer mit unterschiedlichen Bandbreiten gestreamt werden kann. Dieses Feature wird als Multiple Bit Rate (MBR) bezeichnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**CBR-Codierung (Constant Bit Rate)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> <dt>

[**Codierung mit variabler Bitrate (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




