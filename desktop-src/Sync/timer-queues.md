---
description: Die CreateTimerQueue-Funktion erstellt eine Warteschlange für Timer.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Timerwarteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16e0ae30e02ad9fbc8889c0d7b1094895ebec27c3db8b67acf509ee02e9da85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885878"
---
# <a name="timer-queues"></a>Timerwarteschlangen

Die [**CreateTimerQueue-Funktion**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) erstellt eine Warteschlange für Timer. Timer in dieser Warteschlange, die als *Timer-Warteschlangen-Timer* bezeichnet werden, sind einfache Objekte, mit denen Sie eine Rückruffunktion angeben können, die aufgerufen werden soll, wenn die angegebene zeitbasierte Zeit eintrifft. Der Wartevorgang wird von einem Thread im [Threadpool ausgeführt.](../procthread/thread-pooling.md)

Um der Warteschlange einen Timer hinzuzufügen, rufen Sie die [**CreateTimerQueueTimer-Funktion**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) auf. Um einen Timer-Queue-Timer zu aktualisieren, rufen Sie die [**ChangeTimerQueueTimer-Funktion**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) auf. Sie können eine Rückruffunktion angeben, die von einem Arbeitsthread aus dem Threadpool ausgeführt werden soll, wenn der Timer abläuft.

Um einen ausstehenden Timer abzubruchen, rufen Sie die [**DeleteTimerQueueTimer-Funktion**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) auf. Wenn Sie mit der Warteschlange von Timern fertig sind, rufen Sie die [**DeleteTimerQueueEx-Funktion**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) auf, um die Timerwarteschlange zu löschen. Alle ausstehenden Timer in der Warteschlange werden abgebrochen und gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Timerwarteschlangen](using-timer-queues.md)
</dt> </dl>

 

 
