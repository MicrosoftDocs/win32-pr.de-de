---
title: Codierung der Variablen Bitrate (VBR)
description: Codierung der Variablen Bitrate (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media-Format-SDK, VBR-Codierung
- Windows Media-Format-SDK, Variable Bitrate (VBR)
- Windows Media-Format-SDK, Qualitäts basierte VBR-Codierung
- Windows Media-Format-SDK, uneingeschränkte VBR-Codierung
- Windows Media-Format-SDK, eingeschränkte VBR-Codierung
- Codecs, VBR-Codierung
- Codecs, Variable Bitrate (VBR)
- Codecs, Qualitäts basierte VBR-Codierung
- Codecs, nicht eingeschränkte VBR-Codierung
- Codecs, eingeschränkte VBR-Codierung
- Variable Bitrate (VBR), Informationen zu
- VBR (Variable Bitrate), Informationen zu
- Qualitäts basierte VBR-Codierung, Informationen zu
- nicht eingeschränkte VBR-Codierung, Informationen zu
- eingeschränkte VBR-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341680"
---
# <a name="variable-bit-rate-vbr-encoding"></a>Codierung der Variablen Bitrate (VBR)

Die VBR-Codierung (Variable Bitrate) ist eine Alternative zur konstanten Bitrate-Codierung (CBR) und wird von einigen Codecs unterstützt. Wenn die CBR-Codierung die Bitrate der codierten Medien beibehalten soll, strebt VBR die bestmögliche Qualität der codierten Medien an.

Die Qualität der codierten Inhalte hängt von der Menge der Daten ab, die bei der Komprimierung/Dekomprimierung der Inhalte verloren geht. Der Datenverlust bei der Komprimierung hängt von vielen Faktoren ab. Im Allgemeinen gehen jedoch umso mehr Details beim Komprimierungsprozess verloren, je komplexer die Ausgangsdaten und je höher die Komprimierungsrate ist.

Es gibt drei Arten von VBR-Codierung: Qualitäts basiert, nicht eingeschränkt und eingeschränkt.

## <a name="quality-based-vbr-encoding"></a>Qualitäts basierte VBR-Codierung

Der erste Typ der VBR-Codierung ist Qualitäts basiert und verwendet einen Codierungs Durchlauf. Bei der Qualitäts basierten VBR-Codierung können Sie eine Qualitätsstufe für einen digitalen Mediendaten Strom anstelle einer Bitrate angeben. Der Codec codiert dann den Inhalt, sodass alle Beispiele eine vergleichbare Qualität haben.

Der Hauptvorteil der Qualitäts basierten VBR-Codierung besteht darin, dass die Qualität innerhalb einer Datei und von einer Datei zur nächsten konsistent ist. Beispielsweise können Sie ein Programm zum Kopieren von Liedern von CD in ASF-Dateien auf einem Computer schreiben. In diesem Fall ist die konsistente Qualität wahrscheinlich wichtiger für die Endbenutzer Leistung als die konsistente Dateigröße. Durch die Verwendung der Qualitäts basierten VBR-Codierung wird sichergestellt, dass alle kopierten Lieder dieselbe Qualität aufweisen.

Der Nachteil der Qualitäts basierten VBR-Codierung besteht darin, dass es keine Möglichkeit gibt, die Größen-oder Bandbreitenanforderungen der codierten Medien vor der Codierung zu ermitteln. Dadurch können Qualitäts basierte VBR-codierte Dateien für Situationen ungeeignet werden, in denen der Arbeitsspeicher oder die Bandbreite eingeschränkt ist, z. b. Portable Media Player oder Internet Verbindungen mit geringer Bandbreite.

Im Allgemeinen eignet sich die Qualitäts basierte VBR-Codierung gut für die lokale Wiedergabe oder Netzwerkverbindungen mit hoher Bandbreite. In diesen Fällen bietet die konsistente Qualität eine bessere Benutzer Leistung.

## <a name="unconstrained-vbr-encoding"></a>Nicht eingeschränkte VBR-Codierung

Bei der uneingeschränkten VBR-Codierung werden zwei Codierungs Durchgänge verwendet. Wenn Sie die nicht eingeschränkte VBR-Codierung verwenden, geben Sie wie bei der CBR-Codierung eine Bitrate für den Datenstrom an. Der Codec verwendet diesen Wert jedoch nur als durchschnittliche Bitrate für den Stream und codiert, sodass die Qualität so hoch wie möglich ist, während der Durchschnitt beibehalten wird. Die tatsächliche Bitrate an einem beliebigen Punkt im codierten Stream kann stark vom Durchschnittswert abweichen.

Sie legen kein Puffer Fenster für die unbeschränkte VBR-Codierung fest, wie es bei einem CBR-codierten Stream der Fall wäre. Stattdessen berechnet der Codec die Größe des erforderlichen Puffer Fensters basierend auf den Anforderungen der codierten Stichproben.

Der Vorteil der uneingeschränkten VBR-Codierung besteht darin, dass der komprimierte Datenstrom die höchste mögliche Qualität aufweist und gleichzeitig in einer vorhersagbaren durchschnittlichen Bandbreite bleibt.

## <a name="constrained-vbr-encoding"></a>Eingeschränkte VBR-Codierung

Die eingeschränkte VBR-Codierung ist mit der nicht eingeschränkten VBR-Codierung identisch, mit der Ausnahme, dass Sie eine maximale Bitrate und ein maximales Puffer Fenster im Profil angeben. Der Codec verwendet dann die maximalen Werte, um zu bestimmen, wie die Daten komprimiert werden sollen. Wenn Sie die maximalen Werte hoch genug festlegen, erzeugt die eingeschränkte VBR-Codierung denselben codierten Stream wie die uneingeschränkte VBR-Codierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Auswählen einer Codierungsmethode**](choosing-an-encoding-method.md)
</dt> <dt>

[**Codec-Features**](codec-features.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Konfigurieren von VBR-Streams**](configuring-vbr-streams.md)
</dt> <dt>

[**Codierung mit konstanter Bitrate (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Zwei-Pass-Codierung**](two-pass-encoding.md)
</dt> <dt>

[**Verwenden von Two-Pass Codierung**](using-two-pass-encoding.md)
</dt> </dl>

 

 




