---
title: Anfordern von Zeitformaten
description: Anfordern von Zeitformaten
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- Digital Instrumentation Digital Interface (MIDI), Zeitformate
- MIDI (Digital Interface Digital Interface), Zeitformate
- MIDI-Dienste, Zeitformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724808"
---
# <a name="requesting-time-formats"></a>Anfordern von Zeitformaten

Windows verwendet die [**mmtime**](/previous-versions//dd757347(v=vs.85)) -Struktur, um die Zeit in einem oder mehreren unterschiedlichen Formaten darzustellen, einschließlich der Millisekunden, Samples, SMPTE und der Formatvorlagen-Formatvorlagen. Der **wType** -Member gibt das Zeitformat an.

Die [**midistreamposition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) -Funktion verwendet die **mmtime** -Struktur. Bevor Sie diese Funktion aufrufen, müssen Sie das **wType** -Element festlegen, um das angeforderte Zeitformat anzugeben. Um festzustellen, ob das angeforderte Zeitformat unterstützt wird, überprüfen Sie **wType** nach dem Aufruf. Wenn das angeforderte Zeitformat nicht unterstützt wird, wird die Uhrzeit in einem vom Gerätetreiber ausgewählten Alternativen Zeitformat angegeben, und das **wType** -Element wird so geändert, dass das ausgewählte Zeitformat angegeben wird.

Weitere Informationen zur **mmtime** -Struktur finden Sie unter [Multimedia-Timer](multimedia-timers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDI-Dienste](midi-services.md)
</dt> </dl>

 

 