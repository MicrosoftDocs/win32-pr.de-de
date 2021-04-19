---
description: Warum akzeptiert ein Decoder nicht das von mir festgelegte Eingabeformat?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Warum akzeptiert ein Decoder nicht das von mir festgelegte Eingabeformat?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349136"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>Warum akzeptiert ein Decoder nicht das von mir festgelegte Eingabeformat?

Es gibt zahlreiche Gründe, warum ein Decoder ein Format ablehnen könnte. Am häufigsten werden fehlende oder falsche erweiterte Formatierungsdaten angezeigt. Bei den erweiterten Formatierungsdaten handelt es sich um Codec-spezifische Informationen, die an die Struktur angehängt werden, die den Medientyp beschreibt.

Wenn Sie einen Ausgabetyp mit einem encoderobjekt auflisten, verweist der **pbformat** -Member der [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur auf eine **WaveFormatEx** -Struktur. An diese Struktur werden erweiterte Formatierungsdaten angehängt, und die Größe dieser Daten wird im **WaveFormatEx. cbSize** -Element gespeichert. Unabhängig vom Container, der zum Speichern der komprimierten Daten verwendet wird, müssen Sie die **WaveFormatEx** -Struktur persistent speichern und im Eingabetyp für den Decoder verwenden. Ohne die erweiterten Formatierungsdaten kann der Decoder den Inhalt nicht dekomprimieren.

Bei Videoformaten müssen Sie die erweiterten Formatierungsdaten manuell abrufen und an die **videoinfoheader** -Struktur anfügen. Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 
