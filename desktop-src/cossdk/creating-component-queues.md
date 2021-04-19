---
description: Eine Anwendung, die mindestens eine in der Warteschlange befindliche Komponente enthält, kann mithilfe des Verwaltungs Programms Komponenten Dienste als in die Warteschlange eingereiht gekennzeichnet werden.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Komponenten Warteschlangen erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343171"
---
# <a name="creating-component-queues"></a>Komponenten Warteschlangen erstellen

Eine Anwendung, die mindestens eine in der Warteschlange befindliche Komponente enthält, kann mithilfe des Verwaltungs Programms Komponenten Dienste als in die Warteschlange eingereiht gekennzeichnet werden.

Wenn eine Anwendung als in die Warteschlange eingereiht markiert ist, erstellt com+ automatisch eine Message queuingwarteschlange. Der Warteschlangen Name ist der Name der Anwendung. Wenn der Name der Warteschlange mit dem Namen einer vorhandenen Warteschlange übereinstimmt, verwendet com+ die vorhandene Warteschlange.

> [!Note]  
> Der Message Queuing *pathname* -Parameter ist eine Kombination aus Remote Server Name (RSN) und dem Namen der com+-Anwendung. Die RSN bezieht sich auf das Ziel einer Remote Aktivierung. Sie geben eine RSN während der Installation einer exportierbaren Client Anwendung auf einem Client Computer an. Bei der Installation wird die RSN verwendet, um die Aktivierung an einen angegebenen Client Computer weiterzuleiten. Weitere Informationen zu Warteschlangen Namen finden Sie in der Tabelle mit Parametern im Abschnitt "Queue Moniker Parameters" unter [using the Queue Moniker](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Führen Sie die folgenden Schritte aus, um eine COM+-Anwendung in der Warteschlange anzugeben:

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung, für die Sie eine Warteschlange erstellen möchten, und klicken Sie dann auf **Eigenschaften**.

3.  Wählen Sie **im Dialog** Feldeigenschaften die Registerkarte Queue aus.

4.  Aktivieren Sie das Kontrollkästchen mit der Bezeichnung Queue **– diese Anwendung kann durch MSMQ-Warteschlangen erreicht werden**.

    > [!Note]  
    > Wenn das Kontrollkästchen in der Warteschlange deaktiviert ist, enthält die Anwendung keine Komponenten, die in die Warteschlange **eingereiht** werden können.

     

5.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="remarks"></a>Bemerkungen

Warteschlangen, die von der com+-Verwaltungs Bibliothek oder dem Verwaltungs Programmkomponenten Dienste erstellt wurden, sind mit dem Message Queuing Transaktions Attribut markiert.

Nachdem eine in der Warteschlange befindliche Anwendung auf dem Server installiert wurde, kann Sie den Clients durch Exportieren der Anwendung und anschließendes Importieren der Anwendung auf jedem Client zur Verfügung gestellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Warteschlangen fähigen Komponenten](creating-queuable-components.md)
</dt> <dt>

[Architektur der Warteschlangen Komponenten](queued-components-architecture.md)
</dt> </dl>

 

 



