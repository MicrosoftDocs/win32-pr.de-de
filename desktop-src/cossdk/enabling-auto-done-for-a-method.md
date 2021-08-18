---
description: Sie können das Feature "Automatisch fertig" für jede Methode aktivieren, die von einer Komponente verfügbar gemacht wird, für die die COM+-JIT-Aktivierung aktiviert ist. Wenn die JIT-Aktivierung deaktiviert ist, ist die automatische Aktivierung nicht verfügbar.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Aktivieren der automatischen Vorgehensweise für eine Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58eec7a7b87284145ea880338bfe61db2aa1afca06f1f83ee811e4375a1e473c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637690"
---
# <a name="enabling-auto-done-for-a-method"></a>Aktivieren der automatischen Vorgehensweise für eine Methode

Sie können das Feature "Automatisch fertig" für jede Methode aktivieren, die von einer Komponente verfügbar gemacht wird, für die die COM+-JIT-Aktivierung aktiviert ist. Wenn die JIT-Aktivierung deaktiviert ist, ist die automatische Aktivierung nicht verfügbar.

Sie sollten auto-done nur für eine Methode aktivieren, die absichtlich geschrieben wurde, um sie zu nutzen, da dieses Feature möglicherweise das erwartete Verhalten der Methode ändern kann.

Wenn Sie die automatische Aktivierung aktivieren, ändern Sie das Standardverhalten sowohl der JIT-Aktivierung als auch der automatischen Transaktionen für diese Methode. Möglicherweise möchten Sie dieses Feature verwenden, da dadurch die Notwendigkeit beseitigt werden kann, Konsistenz und Genauigkeit explizit zu deklarieren. Dies kann stattdessen erfolgen, indem einfach ein HRESULT zurückgegeben wird, wenn "Auto-Done" aktiviert ist. Wenn Sie die automatische Aktivierung aktivieren, weisen Sie COM+ im Wesentlichen an, Folgendes zu tun:

-   Legen Sie das fertige Bit für den Kontext, in dem das -Objekt ausgeführt wird, standardmäßig auf True fest, wenn diese Methode aufgerufen wird.
-   Überprüfen Sie das von der -Methode zurückgegebene HRESULT. Wenn success oder FAILURE angegeben ist, legen Sie das Konsistenzbit entsprechend fest. Dies kann zu einem automatischen Aufruf von [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)führen, je nachdem, was die Methode intern tut.

**So aktivieren Sie die automatische Vorgehensweise für eine Methode**

1.  Klicken Sie im Detailbereich des Verwaltungstool Komponentendienste mit der rechten Maustaste auf die Methode, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Methodeneigenschaften auf die **Registerkarte** Allgemein.

3.  Aktivieren Sie das Kontrollkästchen Dieses Objekt automatisch deaktivieren, wenn diese Methode zurückgegeben wird, um die automatische Aktivierung **zu** aktivieren. Wenn das Kontrollkästchen nicht verfügbar ist, müssen Sie zuerst die JIT-Aktivierung für die Komponente aktivieren. (Ausführliche Anweisungen finden Sie unter Aktivieren der[JIT-Aktivierung](enabling-jit-activation-for-a-component.md) für eine Komponente.)

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der COM+-Just-In-Time-Aktivierung](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Festlegen des done-Bit](setting-the-done-bit.md)
</dt> </dl>

 

 



