---
description: Sie können eine Komponente so konfigurieren, dass Sie nur dann in einem Pool zusammengefasst wird, wenn Sie ordnungsgemäß geschrieben wurde Ausführliche Informationen zu diesen Anforderungen finden Sie unter Anforderungen für in einem Pool Bare Objekte.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Konfigurieren einer Komponente, die in einem Pool zusammengefasst werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127564"
---
# <a name="configuring-a-component-to-be-pooled"></a>Konfigurieren einer Komponente, die in einem Pool zusammengefasst werden soll

Sie können eine Komponente so konfigurieren, dass Sie nur dann in einem Pool zusammengefasst wird, wenn Sie ordnungsgemäß geschrieben wurde Ausführliche Informationen zu diesen Anforderungen finden Sie unter [Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md).

> [!Note]  
> Standardmäßig ist eine Komponente nicht für ein Pool konfiguriert.

 

Wenn Sie eine Komponente so konfigurieren, dass Sie in einem Pool zusammengefasst wird, können Sie die folgenden Eigenschaften angeben, um zu bestimmen, wie com+ den Pool verwaltet:

-   **Minimale Poolgröße.** Stellt die Anzahl der Objekte dar, die beim Start der Anwendung erstellt werden, und die Mindestanzahl von Objekten, die im Pool gewartet werden, während die Anwendung ausgeführt wird. Wenn die Anzahl der verfügbaren Objekte im Pool unter den angegebenen Minimalwert sinkt, werden neue Objekte erstellt, um ausstehende Objekt Anforderungen zu erfüllen und den Pool erneut auszufüllen. Wenn die Anzahl der verfügbaren Objekte im Pool größer ist als die Mindestanzahl, werden diese überzähligen Objekte während eines Bereinigungs Prozesses zerstört.
-   **Maximale Poolgröße.** Stellt die maximale Anzahl von in einem Pool zusammengefassten Objekten dar, die vom Pooling-Manager erstellt werden, der von den Clients aktiv verwendet und inaktiv im Pool verwendet wird. Beim Erstellen von Objekten prüft der Pooling Manager, ob die maximale Poolgröße nicht erreicht wurde, und wenn dies nicht der Fall ist, erstellt der Pool-Manager eine neue Instanz des Objekts, das auf den Client verzichtet. Wenn die maximale Poolgröße erreicht ist, werden Client Anforderungen in die Warteschlange eingereiht und empfangen das erste verfügbare Objekt aus dem Pool auf der Grundlage der ersten Bereitstellung. Bei Objekt Erstellungs Anforderungen wird nach einem bestimmten Zeitraum ein Timeout festgelegt.
-   **Erstellungs Timeout (MS).** Gibt an, wie lange ein Client nach einem [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)-Aufrufvorgang (in Millisekunden) darauf wartet, dass ein Objekt aus dem Pool zurückgegeben wird. Wenn der Client-Rückruf nicht erfolgreich ist, wird der Fehler E \_ Timeout zurückgegeben.

**So legen Sie Pooling-bezogene Eigenschaften fest**

1.  Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .

3.  Aktivieren Sie das Kontrollkästchen **Objekt Pooling aktivieren** , um das Objekt Pooling für die Komponente zu aktivieren.

4.  Geben Sie im Feld **minimale Poolgröße** die Mindestanzahl von Objekten dieses Typs in den Pool ein. Der Pool wird so verwaltet, dass er mindestens über diese Anzahl von Objekten verfügt.

5.  Geben Sie im Feld u die maximale Anzahl von Objekten dieses Typs in den Pool ein. Die Anzahl der aktivierten und deaktivierten Objekte überschreitet diesen Wert nie.

6.  Geben Sie im Feld **Erstellungs Timeout (MS)** die Zeitspanne in Millisekunden ein, die ein Client auf ein in einem Pool zusammen gefases Objekt wartet, wenn es nicht sofort verfügbar ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objekt Statistik überwachen](monitoring-object-statistics.md)
</dt> </dl>

 

 
