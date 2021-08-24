---
description: Aktivieren der JIT-Aktivierung für eine Komponente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Aktivieren der JIT-Aktivierung für eine Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beac51cd4f97a451b372d8eeee8ef419ead3140a672ca85dcdc3740d8c52de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637700"
---
# <a name="enabling-jit-activation-for-a-component"></a>Aktivieren der JIT-Aktivierung für eine Komponente

Sie sollten eine Komponente nur so konfigurieren, dass sie JIT aktiviert wird, wenn sie ordnungsgemäß geschrieben wurde, um den JIT-Aktivierungsdienst (Com+ Just-In-Time) zu unterstützen. Wenn eine Komponente zwischen Methodenaufrufen deaktiviert wird, geht der zugeordnete Zustand verloren. Angesichts des Standardverhaltens der JIT-Aktivierung ist dies unwahrscheinlich, wenn Sie dies nicht erwarten. Sie sollten jedoch die Anforderungen einer Komponente kennen, bevor Sie ihre Konfiguration ändern, und die Erwartungen der Clients kennen, die die Komponente aufrufen.

> [!Note]  
> Wenn eine Komponente so konfiguriert ist, dass Transaktionen erforderlich sind, wird der COM+-JIT-Aktivierungsdienst automatisch aktiviert. Sie können sie in diesem Fall nicht deaktivieren. Weitere Informationen finden Sie unter [Konfigurieren von Transaktionen.](configuring-transactions.md)

 

Wenn Sie die JIT-Aktivierung für eine Komponente aktivieren, wird ihr Synchronisierungsattribut für diese Komponente auf erforderlich festgelegt. In diesem Fall können Sie die Synchronisierungseinstellung nicht ändern. Weitere Informationen finden Sie unter [Synchronisierungsabhängigkeiten.](synchronization-dependencies.md)

**So aktivieren Sie die JIT-Aktivierung**

1.  Klicken Sie im Detailbereich des Component Services-Verwaltungstools mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung.**

3.  Aktivieren Sie das Kontrollkästchen **Just-In-Time-Aktivierung aktivieren,** um die JIT-Aktivierung für die Komponente zu aktivieren.

4.  Klicken Sie auf **OK**.

Wenn Sie die JIT-Aktivierung für eine Komponente aktiviert haben, haben Sie die Möglichkeit, das feature auto-done für jede Methode zu aktivieren, die von dieser Komponente verfügbar gemacht wird. Weitere Informationen finden Sie unter [Aktivieren von Auto-Done für eine Methode.](enabling-auto-done-for-a-method.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von "Auto-Done" für eine Methode](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Festlegen des Done-Bits](setting-the-done-bit.md)
</dt> </dl>

 

 



