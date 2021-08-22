---
description: Sie können Transaktionsattribute manuell festlegen, indem Sie das Verwaltungstool Komponentendienste verwenden, oder Sie können programmgesteuerte Unterstützung für Transaktionen hinzufügen, wenn Sie Ihre Komponente schreiben.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Festlegen des Transaktionsattributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6310d2544090d4b551a93782b4756b3d89f2d6d365dfc09aec4658d5d3e1b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546217"
---
# <a name="setting-the-transaction-attribute"></a>Festlegen des Transaktionsattributs

Sie können Transaktionsattribute manuell festlegen, indem Sie das Verwaltungstool Komponentendienste verwenden, oder Sie können programmgesteuerte Unterstützung für Transaktionen hinzufügen, wenn Sie Ihre Komponente schreiben.

Weitere Informationen zu Transaktionsattributwerten finden Sie unter [Konfigurieren von Transaktionen.](configuring-transactions.md)

**So legen Sie den Attributwert mithilfe des Verwaltungstools "Komponentendienste" fest**

1.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen.**

3.  Wählen Sie unter **Transaktionsunterstützung** die Option für den gewünschten Wert aus. Der Standardwert für alle Komponenten ist **Nicht unterstützt.**

4.  Klicken Sie auf **OK**.

Sie müssen dieses Verfahren für jede Komponente wiederholen.

## <a name="to-set-the-attribute-value-programmatically"></a>So legen Sie den Attributwert programmgesteuert fest

Programmierer, die Microsoft Visual Basic verwenden, können das Transaktionsattribut mit **MTSTransactionMode** festlegen, einer Klassenmoduleigenschaft für ActiveX DLL-Projekte. Visual Basic ordnet Ihre Auswahl dem entsprechenden COM+-Transaktionsattributwert zu und veröffentlicht den Wert in der Typbibliothek Ihrer Komponente.

In der folgenden Tabelle wird jeder **KONSTANTE MTSTransactionMode-Wert** dem entsprechenden COM+-Transaktionswert zugeordnet.



| MTSTransactionMode-Konstante         | COM+-Transaktionswert             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (Standard)<br/> | Disabled<br/>                |
| NoTransactions<br/>           | Nicht unterstützt (Standard)<br/> |
| RequiresTransaction <br/>     | Erforderlich<br/>                |
| UsesTransaction <br/>         | Unterstützt<br/>               |
| RequiresNewTransaction <br/>  | Requires New<br/>            |



 

Auf die **MTSTransactionMode-Eigenschaft** kann auch programmgesteuert über die COM+-Verwaltungsbibliotheks-API zugegriffen werden.

 

 




