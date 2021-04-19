---
title: Auswählen einer Codierungsmethode
description: Auswählen einer Codierungsmethode
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- Profile, auswählen von Codierungs Methoden
- Profile, Codierungs Methoden
- Codecs, auswählen von Codierungs Methoden
- Codecs, Codierungs Methoden
- Profile, auswählen von Codierungs Methoden
- Codecs, auswählen von Codierungs Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337982"
---
# <a name="choosing-an-encoding-method"></a>Auswählen einer Codierungsmethode

Einige Codecs, wie der Windows Media Video 9-Codec, unterstützen mehrere Codierungs Methoden. Die Codierungsmethode, die Sie für einen Stream auswählen, hängt davon ab, wie der Stream übermittelt werden soll. In der folgenden Tabelle wird beschrieben, wann die verschiedenen Codierungs Methoden verwendet werden.



| Codiermethode                | BESCHREIBUNG                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1-Pass-Konstante Bitrate (CBR) | Die einzige Option für Live Streaming. Codiert in eine vorhersagbare Bitrate und bietet die niedrigste Qualität aller Codierungs Methoden.                                                                    |
| 2-Pass-CBR                     | Verwenden Sie für Dateien, die über ein Netzwerk an einen Client Leser gestreamt werden, aber nicht von einer Live Quelle übertragen werden. Codiert in eine vorhersagbare Bitrate, aber mit besserer Qualität als 1-Pass-CBR. |
| 1-Pass-Variable Bitrate (VBR) | Verwenden Sie, wenn Sie die Qualität der codierten Ausgabe angeben müssen. Bietet die konsistente Qualität aller Codierungs Methoden. Wird nur für lokale Dateien oder zum Herunterladen verwendet.                        |
| 2-Pass-VBR – nicht eingeschränkt     | Verwenden Sie, wenn Sie eine Bandbreite angeben müssen, aber Schwankungen in Bezug auf die angegebene Bandbreite sind zulässig. Für lokale Dateien oder nur herunterladen.                                                    |
| 2-Pass-VBR – eingeschränkt       | Verwenden Sie unter denselben Bedingungen wie nicht eingeschränkt, aber wenn Sie eine maximale momentane Bitrate angeben müssen. Für lokale Dateien oder nur herunterladen.                                                |



 

In der folgenden Tabelle werden die Codierungs Methoden aufgelistet, die von den Codecs unterstützt werden, die mit dem Windows Media-Format SDK ausgeliefert werden.



| Codec                                  | CBR | 2-Pass-CBR | VBR | 2-Pass-VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media Video 9                  | X   | X          | X   | X          |
| Windows Media Audio 9 und höher        | X   | X          | X   | X          |
| Windows Media Video 9-Bildschirm           | X   |            | X   |            |
| Windows Media Audio 9-Stimme            | X   |            |     |            |
| Windows Media Audio Professional       | X   | X          | X   | X          |
| Verlust von Windows Media Audio Verlust           |     |            | X   |            |
| Windows Media Video 9-Image und höher  | X   |            | X   |            |
| Erweiterte profile Windows Media Video 9 | X   | X          | X   | X          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwerfen von Profilen**](designing-profiles.md)
</dt> <dt>

[**Codierung mit konstanter Bitrate (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Zwei-Pass-Codierung**](two-pass-encoding.md)
</dt> <dt>

[**Codierung der Variablen Bitrate (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




