---
description: Erzwingen von Eltern Verwaltungsebenen
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Erzwingen von Eltern Verwaltungsebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482350"
---
# <a name="enforcing-parental-management-levels"></a>Erzwingen von Eltern Verwaltungsebenen

Jedem Titel oder einem Teil eines Titels auf einer DVD-Video Platte kann eine generische Ebene für die Jugendverwaltung (PML) von 1 bis 8 zugewiesen werden. Wenn der DVD-Navigator Inhalte mit PML liest, wird er als " *Eltern Block*" bezeichnet. Ein Eltern Block besteht möglicherweise aus einem Teil eines Kapitels, mehreren Kapiteln oder mehreren Titeln. Eine DVD-Anwendung, die für einen internationalen Markt gedacht ist, sollte ein bestimmtes Bewertungssystem nicht in seine Jugend Verwaltungs Logik hart codieren.

Der DVD-Navigator selbst erzwingt nicht die PMLs. Sie informiert ihre Anwendung lediglich darüber, wenn auf dem Datenträger PML-Informationen gefunden werden. Standardmäßig werden diese Informationen auf der Festplatte ignoriert und der Inhalt der höchsten Ebene wiedergegeben. Um die PMLs zu erzwingen, muss Ihre Anwendung eine Form von Kenn Wort Steuerungslogik implementieren, die Benutzerebenen zuordnet, den DVD-Navigator anweisen, IT-PML-Ereignis Benachrichtigungen zu senden (durch Aufrufen der [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) -Methode beim Start, mit den Parametern DVD \_ notifyparamevelchange und **true**) und auf diese Ereignisse zu reagieren, um den Zugriff nach

Ein DVD-Titel kann über eine Gesamt-PML verfügen, aber von Disc-Autoren können bestimmte Abschnitte dieses Titels höher oder restriktiver PMLs zugewiesen werden. Diese werden als temporäre PML-Befehle bezeichnet. Diese Befehle enthalten immer zwei Verzweigungs Anweisungen: einen, der befolgt werden soll, wenn der temporäre PML-Befehl von der Player Anwendung akzeptiert wird, und der andere, der befolgt werden soll, wenn der Befehl abgelehnt wird. Die Abfolge der Ereignisse lautet wie folgt. Der DVD-Navigator liest Videoinhalte (DVD-Titel Domäne), wenn er auf der Festplatte auf einen temporären PML-Befehl stößt. Das interne Flag wird überprüft, um festzustellen, ob die Anwendung über dieses Ereignis benachrichtigt werden muss. Wenn das Flag nicht festgelegt ist, wird die DVD nach dem auf der Festplatte angegebenen Branch "Änderung der Änderung der vertrauenden Ebene" wieder abgespielt. Wenn das-Flag festgelegt ist, sendet die DVD ein EC \_ \_ -DVD \_ \_ -Änderungs Ereignis auf der Ebene der Anwendung und wartet in einem angehaltenen Zustand, bis eine Antwort erhalten wird. Wenn die Anwendung das Ereignis empfängt, verwendet Sie Ihre eigene Logik, um zu bestimmen, ob der Befehl akzeptiert werden soll. Anschließend wird [**IDvdControl2:: akzeptparentallevelchange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) mit dem Argument " **true** " oder " **false**" aufgerufen. Wenn der Wert **true** ist, wird die Wiedergabe des DVD-Navigators fortgesetzt Andernfalls wird die Wiedergabe fortgesetzt und die Verzweigung "abgelehnte Änderung der Jugendebene" befolgt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



