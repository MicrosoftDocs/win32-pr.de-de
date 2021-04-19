---
description: Sie können das Feature für automatische Ausführung für jede Methode aktivieren, die von einer Komponente verfügbar gemacht wird, für die die com+-JIT-Aktivierung aktiviert ist. Wenn die JIT-Aktivierung deaktiviert ist, ist die automatische Ausführung nicht verfügbar.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Aktivieren von "automatisch abgeschlossen" für eine Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339701"
---
# <a name="enabling-auto-done-for-a-method"></a>Aktivieren von "automatisch abgeschlossen" für eine Methode

Sie können das Feature für automatische Ausführung für jede Methode aktivieren, die von einer Komponente verfügbar gemacht wird, für die die com+-JIT-Aktivierung aktiviert ist. Wenn die JIT-Aktivierung deaktiviert ist, ist die automatische Ausführung nicht verfügbar.

Sie sollten die automatische Ausführung nur für eine Methode aktivieren, die absichtlich geschrieben wurde, um Sie zu nutzen, da dieses Feature potenziell das erwartete Verhalten der Methode ändern kann.

Wenn Sie die Option automatisch abgeschlossen aktivieren, ändern Sie das Standardverhalten der JIT-Aktivierung und der automatischen Transaktionen für diese Methode. Sie können diese Funktion verwenden, da Sie die Notwendigkeit der expliziten Deklaration von Konsistenz und Sicherheit entfernen kann. Dies kann stattdessen erfolgen, indem einfach ein HRESULT zurückgegeben wird, wenn die automatische Ausführung aktiviert ist. Wenn Sie das automatische ausführen aktivieren, weisen Sie com+ im Wesentlichen an, Folgendes durchzuführen:

-   Legen Sie das done-Bit standardmäßig für den Kontext fest, in dem das-Objekt ausgeführt wird, wenn diese Methode aufgerufen wird.
-   Überprüfen Sie das von der-Methode zurückgegebene HRESULT. Wenn Sie Erfolg oder Fehler angibt, legen Sie das Konsistenz Bit entsprechend fest. Dies kann zu einem automatischen Aufrufen von [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)führen, je nachdem, was die Methode intern tut.

**So aktivieren Sie die automatische Ausführung für eine Methode**

1.  Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Methode, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Eigenschaften der Methode auf die Registerkarte **Allgemein** .

3.  Aktivieren Sie das Kontrollkästchen **dieses Objekt automatisch deaktivieren, wenn diese Methode zurück** gegeben wird, um die automatische Durchführung zu aktivieren. Wenn das Kontrollkästchen nicht verfügbar ist, müssen Sie zunächst die JIT-Aktivierung für die Komponente aktivieren. (Ausführliche Anweisungen finden Sie unter[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md) .)

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte für die Just-in-Time-Aktivierung in com+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Festlegen des done-Bits](setting-the-done-bit.md)
</dt> </dl>

 

 



