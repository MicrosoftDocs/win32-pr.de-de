---
description: Die Funktion "kreatetimerqueue" erstellt eine Warteschlange für Timer.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Timer-Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363498"
---
# <a name="timer-queues"></a>Timer-Warteschlangen

Die Funktion " [**kreatetimerqueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) " erstellt eine Warteschlange für Timer. Timer in dieser Warteschlange, die als *Timer-Queue-Timer* bezeichnet werden, sind Lightweight-Objekte, die es Ihnen ermöglichen, eine Rückruffunktion anzugeben, die aufgerufen wird, wenn die angegebene Fälligkeits Zeit erreicht wird. Der Warte Vorgang wird von einem Thread im [Thread Pool](../procthread/thread-pooling.md)ausgeführt.

Um der Warteschlange einen Zeitgeber hinzuzufügen, müssen Sie [**die Funktion "**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) die Funktion" "" ". Um einen Timer für Timer-Queue zu aktualisieren, nennen Sie die [**changetimerqueuetimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) -Funktion. Sie können eine Rückruffunktion angeben, die von einem Arbeits Thread aus dem Thread Pool ausgeführt wird, wenn der Zeitgeber abläuft.

Um einen ausstehenden Timer abzubrechen, rufen Sie die [**deletetimerqueuetimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) -Funktion auf. Wenn Sie mit der Warteschlange für Timer fertig sind, müssen Sie die [**deletetimerqueueex**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) -Funktion aufrufen, um die Zeit Geber Warteschlange zu löschen. Alle ausstehenden Timer in der Warteschlange werden abgebrochen und gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Timer](using-timer-queues.md)
</dt> </dl>

 

 
