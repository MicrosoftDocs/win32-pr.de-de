---
description: Beenden einer automatischen Transaktion durch Aufrufen von SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Beenden einer automatischen Transaktion durch Aufrufen von SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344953"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Beenden einer automatischen Transaktion durch Aufrufen von SetComplete

Um automatische Transaktionen effektiv zu verwenden, sollte jede Transaktions Komponente angeben, dass Sie Ihre Arbeit abgeschlossen hat. Wenn eine Objektinstanz die Aufgabe erfolgreich abgeschlossen hat, sollte Sie Ihre konsistenten und done-Flags auf true festlegen, indem Sie die [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) -Methode aufruft, die über die [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) -Schnittstelle und das [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) -Objekt verfügbar gemacht wird.

Die effizienteste Methode zum Ausführen einer automatischen Transaktion besteht darin, das Stamm Objekt mithilfe der [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) -Methode explizit zu deaktivieren. Wenn Sie explizit angeben, dass ein Stamm Objekt seine Arbeit abgeschlossen hat, können Sie die Länge der Transaktion reduzieren.

Im folgenden Visual Basic Beispiel wird gezeigt, wie angegeben wird, dass die Arbeit eines transaktionalen Objekts erfolgreich abgeschlossen wurde:


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konsistente und done-Flags](consistent-and-done-flags.md)
</dt> <dt>

[Verwalten von automatischen Transaktionen in com+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



