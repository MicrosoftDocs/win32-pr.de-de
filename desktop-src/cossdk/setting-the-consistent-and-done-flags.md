---
description: Festlegen der Flags "Konsistent" und "Fertig"
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Festlegen der Flags "Konsistent" und "Fertig"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518864efda3716ea9998ed306b0ca6901b70697f8cb3acabe813d3e2e3e0bcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500050"
---
# <a name="setting-the-consistent-and-done-flags"></a>Festlegen der Flags "Konsistent" und "Fertig"

Sie legen die konsistenten und fertig-Flags fest, indem Sie Methoden für die [**IObjectContext-**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) oder [**die IContextState-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) aufrufen. Die von diesen beiden Schnittstellen verwendeten Strategien unterscheiden sich erheblich. **IObjectContext** verfügt über vier Methoden, die konsistente und fertige Flags in eindeutigen Kombinationen miteinander verbinden, während **IContextState** über zwei Methoden verfügt, mit denen Sie jedes Flag unabhängig festlegen können. Die Methoden von **IObjectContext** werden auch über das [**ObjectContext-Objekt**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) verfügbar gemacht.

Für die unabhängige Steuerung jedes Flags stellt [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) eine Methode zum Festlegen des konsistenten Flags auf True oder False und eine Methode zum Festlegen des done-Flags auf True oder False zur Verfügung. Diese Methoden sind [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) bzw. [**SetDeactivateOnReturn.**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) Die **IContextState-Schnittstelle** enthält auch Methoden zum Abrufen des aktuellen Werts der einzelnen Flags.

Wenn Sie den [**SetMyTransactionVote-Methodenwert**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) auf TxCommit festlegen, überprüft COM+ das Vorhandensein einer Transaktion. Wenn COM+ keine Transaktion erkennt, wird ein Fehler generiert, den Sie in einer Protokolldatei erfassen können. Angenommen, eine Person konfiguriert versehentlich das Transaktionsattribut Ihrer Komponente auf Nicht unterstützt, aber Sie haben erwartet, dass es auf Erforderlich festgelegt ist. Durch Festlegen **von SetMyTransactionVote** = TxCommit können Sie den Konflikt identifizieren und Maßnahmen ergreifen.

In der folgenden Tabelle werden die Methodenaufrufe beschrieben, die zum Festlegen der konsistenten und fertig-Flags verwendet werden können.



| Konsistentes Flag  | Flag "Fertig"        | IObjectContext-Methode                                            | IContextState-Methoden                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| True<br/>  | False<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/> |
| False<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True              |



 

> [!Note]  
> Die automatisch durchgeführte Eigenschaft, die auf Methodenebene festgelegt wird, kann sich darauf auswirken, wie die konsistenten und fertigen Flags festgelegt werden. Weitere Informationen zur automatisch durchgeführten Eigenschaft finden Sie unter [Aktivieren der](enabling-auto-done-for-a-method.md) automatischen Verarbeitung für eine Methode und Festlegen von [Done Bit](setting-the-done-bit.md).

 

 

 




