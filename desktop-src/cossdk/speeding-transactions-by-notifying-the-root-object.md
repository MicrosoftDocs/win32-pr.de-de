---
description: Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214117"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts

Um automatische Transaktionen effektiv zu verwenden, sollte jede Transaktions Komponente angeben, dass Sie Ihre Arbeit abgeschlossen hat. Wenn eine Objektinstanz die Aufgabe erfolgreich abgeschlossen hat, sollte Sie Ihre konsistenten und done-Flags auf true festlegen, indem Sie die [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) -Methode aufruft. Wenn alle inneren Objekte der Transaktion **SetComplete** aufgerufen haben, kann die Transaktion beendet werden, indem das Stamm Objekt durch Aufrufen der **SetComplete** -Methode explizit deaktiviert wird. Wenn Sie explizit angeben, dass ein Stamm Objekt seine Arbeit abgeschlossen hat, können Sie die Länge der Transaktion reduzieren.

Wenn eine transaktionale Objektmethode fehlschlägt, sollte das Objekt das konsistente Flag auf false und das done-Flag auf true festlegen, indem die [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) -Methode aufgerufen wird. Durch Aufrufen der **SetAbort** -Methode gibt ein Objekt die Steuerung an seinen Aufrufer zurück und stellt sicher, dass die Transaktion letztendlich abgebrochen wird.

Es sei denn, das Objekt, von dem [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) aufgerufen wird, ist der Stamm der Transaktion. die Transaktion wird jedoch weiterhin ausgeführt, auch wenn Sie Sie nicht speichern kann. Um die Beendigung einer fehlgeschlagenen Transaktion zu beschleunigen, können Sie einen Fehler generieren, um das Stamm Objekt darauf hinzuweisen, dass auch **SetAbort** aufgerufen wird. Zum Abschluss sollte das Stamm Objekt dann eine Fehlermeldung an den Client senden.

Obwohl es viele verschiedene Ansätze gibt, die Sie zur Behandlung von Fehlern verwenden können, sollte Ihr Ansatz die Kommunikation zwischen inneren Objekten und dem Stamm Objekt eindeutig koordinieren.

Die folgenden Visual Basic Code Fragmente zeigen einen Ansatz für die Fehlerbehandlung. Im ersten Fragment Ruft ein inneres Objekt [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)auf, löst einen Fehler aus und generiert eine Fehlermeldung wie folgt:

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

Im zweiten Fragment verarbeitet das Stamm Objekt den Fehler und übergibt die Nachricht wie folgt an den Client:

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von automatischen Transaktionen in com+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



