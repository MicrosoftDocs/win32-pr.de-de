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
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="55aca-103">Zeichnen auf mehreren Anzeige Monitoren</span><span class="sxs-lookup"><span data-stu-id="55aca-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="55aca-104">Das System verarbeitet das Zeichnen automatisch in einen Gerätekontext (DC), der mehr als einen Monitor umfasst, auch wenn die Monitore eine andere Farbtiefe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="55aca-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="55aca-105">Dies führt in der Regel zu guten Ergebnissen, ist aber möglicherweise nicht optimal.</span><span class="sxs-lookup"><span data-stu-id="55aca-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="55aca-106">Beispielsweise könnte ein Fenster auf zwei Monitoren mit einer sehr unterschiedlichen Farbtiefe eine schlechte Farbwiedergabe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="55aca-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="55aca-107">Außerdem haben Monitore mit der gleichen Farbtiefe möglicherweise unterschiedliche Farb Formatwerte, z. b., Farben können mit unterschiedlichen Bits-Werten codiert werden oder sich an unterschiedlichen Stellen im Farbwert eines Pixels befinden.</span><span class="sxs-lookup"><span data-stu-id="55aca-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="55aca-108">Um die besten Ergebnisse für die einzelnen Monitore in einem Domänen Controller zu erhalten, der mehr als eine Anzeige umfasst, können Sie " [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) " aufrufen, um die Monitore aufzulisten, die ihren Domänen Controller überschneiden, und den überschneidenden Bereich in jedem dieser Monitore separat entsprechend den Anzeige Attributen für diesen Monitor zeichnen.</span><span class="sxs-lookup"><span data-stu-id="55aca-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="55aca-109">Sehen Sie sich das Beispiel unterzeichnen auf einem Domänen Controller [an, der mehrere anzeigen umfasst](painting-on-a-dc-that-spans-multiple-displays.md).</span><span class="sxs-lookup"><span data-stu-id="55aca-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="55aca-110">Wenn Sie alle Ihre Zeichnung in Ihrem WM-Zeichnungs Code durchführen und der **WM \_** -Zeichnungs Code alle verschiedenen Video Modi verarbeitet, sollten Sie den **WM \_** -Zeichnungs Code in der **MonitorEnumProc** von [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) mit nur wenigen Änderungen platzieren können. **\_**</span><span class="sxs-lookup"><span data-stu-id="55aca-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



