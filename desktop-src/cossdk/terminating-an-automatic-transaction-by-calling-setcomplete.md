---
description: Beenden einer automatischen Transaktion durch Aufrufen von SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Beenden einer automatischen Transaktion durch Aufrufen von SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d84d18b45309d750864d514728b8e23a3326e5edeba0bf144105bcbaa4797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499660"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Beenden einer automatischen Transaktion durch Aufrufen von SetComplete

Um automatische Transaktionen effektiv zu verwenden, sollte jede Transaktionskomponente angeben, dass sie ihre Arbeit abgeschlossen hat. Wenn eine Objektinstanz ihre Aufgabe erfolgreich abgeschlossen hat, sollte sie ihre konsistenten und abgeschlossenen Flags auf True festlegen, indem sie die [**IObjectContext::SetComplete-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) aufruft, die sowohl über die [**IObjectContext-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) als auch über das [**ObjectContext-Objekt**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) verfügbar gemacht wird.

Die effizienteste Möglichkeit zum Abschließen einer automatischen Transaktion besteht darin, das Stammobjekt explizit mithilfe der [**SetComplete-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) zu deaktivieren. Indem Sie explizit angeben, dass ein Stammobjekt seine Arbeit abgeschlossen hat, können Sie die Länge der Transaktion reduzieren.

Das folgende Visual Basic Beispiel zeigt, wie Sie angeben, dass ein Transaktionsobjekt seine Arbeit erfolgreich abgeschlossen hat:


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

[Konsistente und fertige Flags](consistent-and-done-flags.md)
</dt> <dt>

[Verwalten automatischer Transaktionen in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



