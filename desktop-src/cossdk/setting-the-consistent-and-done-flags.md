---
description: Festlegen der konsistenten und done-Flags
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Festlegen der konsistenten und done-Flags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd45d457828a222ce7f4ccbdc0080001b0f0b55f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483022"
---
# <a name="setting-the-consistent-and-done-flags"></a>Festlegen der konsistenten und done-Flags

Sie legen die konsistenten und done-Flags fest, indem Sie Methoden für die [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) -oder die [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) -Schnittstelle aufrufen. Die von diesen beiden Schnittstellen verwendeten Strategien unterscheiden sich erheblich. **IObjectContext** verfügt über vier Methoden, die die konsistenten und done-Flags in eindeutigen Kombinationen zusammenbinden, während **IContextState** über zwei Methoden verfügt, die es Ihnen ermöglichen, jedes Flag unabhängig festzulegen. Die Methoden von **IObjectContext** werden auch über das [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) -Objekt verfügbar gemacht.

Zum unabhängigen Steuern der einzelnen Flags bietet [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) eine Methode, um das konsistente Flag auf true oder false festzulegen, und eine Methode, um das done-Flag auf true oder false festzulegen. Diese Methoden sind [**setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) bzw. [**setDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn). Die **IContextState** -Schnittstelle enthält auch Methoden zum Abrufen des aktuellen Werts der einzelnen Flags.

Wenn Sie den [**setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) -Methoden Wert auf txcommit festlegen, überprüft com+, ob eine Transaktion vorhanden ist. Wenn com+ keine Transaktion erkennt, wird ein Fehler generiert, den Sie in einer Protokolldatei erfassen können. Nehmen wir beispielsweise an, dass jemand versehentlich das Transaktions Attribut Ihrer Komponente so konfiguriert, dass es nicht unterstützt wird Durch Festlegen von **setmytransaction Vote** = txcommit können Sie den Konflikt identifizieren und Maßnahmen ergreifen.

In der folgenden Tabelle werden die Methodenaufrufe beschrieben, die verwendet werden können, um die konsistenten und done-Flags festzulegen.



| Konsistentes Flag  | Done-Flag        | IObjectContext-Methode                                            | IContextState-Methoden                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Richtig<br/>  | False<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote* = txcommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren* = false<br/> |
| False<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote* = txabort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren* = false<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote* = txabort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren* = true<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote* = txcommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren* = true              |



 

> [!Note]  
> Die Auto-done-Eigenschaft, die auf Methoden Ebene festgelegt wird, kann sich darauf auswirken, wie die konsistenten und done-Flags festgelegt werden. Weitere Informationen zur Eigenschaft automatisch abgeschlossen finden Sie unter Aktivieren der [automatischen Ausführung für eine Methode](enabling-auto-done-for-a-method.md) und [Festlegen des done-Bits](setting-the-done-bit.md).

 

 

 




