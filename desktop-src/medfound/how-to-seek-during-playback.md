---
description: In diesem Thema wird beschrieben, wie während der Wiedergabe mit MFPlay gesucht wird.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Suchen während der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47e035ff8cc3764a9080698e8596660ce61907319bda70ac019b4cba1f8c27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974419"
---
# <a name="how-to-seek-during-playback"></a>Suchen während der Wiedergabe

\[MFPlay ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie während der Wiedergabe mit MFPlay gesucht wird.

**So suchen Sie während der Wiedergabe**

1.  Initialisieren Sie ein **PROPVARIANT,** um die Suchzeit in Einheiten von 100 Nanosekunden als **LARGE \_ INTEGER** -Typ **(VT \_ I8)** zu speichern.
2.  Rufen Sie [**IMFPMediaPlayer::SetPosition auf.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition) Geben Sie **MFP \_ POSITIONTYPE \_ 100NS** für den ersten Parameter an, und übergeben Sie **propvariant** für den zweiten Parameter.

## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



