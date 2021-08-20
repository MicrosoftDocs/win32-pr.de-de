---
title: Auswählen einer Codierungsmethode
description: Auswählen einer Codierungsmethode
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- Profile,Auswählen von Codierungsmethoden
- Profile,Codierungsmethoden
- Codecs,Auswählen von Codierungsmethoden
- Codecs,Codierungsmethoden
- Profile,Auswählen von Codierungsmethoden
- Codecs,Auswählen von Codierungsmethoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a780798885e86b515a8d111797af304a58f13c962ecab7f7862dfb1790411
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656130"
---
# <a name="choosing-an-encoding-method"></a>Auswählen einer Codierungsmethode

Einige Codecs wie der Windows Media Video 9-Codec unterstützen mehrere Codierungsmethoden. Die Codierungsmethode, die Sie für einen Stream auswählen, hängt davon ab, wie der Stream übermittelt werden soll. In der folgenden Tabelle wird beschrieben, wann die verschiedenen Codierungsmethoden verwendet werden.



| Codiermethode                | Beschreibung                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1-Pass Constant Bit Rate (CBR) | Die einzige Option für Livestreaming. Codiert in eine vorhersagbare Bitrate und bietet die niedrigste Qualität aller Codierungsmethoden.                                                                    |
| 2-Pass-CBR                     | Wird für Dateien verwendet, die über ein Netzwerk an einen Clientleser gestreamt werden, aber nicht von einer Livequelle übertragen werden. Codiert in eine vorhersagbare Bitrate, jedoch mit einer besseren Qualität als 1-Pass-CBR. |
| Variable Bitrate mit 1 Durchgang (VBR) | Verwenden Sie , wenn Sie die Qualität der codierten Ausgabe angeben müssen. Bietet die konsistenteste Qualität aller Codierungsmethoden. Verwenden Sie nur für lokale Dateien oder zum Herunterladen.                        |
| 2-Pass-VBR – nicht trainiert     | Verwenden Sie , wenn Sie eine Bandbreite angeben müssen, aber Schwankungen um die angegebene Bandbreite sind akzeptabel. Nur für lokale Dateien oder downloads.                                                    |
| 2-Pass-VBR – eingeschränkt       | Verwenden Sie unter den gleichen Umständen wie ungeniert, aber wenn Sie eine maximale momentäre Bitrate angeben müssen. Nur für lokale Dateien oder downloads.                                                |



 

In der folgenden Tabelle sind die Codierungsmethoden aufgeführt, die von den Codecs unterstützt werden, die im Windows Media Format SDK enthalten sind.



| Codec                                  | Cbr | 2-Pass-CBR | Vbr | 2-Pass-VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media Video 9                  | X   | X          | X   | X          |
| Windows Medienaudio 9 und höher        | X   | X          | X   | X          |
| Windows Media Video 9 Screen           | X   |            | X   |            |
| Windows Media Audio 9 Voice            | X   |            |     |            |
| Windows Medienaudio Professional       | X   | X          | X   | X          |
| Windows Medienaudio verlustfrei           |     |            | X   |            |
| Windows Medienvideo 9 – Bild und höher  | X   |            | X   |            |
| Windows Media Video 9 Advanced Profile | X   | X          | X   | X          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwerfen von Profilen**](designing-profiles.md)
</dt> <dt>

[**Codierung mit konstanter Bitrate (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codierung mit zwei Durchgangen**](two-pass-encoding.md)
</dt> <dt>

[**VBR-Codierung (Variable Bit Rate)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




