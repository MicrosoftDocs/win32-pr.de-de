---
description: Nachdem sich ein Aufruf im verbundenen Zustand befindet, können Informationen darüber übertragen werden.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Generieren von Inband-Ziffern und -Tönen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f144d4bc6b6273f71da37f6b9864146465c5ca29b91018a2e2ff097f6f19b44f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424880"
---
# <a name="generating-inband-digits-and-tones"></a>Generieren von Inband-Ziffern und -Tönen

Nachdem sich ein Aufruf im *verbundenen* Zustand befindet, können Informationen darüber übertragen werden. Es werden zwei Funktionen bereitgestellt, die eine End-to-End-Inbandsignalisierung zwischen der Anwendung und den Geräten der Remotestation ermöglichen, z. B. einem Antwortcomputer. Eine Funktion ist [**lineGenerateDigits,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)die Bandziffern bei einem Anruf generiert und sie über den Sprachkanal signalisiert. Ziffern können entweder als Stimm-/Pulsesequenzen oder als MFF-Töne signalisiert werden. Die andere Funktion ist [**lineGenerateTone,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)die es der Anwendung ermöglicht, einen von einer Vielzahl von Multifrequency-Tönen inband (über den Medienstream) zu generieren. Dadurch werden Telefoniefarben wie Ringback, Signalton und Ausgelastet sowie beliebige Töne mit mehrfacher Frequenz und mehreren Tönen generiert.

Bei einem Aufruf kann jeweils nur eine Ziffer oder eine Tongenerierung ausgeführt werden. Wenn die Ziffern- oder Tongenerierung abgeschlossen ist, wird eine [**LINE \_ GENERATE-Nachricht**](line-generate.md) an die Anwendung gesendet, die die Generierung angefordert hat. Wenn mehrere Ziffern generiert werden, wird nur eine einzelne Nachricht zurückgesendet, nachdem alle Ziffern generiert wurden. Wenn [**Sie lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) oder [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) aufrufen, während die Ziffern- oder Tongenerierung ausgeführt wird, wird die derzeit ausgeführte Generierung abgebrochen und die LINE \_ GENERATE-Nachricht an die Anwendung gesendet, deren Generierung mit einer Abbruchanzeige abgebrochen wurde.

 

 



