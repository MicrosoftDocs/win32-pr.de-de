---
title: Codierung mit konstanter Bitrate (CBR)
description: Codierung mit konstanter Bitrate (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media-Format-SDK, CBR-Codierung
- Windows Media-Format-SDK, Konstante Bitrate (CBR)
- Codecs, CBR-Codierung
- Codecs, Konstante Bitrate (CBR)
- Konstante Bitrate (CBR)
- CBR (Konstante Bitrate)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388658"
---
# <a name="constant-bit-rate-cbr-encoding"></a>Codierung mit konstanter Bitrate (CBR)

Bei der Codierung mit konstanter Bitrate (CBR) handelt es sich um die Standard Codierungsmethode mit dem Windows Media-Format-SDK. Wenn Sie die CBR-Codierung verwenden, geben Sie die Zielbitrate für einen Datenstrom an, und der Codec verwendet die erforderliche Komprimierung, um dies zu erreichen.

Bei der CBR-Codierung sind die Bitrate und die Größe des codierten Streams vor der Codierung bekannt. Wenn Sie z. b. einen dreiminütigen Titel bei 32.000 Bits pro Sekunde codieren, wissen Sie, dass die Dateigröße ungefähr 704 Kilobyte beträgt (32.000 Bit/s = 180 Sekunden/8 Bits pro Byte/1.024). Sie wissen auch, dass die Bandbreite, die zum Streamen des codierten Inhalts erforderlich ist, ungefähr 32.000 Bits pro Sekunde beträgt.

Bei der Codierung mit eingeschränkter Variablen Bitrate (im folgenden Abschnitt beschrieben) können Sie auch die Bitrate vor der Codierung ermitteln. da die Rate jedoch variabel ist, kann die resultierende Datei nicht so effizient wie eine im CBR-Modus codierte Datei gestreamt werden. Mit CBR bleibt die Bitrate im Lauf der Zeit immer in der Nähe der durchschnittlichen oder Zielbitrate, und die Menge an Variation kann angegeben werden.

Der Nachteil der CBR-Codierung besteht darin, dass die Qualität des codierten Inhalts nicht konstant ist. Da es schwieriger ist, Inhalte zu komprimieren, sind Teile eines CBR-Streams von geringerer Qualität als andere. Ein typischer Film hat z. b. einige Szenen, die relativ statisch sind, und einige Szenen, die vollständig ausgeführt werden. Wenn Sie einen Film mit CBR codieren, sind die Szenen, die statisch und somit einfach zu codieren sind, von höherer Qualität als die Aktions Szenen, die eine effiziente Codierung wesentlich erschweren.

Die CBR-Codierung kann auch zu inkonsistenter Qualität von einer Datei zu einer anderen führen. Wenn Sie CBR verwenden, um mehrere Lieder verschiedener Genres mit derselben Bitrate zu codieren, werden Sie möglicherweise einen gewissen Unterschied in der Qualität feststellen.

Im Allgemeinen sind Variationen der Qualität einer CBR-Datei in niedrigeren Bitraten deutlicher ausgeprägt. Bei höheren Bitraten variiert die Qualität einer CBR-codierten Datei weiterhin, aber die Qualitätsprobleme sind für den Benutzer weniger bemerkbar. Wenn Sie die CBR-Codierung verwenden, sollten Sie die Bandbreite so hoch festlegen, dass Sie das Liefer Szenario zulässt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Auswählen einer Codierungsmethode**](choosing-an-encoding-method.md)
</dt> <dt>

[**Codec-Features**](codec-features.md)
</dt> <dt>

[**Codierung der Variablen Bitrate (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




