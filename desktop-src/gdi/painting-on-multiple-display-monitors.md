---
description: Das System verarbeitet das Zeichnen automatisch in einen Gerätekontext (DC), der mehr als einen Monitor umfasst, auch wenn die Monitore eine andere Farbtiefe aufweisen.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Zeichnen auf mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754344"
---
# <a name="painting-on-multiple-display-monitors"></a>Zeichnen auf mehreren Anzeige Monitoren

Das System verarbeitet das Zeichnen automatisch in einen Gerätekontext (DC), der mehr als einen Monitor umfasst, auch wenn die Monitore eine andere Farbtiefe aufweisen. Dies führt in der Regel zu guten Ergebnissen, ist aber möglicherweise nicht optimal. Beispielsweise könnte ein Fenster auf zwei Monitoren mit einer sehr unterschiedlichen Farbtiefe eine schlechte Farbwiedergabe aufweisen. Außerdem haben Monitore mit der gleichen Farbtiefe möglicherweise unterschiedliche Farb Formatwerte, z. b., Farben können mit unterschiedlichen Bits-Werten codiert werden oder sich an unterschiedlichen Stellen im Farbwert eines Pixels befinden.

Um die besten Ergebnisse für die einzelnen Monitore in einem Domänen Controller zu erhalten, der mehr als eine Anzeige umfasst, können Sie " [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) " aufrufen, um die Monitore aufzulisten, die ihren Domänen Controller überschneiden, und den überschneidenden Bereich in jedem dieser Monitore separat entsprechend den Anzeige Attributen für diesen Monitor zeichnen. Sehen Sie sich das Beispiel unterzeichnen auf einem Domänen Controller [an, der mehrere anzeigen umfasst](painting-on-a-dc-that-spans-multiple-displays.md).

Wenn Sie alle Ihre Zeichnung in Ihrem WM-Zeichnungs Code durchführen und der **WM \_** -Zeichnungs Code alle verschiedenen Video Modi verarbeitet, sollten Sie den **WM \_** -Zeichnungs Code in der **MonitorEnumProc** von [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) mit nur wenigen Änderungen platzieren können. **\_**

 

 



