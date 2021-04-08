---
title: ID3-Unterstützung
description: ID3 ist eine Organisation, die einen Satz von Standards zum Einschließen von Metadaten in MP3-Audiodateien (MPEG Layer 3) definiert hat.
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media-Format-SDK, ID3-Unterstützung
- Advanced Systems Format (ASF), ID3-Unterstützung
- ASF (Advanced Systems Format), ID3-Unterstützung
- Metadaten, id3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713368"
---
# <a name="id3-support"></a>ID3-Unterstützung

ID3 ist eine Organisation, die einen Satz von Standards zum Einschließen von Metadaten in MP3-Audiodateien (MPEG Layer 3) definiert hat. Die Objekte des SDK für den Windows Media-Format bieten Unterstützung für mit ID3 kompatible Attribute. Drei verschiedene ID3-Versionen werden unterstützt: ID3v1. x, id3v 2.2 und id3v 2.3/v2, 4. Eine Liste der Attribute, die auf ID3-Frames entsprechen, finden Sie [unter Unterstützung von Unterstützung von Unterstützung](id3-tag-support.md).

Sofern nicht anders angegeben, wird von den Objekten dieses SDK keine Überprüfung von ID3-Frame-Daten durchgeführt. Das Metadatenattribut [**WM/ \_ liedsynchron**](wm-lyrics-synchronised.md) speichert z. b. die songtexte mit den entsprechenden Zeitstempeln. Wenn Sie ein **\_ synchronisiertes WM/Lied-** Attribut schreiben, werden die Objekte dieses SDK nicht überprüft, um sicherzustellen, dass die Zeitstempel in chronologischer Reihenfolge sind oder eine Überprüfung jeglicher Art ausführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**Metadatenfeatures**](metadata-features.md)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




