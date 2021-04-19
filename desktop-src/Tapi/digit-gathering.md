---
description: Neben der Aktivierung der Ziffern Überwachung und der Benachrichtigung über die einzelnen Ziffern kann eine Anwendung auch anfordern, dass mehrere Ziffern in einem Puffer gesammelt werden.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Ziffern Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353210"
---
# <a name="digit-gathering"></a>Ziffern Erfassung

Neben der Aktivierung der Ziffern Überwachung und der Benachrichtigung über die einzelnen Ziffern kann eine Anwendung auch anfordern, dass mehrere Ziffern in einem Puffer gesammelt werden. Nur wenn der Puffer voll ist oder eine andere Beendigungs Bedingung erfüllt ist, wird die Anwendung benachrichtigt. Die Ziffern Erfassung eignet sich für Funktionen wie z. b. die Sammlung von Kreditkartennummern. Sie wird ausgeführt, wenn eine Anwendung [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)aufruft und einen Puffer angibt, der mit Ziffern aufgefüllt werden soll. Die Ziffern Erfassung wird beendet, wenn eine der folgenden Bedingungen zutrifft:

-   Die angeforderte Anzahl von Ziffern wurde gesammelt.
-   Eine von mehreren Beendigungs Ziffern wurde erkannt. Die Beendigungs Ziffern werden für [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)angegeben, und die Beendigungs Ziffer wird ebenfalls in den Puffer eingefügt.
-   Einer von zwei Timeouts läuft ab. Bei den Timeouts handelt es sich um ein erstes stelliges Timeout, das die maximale Dauer angibt, bevor die erste Ziffer erfasst werden muss, und einen zwischen stelligen Timeout Wert, der die maximale Dauer zwischen aufeinander folgenden Ziffern angibt.
-   Die Ziffern Sammlung wird von [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) erneut mit einem anderen Satz von Parametern zum Starten einer neuen Sammlungs Anforderung oder mithilfe eines **null** stelligen Puffer Parameters abgebrochen, um den Vorgang abzubrechen.

Wenn die Ziffern Erfassung aus irgendeinem Grund beendet wird, wird eine [**Zeile \_ gatherdigits**](line-gatherdigits.md) -Nachricht an die Anwendung gesendet, die die Ziffern Erfassung angefordert hat. Für alle Anwendungen, die Besitzer des Aufrufes sind, kann jeweils nur eine Anforderung zur Erfassung eines einzelnen Ziffern aussteht.

Die Ziffern Erfassung und die Ziffern Überwachung können gleichzeitig für denselben Aufruf aktiviert werden. In diesem Fall empfängt die Anwendung eine Zeile " [**\_ monitordigits**](line-monitordigits.md) " für jede erkannte Ziffer und eine separate Zeile " \_ gatherdigits", wenn der Puffer zurückgesendet wird.

 

 



