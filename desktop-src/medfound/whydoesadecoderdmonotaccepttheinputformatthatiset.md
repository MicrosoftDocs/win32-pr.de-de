---
description: Warum akzeptiert ein Decoder das von mir festgelegte Eingabeformat nicht?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Warum akzeptiert ein Decoder das von mir festgelegte Eingabeformat nicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7299045e41c7ec6e4c4796ed77e22c4b59af1f2c63dfc8817de8a551021f29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887040"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>Warum akzeptiert ein Decoder das von mir festgelegte Eingabeformat nicht?

Es gibt viele Gründe, warum ein Decoder ein Format ablehnen kann. Die häufigste sind fehlende oder falsche Daten im erweiterten Format. Die Daten im erweiterten Format sind codecspezifische Informationen, die an die Struktur angefügt werden, die den Medientyp beschreibt.

Wenn Sie einen Ausgabetyp mithilfe eines Encoderobjekts aufzählen, wird der **pbFormat-Member** der [**DMO MEDIA \_ \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) auf eine **WAVEFORMATEX-Struktur** verweisen. An diese Struktur sind erweiterte Formatdaten angefügt, und die Größe dieser Daten wird im **WAVEFORMATEX.cbSize-Member** gespeichert. Unabhängig vom Container, der zum Speichern der komprimierten Daten verwendet wird, müssen Sie die **WAVEFORMATEX-Struktur** beibehalten und im Eingabetyp für den Decoder verwenden. Ohne die Daten im erweiterten Format kann der Decoder den Inhalt nicht dekomprimieren.

Bei Videoformaten müssen Sie die Daten im erweiterten Format manuell abrufen und an die **VIDEOINFOHEADER-Struktur** anfügen. Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 
