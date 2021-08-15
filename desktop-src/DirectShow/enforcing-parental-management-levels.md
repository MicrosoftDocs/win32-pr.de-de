---
description: Erzwingen der Verwaltungsebenen von Eltern
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Erzwingen der Verwaltungsebenen von Eltern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58bb9613af2bafb353df15bd84849724890faeb5c1191701cf2599522fd26fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819933"
---
# <a name="enforcing-parental-management-levels"></a>Erzwingen der Verwaltungsebenen von Eltern

Jedem Titel oder Teil eines Titels auf einem DVD-Video Datenträger kann eine generische Jugendverwaltungsebene (PML) von 1 bis 8 zugewiesen werden. Wenn der DVD-Navigator Inhalt liest, der über eine PML verfügt, wird davon gesprochen, dass er sich in einem *Elternblock befindet.* Ein Elternblock kann aus einem Kapitel, mehreren Kapiteln oder mehreren Titeln bestehen. Eine DVD-Anwendung, die für einen internationalen Markt vorgesehen ist, sollte ein bestimmtes Bewertungssystem nicht hart in die Logik der Elternverwaltung programmieren.

Der DVD-Navigator selbst erzwingt die PMLs nicht. Sie informiert Ihre Anwendung lediglich, wenn PML-Informationen auf dem Datenträger gefunden werden. Standardmäßig werden diese Informationen auf dem Datenträger ignoriert und der Inhalt der höchsten Ebene wiedergegeben. Um die PMLs zu erzwingen, muss Ihre Anwendung eine Form der Kennwortsteuerungslogik implementieren, die Benutzer Ebenen zuweist, den DVD-Navigator anweist, pml-Ereignisbenachrichtigungen an ihn zu senden (durch Aufrufen der [**IDvdControl2::SetOption-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) beim Start mit den Parametern DVD \_ NotifyParentalLevelChange und **TRUE),** und auf diese Ereignisse reagieren, um den Zugriff nach Bedarf zuzulassen oder zuzulassen.

Ein DVD-Titel kann über eine allgemeine PML verfügen, aber Datenträgerautoren können bestimmten Abschnitten dieses Titels höhere oder restriktivere PMLs erteilen. Diese werden als temporäre PML-Befehle bezeichnet. Diese Befehle enthalten immer zwei Verzweigungsanweisungen: eine, die befolgt werden soll, wenn der temporäre PML-Befehl von der Playeranwendung akzeptiert wird, und die andere, die befolgt werden soll, wenn der Befehl abgelehnt wird. Die Abfolge der Ereignisse sieht wie folgt aus. Der DVD-Navigator liest Videoinhalte (DVD-Titeldomäne), wenn ein temporärer PML-Befehl auf dem Datenträger auftritt. Es überprüft das interne Flag, um festzustellen, ob die Anwendung angefordert hat, über dieses Ereignis benachrichtigt zu werden. Wenn das Flag nicht festgelegt ist, wird die DVD weiterhin wiedergegeben, nachdem auf dem Datenträger der Branch "Änderung auf Elternebene abgelehnt" angegeben wurde. Wenn das Flag festgelegt ist, sendet die DVD ein EC \_ \_ DVD-EREIGNIS FÜR DIE ÄNDERUNG AUF EBENE AN die Anwendung und \_ wartet in einem \_ angehaltenen Zustand, bis sie eine Antwort erhält. Wenn Ihre Anwendung das Ereignis empfängt, verwendet sie ihre eigene Logik, um zu bestimmen, ob der Befehl akzeptiert werden soll. Anschließend ruft sie [**IDvdControl2::AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) mit dem Argument **TRUE** oder **FALSE** auf. True gibt an, dass die Wiedergabe des DVD-Navigators fortgesetzt wird, nachdem der Branch "Änderung auf Elternebene akzeptiert" auf dem Datenträger angegeben wurde. Andernfalls wird die Wiedergabe fortgesetzt, und es folgt der Verzweigung "Änderung der Elternebene abgelehnt".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



