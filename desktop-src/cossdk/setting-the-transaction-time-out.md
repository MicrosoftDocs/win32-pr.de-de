---
description: Sie können das Timeout für Transaktionen manuell mithilfe des Verwaltungs Tools Komponenten Dienste festlegen, oder Sie können das Timeout mithilfe der com+-Verwaltungs Schnittstellen Programm gesteuert konfigurieren.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Festlegen der Transaktions Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483782"
---
# <a name="setting-the-transaction-time-out"></a>Festlegen der Transaktions Time-Out

Sie können das Timeout für Transaktionen manuell mithilfe des Verwaltungs Tools Komponenten Dienste festlegen, oder Sie können das Timeout mithilfe der [com+-Verwaltungs Schnittstellen](com--administration-interfaces.md)Programm gesteuert konfigurieren. Das Timeout kann auf der Ebene des lokalen Computers und auch für einzelne Komponenten konfiguriert werden.

**So legen Sie das Transaktions Timeout für den lokalen Computer mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**

1.  Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf den lokalen Computer, den Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Computer Eigenschaften auf die Registerkarte **Optionen** .

3.  Geben Sie unter **Transaktions Timeout** den Transaktions Timeout in Sekunden ein. Der Standardwert für das Timeout beträgt 60 Sekunden.

4.  Klicken Sie auf **OK**.

**So legen Sie das Transaktions Timeout für eine Komponente mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**

1.  Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen** .

3.  Aktivieren Sie das Kontrollkästchen mit der Bezeichnung **globalen Transaktions Timeout Wert überschreiben**.

    > [!Note]  
    > Sie können das Kontrollkästchen nicht aktivieren, um den Timeout Wert für die globale Transaktion zu überschreiben, wenn die **Transaktionsunterstützung** auf **deaktiviert**, **nicht unterstützt** oder **unterstützt** festgelegt ist.

     

4.  Geben Sie unter **Transaktions Timeout** den Transaktions Timeout in Sekunden ein. Der Standardwert für das Timeout beträgt 0 Sekunden. Dies bedeutet, dass die Komponente niemals ein Timeout für die Transaktion verursacht.

5.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von automatischen Transaktionen in com+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



