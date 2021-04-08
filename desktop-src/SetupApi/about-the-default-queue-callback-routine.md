---
description: Die standardmäßige Warteschlangen Rückruf Routine verarbeitet von setupcommitfilequeue gesendete Benachrichtigungen auf generische Weise.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Informationen zur Standard Warteschlangen Rückruf-Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862379"
---
# <a name="about-the-default-queue-callback-routine"></a>Informationen zur Standard Warteschlangen Rückruf-Routine

Die standardmäßige Warteschlangen Rückruf Routine verarbeitet von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gesendete Benachrichtigungen auf generische Weise. Wenn Sie die Standard Routine verwenden, erhalten Sie eine vorgefertigte Benutzeroberfläche, um allgemeine Setup Dialogfelder zu erstellen. Es wird empfohlen, dass Sie die standardmäßige Warteschlangen Rückruf Routine verwenden, um die Benutzerfreundlichkeit zu vereinfachen und eine konsistente Darstellung und das Verhalten von Dialogfeldern sicherzustellen, die während der Installation generiert werden.

Die Standard Rückruf Routine erfordert eine Kontext Struktur für die interne Daten Satz Aufbewahrung. Außerdem übergibt die Warteschlange zusätzliche Informationen, die für die aktuelle Benachrichtigung relevant sind, in einer Reihe von Parametern, *param1* und *Param2*.

Wenn die Warteschlange z. b. eine spfilenotify- \_ needmedia-Benachrichtigung an die standardmäßige Rückruf Routine sendet, verweist *param1* auf eine [**Quell \_ Medien**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) Struktur, die Informationen über das benötigte Medium enthält, und *Param2* verweist auf ein Zeichen Array, das neue Pfadinformationen vom Benutzer empfangen kann.

Die Standard Rückruf Routine verwendet diese Informationen, um den Benutzer aufzufordern, entweder die erforderlichen Quell Medien einzufügen, einen neuen Pfad anzugeben, das Kopieren der aktuellen Datei zu überspringen oder den aktuellen Vorgang abzubrechen. Die Standard Warteschlangen Rückruf-Routine gibt fileOp \_ NewPath, fileOp \_ doit, fileOp \_ Skip oder fileOp \_ Abbruch an die Warteschlange zurück, abhängig von der Aktion, die der Benutzer ausgeführt hat.

Informationen dazu, wie die Standard Warteschlangen-Rückruf Routine jede Warteschlangen Benachrichtigung verarbeitet, finden Sie unter [Benachrichtigungen zu Datei Warteschlangen](file-queue-notifications.md).

Informationen zu benutzerdefinierten Warteschlangen Rückruf Routinen finden Sie unter [Erstellen einer benutzerdefinierten Warteschlangen Rückruf-Routine](creating-a-custom-queue-callback-routine.md).

 

 



