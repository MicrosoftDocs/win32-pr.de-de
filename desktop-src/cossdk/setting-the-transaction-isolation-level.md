---
description: Sie können die Transaktionsisolationsstufe von Komponenten manuell festlegen, indem Sie das Verwaltungstool Komponentendienste verwenden, oder Sie können die Transaktionsisolationsstufe für eine Komponente programmgesteuert konfigurieren, indem Sie die COM+-Verwaltungsschnittstellen verwenden.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Festlegen der Transaktionsisolationsstufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96af7017f8a46f11428bfacf7282a7d4ae61b4dc3c1fd5bb7e82588f8fff6110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029460"
---
# <a name="setting-the-transaction-isolation-level"></a>Festlegen der Transaktionsisolationsstufe

Sie können die Transaktionsisolationsstufe von Komponenten manuell festlegen, indem Sie das Verwaltungstool komponentendienste verwenden, oder Sie können die Transaktionsisolationsstufe für eine Komponente programmgesteuert konfigurieren, indem Sie die [COM+-Verwaltungsschnittstellen verwenden.](com--administration-interfaces.md)

Weitere Informationen zu Transaktionsisolationsstufen finden Sie unter [Konfigurieren von Transaktionsisolationsstufen.](configuring-transaction-isolation-levels.md)

**So legen Sie die Transaktionsisolationsstufe mit dem Component Services-Verwaltungstool fest**

1.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die **Registerkarte** Transaktionen.

3.  Wählen **Sie unter Transaktionsisolationsstufe** im Dropdownfeld den wert aus, den Sie wünschen. Der Standardwert für alle Komponenten ist **Serialisiert.**

    > [!Note]  
    > Wenn unter **Transaktionsunterstützung** die Option Deaktiviert oder **Nicht** unterstützt ausgewählt **ist,** können Sie die Transaktionsisolationsstufe nicht festlegen.

     

4.  Klicken Sie auf **OK**.

Sie müssen dieses Verfahren für jede Komponente wiederholen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Transaktionsisolationsstufen](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



