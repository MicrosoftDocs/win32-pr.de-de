---
description: Aktivieren der JIT-Aktivierung für eine Komponente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Aktivieren der JIT-Aktivierung für eine Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346237"
---
# <a name="enabling-jit-activation-for-a-component"></a>Aktivieren der JIT-Aktivierung für eine Komponente

Sie sollten eine Komponente so konfigurieren, dass Sie JIT nur dann aktiviert wird, wenn Sie ordnungsgemäß für die Unterstützung des com+ Just-in-time (JIT)-Aktivierungs Dienstanbieter geschrieben wurde. Wenn eine Komponente zwischen Methoden aufrufen deaktiviert wird, verliert sie jeden zugeordneten Zustand. Aufgrund des Standard Verhaltens der JIT-Aktivierung tritt dies wahrscheinlich nicht auf, wenn Sie es nicht erwarten, aber Sie sollten die Anforderungen einer Komponente beachten, bevor Sie die Konfiguration und die Erwartungen von Clients ändern, die die Komponente aufrufen werden.

> [!Note]  
> Wenn eine Komponente so konfiguriert ist, dass Transaktionen erforderlich sind, wird der com+-JIT-Aktivierungs Dienst automatisch aktiviert. Sie können Sie in diesem Fall nicht deaktivieren. Weitere Details finden Sie unter [Konfigurieren von Transaktionen](configuring-transactions.md).

 

Wenn Sie die JIT-Aktivierung für eine Komponente aktivieren, wird das Synchronisierungs Attribut für diese Komponente auf Required festgelegt. In diesem Fall können Sie die Synchronisierungs Einstellung nicht ändern. Weitere Details finden Sie unter [Synchronisierungs Abhängigkeiten](synchronization-dependencies.md).

**So aktivieren Sie die JIT-Aktivierung**

1.  Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .

3.  Aktivieren Sie das Kontrollkästchen Just-in-Time- **Aktivierung aktivieren** , um die JIT-Aktivierung für die Komponente zu aktivieren.

4.  Klicken Sie auf **OK**.

Wenn Sie die JIT-Aktivierung für eine Komponente aktiviert haben, haben Sie die Möglichkeit, die Funktion für automatische Ausführung für jede Methode zu aktivieren, die von dieser Komponente verfügbar gemacht wird. Weitere Informationen finden Sie unter [Aktivieren der automatischen Ausführung für eine Methode](enabling-auto-done-for-a-method.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von "automatisch abgeschlossen" für eine Methode](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Festlegen des done-Bits](setting-the-done-bit.md)
</dt> </dl>

 

 



