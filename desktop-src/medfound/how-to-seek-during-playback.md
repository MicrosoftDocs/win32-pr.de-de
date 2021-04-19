---
description: In diesem Thema wird beschrieben, wie Sie während der Wiedergabe mit mfplay suchen.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Suchen während der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353161"
---
# <a name="how-to-seek-during-playback"></a>Suchen während der Wiedergabe

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Sie während der Wiedergabe mit mfplay suchen.

**So suchen Sie während der Wiedergabe**

1.  Initialisieren Sie eine **PROPVARIANT** , die die Suchzeit in 100-Nanosecond-Einheiten als **großen \_ ganzzahligen** Typ (**VT \_ I8**) enthält.
2.  [**Imfpmediaplayer:: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition)aufrufen. Geben Sie für den ersten Parameter **MFP \_ PositionType \_ 100 ns** an, und übergeben Sie das **PROPVARIANT** -Zeichen für den zweiten Parameter.

## <a name="requirements"></a>Anforderungen

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



