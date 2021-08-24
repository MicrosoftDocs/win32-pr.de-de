---
description: Eine Anwendung, die mindestens eine Warteschlangenkomponente enthält, kann mit dem Verwaltungstool für Komponentendienste als in die Warteschlange gestellt markiert werden.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Erstellen von Komponentenwarteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c44f670cea15e1cb1a4549d5c1e847956eb41d400ae01d557803dbd1ce2b439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793460"
---
# <a name="creating-component-queues"></a>Erstellen von Komponentenwarteschlangen

Eine Anwendung, die mindestens eine Warteschlangenkomponente enthält, kann mit dem Verwaltungstool für Komponentendienste als in die Warteschlange gestellt markiert werden.

Wenn eine Anwendung als in die Warteschlange gestellt markiert wird, erstellt COM+ automatisch eine Message Queuing-Warteschlange dafür. Der Warteschlangenname ist der Name der Anwendung. Wenn der Warteschlangenname dem Namen einer vorhandenen Warteschlange entspricht, verwendet COM+ die vorhandene Warteschlange.

> [!Note]  
> Der Message Queuing *PathName-Parameter* ist eine Kombination aus dem Remoteservernamen (RSN) und dem COM+-Anwendungsnamen. Die RSN bezieht sich auf das Ziel einer Remoteaktivierung. Sie geben eine RSN während der Installation einer exportierbaren Clientanwendung auf einem Clientcomputer an. Bei der Installation wird der RSN verwendet, um die Aktivierung an einen angegebenen Clientcomputer weiter zu richten. Weitere Informationen zu Warteschlangennamen finden Sie in der Tabelle der Parameter im Abschnitt "Queue Moniker Parameters" (Warteschlangenmonikerparameter) unter Using the Queue Moniker (Verwenden [des Warteschlangenmonikers).](using-the-queue-moniker.md)

 

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Um eine COM+-Anwendung als in die Warteschlange gestellt anzugeben, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie in der Konsolenstruktur des Verwaltungstool Komponentendienste unter Komponentendienste den **Ordner COM+-Anwendungen,** der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung, für die Sie eine Warteschlange erstellen möchten, und klicken Sie dann auf **Eigenschaften.**

3.  Wählen Sie **im Eigenschaftendialogfeld** die Registerkarte Queuing aus.

4.  Aktivieren Sie das Kontrollkästchen Queued ( In Warteschlange **– Diese Anwendung kann von MSMQ-Warteschlangen erreicht werden).**

    > [!Note]  
    > Wenn das **Kontrollkästchen Queued** (In Warteschlange) ausgegraut ist, enthält die Anwendung keine Warteschlangenkomponenten.

     

5.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="remarks"></a>Hinweise

Warteschlangen, die von der COM+-Verwaltungsbibliothek oder dem Komponentendienste-Verwaltungstool erstellt werden, werden mit Message Queuing Transaktionsattribut gekennzeichnet.

Nachdem eine Anwendung in der Warteschlange auf dem Server installiert wurde, kann sie clients zur Verfügung gestellt werden, indem die Anwendung exportiert und dann auf jedem Client importiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Queuable-Komponenten](creating-queuable-components.md)
</dt> <dt>

[Architektur von Warteschlangenkomponenten](queued-components-architecture.md)
</dt> </dl>

 

 



