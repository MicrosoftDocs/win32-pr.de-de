---
description: Neben der Aktivierung der Ziffernüberwachung und der Benachrichtigung über Ziffern nacheinander kann eine Anwendung auch anfordern, dass mehrere Ziffern in einem Puffer gesammelt werden.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Ziffernsammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d288bc8ba282f105ca31728e417178919b3d555e5f6728492453903f8fca157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946042"
---
# <a name="digit-gathering"></a>Ziffernsammlung

Neben der Aktivierung der Ziffernüberwachung und der Benachrichtigung über Ziffern nacheinander kann eine Anwendung auch anfordern, dass mehrere Ziffern in einem Puffer gesammelt werden. Nur wenn der Puffer voll ist oder eine andere Beendigungsbedingung erfüllt ist, wird die Anwendung benachrichtigt. Die Ziffernsammlung ist für Funktionen wie die Kreditkartennummernsammlung nützlich. Sie wird ausgeführt, wenn eine Anwendung [**lineGatherDigits aufruft**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)und einen Puffer angibt, der mit Ziffern gefüllt werden soll. Die Ziffernsammlung wird beendet, wenn eine der folgenden Bedingungen zutrifft:

-   Die angeforderte Anzahl von Ziffern wurde erfasst.
-   Eine von mehreren Beendigungsziffern wird erkannt. Die Beendigungsziffern werden für [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)angegeben, und die Beendigungsziffer wird ebenfalls im Puffer platziert.
-   Eines von zwei Timeouts läuft ab. Bei den Timeouts handelt es sich um ein Zeitlimit für die erste Ziffer, das die maximale Dauer vor der Erfassung der ersten Ziffer angibt, und ein zweistelliges Timeout, das die maximale Dauer zwischen aufeinanderfolgenden Ziffern angibt.
-   Die Ziffernsammlung wird explizit durch [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) mit einem anderen Parametersatz abgebrochen, um eine neue Sammlungsanforderung zu starten, oder mithilfe eines **NULL-Ziffernpufferparameters** zum Abbrechen.

Wenn die Ziffernsammlung aus irgendeinem Grund beendet wird, wird eine [**LINE \_ GATHERDIGITS-Nachricht**](line-gatherdigits.md) an die Anwendung gesendet, die die Ziffernsammlung angefordert hat. Bei einem Aufruf kann für alle Anwendungen, die Besitzer des Aufrufs sind, immer nur eine einstellige Sammlungsanforderung ausstehen.

Die Ziffernsammlung und Ziffernüberwachung kann bei demselben Aufruf gleichzeitig aktiviert werden. In diesem Fall empfängt die Anwendung eine [**LINE \_ MONITORDIGITS-Nachricht**](line-monitordigits.md) für jede erkannte Ziffer und eine separate LINE \_ GATHERDIGITS-Nachricht, wenn der Puffer zurückgesendet wird.

 

 



