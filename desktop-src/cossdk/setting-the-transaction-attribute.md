---
description: Transaktions Attribute können manuell mithilfe des Verwaltungs Tools Komponenten Dienste festgelegt werden, oder Sie können beim Schreiben der Komponente programmgesteuerte Unterstützung für Transaktionen hinzufügen.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Festlegen des Transaktions Attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127393"
---
# <a name="setting-the-transaction-attribute"></a>Festlegen des Transaktions Attributs

Transaktions Attribute können manuell mithilfe des Verwaltungs Tools Komponenten Dienste festgelegt werden, oder Sie können beim Schreiben der Komponente programmgesteuerte Unterstützung für Transaktionen hinzufügen.

Weitere Informationen zu Transaktions Attributwerten finden Sie unter [Konfigurieren von Transaktionen](configuring-transactions.md).

**So legen Sie den Attribut Wert mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**

1.  Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen** .

3.  Wählen Sie unter **Transaktionsunterstützung** die Option für den gewünschten Wert aus. Der Standardwert für alle Komponenten wird **nicht unterstützt**.

4.  Klicken Sie auf **OK**.

Sie müssen dieses Verfahren für jede Komponente wiederholen.

## <a name="to-set-the-attribute-value-programmatically"></a>So legen Sie den Attribut Wert Programm gesteuert fest

Programmierer, die Microsoft Visual Basic verwenden, können das Transaction-Attribut mit **mtstransaktionmode** festlegen, einer Klassenmodul Eigenschaft für ActiveX-DLL-Projekte. Visual Basic ordnet die Auswahl dem entsprechenden com+-Transaktions Attribut Wert zu und veröffentlicht den Wert in der Typbibliothek der Komponente.

In der folgenden Tabelle wird jeder **mtstransaktionmode** -Konstante Wert dem entsprechenden com+-Transaktionswert zugeordnet.



| Mtstransaktionmode-Konstante         | Com+-Transaktionswert             |
|-------------------------------------|------------------------------------|
| Notanmtsobject (Standard)<br/> | Disabled<br/>                |
| Notransactions<br/>           | Nicht unterstützt (Standard)<br/> |
| "Requirements stransaction" <br/>     | Erforderlich<br/>                |
| Usestransaction <br/>         | Unterstützt<br/>               |
| Requirements-newtransaction <br/>  | Requires New<br/>            |



 

Der Zugriff auf die **mtstransaktionmode** -Eigenschaft kann auch Programm gesteuert mithilfe der com+-Verwaltungs Bibliothek-API erfolgen.

 

 




