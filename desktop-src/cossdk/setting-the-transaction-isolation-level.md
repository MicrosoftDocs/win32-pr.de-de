---
description: Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die Transaktions Isolationsstufe von Komponenten manuell festlegen, oder Sie können die Transaktions Isolationsstufe für eine Komponente mithilfe der com+-Verwaltungs Schnittstellen Programm gesteuert konfigurieren.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Festlegen der Transaktionsisolationsstufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748841"
---
# <a name="setting-the-transaction-isolation-level"></a>Festlegen der Transaktionsisolationsstufe

Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die Transaktions Isolationsstufe von Komponenten manuell festlegen, oder Sie können die Transaktions Isolationsstufe für eine Komponente mithilfe der [com+-Verwaltungs Schnittstellen](com--administration-interfaces.md)Programm gesteuert konfigurieren.

Weitere Informationen zu Transaktions Isolations Stufen finden Sie unter [Konfigurieren von Transaktions Isolations Stufen](configuring-transaction-isolation-levels.md).

**So legen Sie die Transaktions Isolationsstufe mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**

1.  Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen** .

3.  Wählen Sie unter **Transaktions Isolationsstufe** den gewünschten Wert aus dem Dropdown Feld aus. Der Standardwert für alle Komponenten wird **serialisiert**.

    > [!Note]  
    > Wenn unter **Transaktionsunterstützung** entweder **deaktiviert** oder **nicht unterstützt** ausgewählt ist, kann die Transaktions Isolationsstufe nicht festgelegt werden.

     

4.  Klicken Sie auf **OK**.

Sie müssen dieses Verfahren für jede Komponente wiederholen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Transaktions Isolations Stufen](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



