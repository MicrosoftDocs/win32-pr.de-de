---
description: Eine Komponente mit mindestens einer Warteschlangen Schnittstelle ist eine in der Warteschlange befindliche Komponente.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Erstellen von Warteschlangen fähigen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393073"
---
# <a name="creating-queuable-components"></a>Erstellen von Warteschlangen fähigen Komponenten

Eine Komponente mit mindestens einer Warteschlangen Schnittstelle ist eine in der *Warteschlange befindliche Komponente*. Damit eine Komponente von einer Warteschlange aufgerufen werden kann, müssen die Schnittstellen als in die Warteschlange eingereiht werden, und die Komponente muss in einer Anwendung in der Warteschlange installiert sein. Eine in der Warteschlange befindliche Komponente kann jedoch eine Komponente einer Anwendung sein, die keine Warteschlange ist.

Eine queuable-Schnittstelle darf nur in-Parameter enthalten – keine out-Parameter und keine Rückgabewerte. Diese Eigenschaften werden durch die Analyse der Typinformationen während der Installation von Komponenten überprüft. Wenn die Schnittstelle nicht in die Warteschlange eingereiht werden kann, kann die Warteschlange der Anwendung mit der Komponente nicht aktiviert werden.

Um eine COM+-Schnittstelle als Warteschlange anzugeben, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Öffnen Sie den Ordner **Interfaces** der Komponente der com+-Anwendung, die Sie in die Warteschlange stellen möchten.

3.  Klicken Sie mit der rechten Maustaste auf die Schnittstelle, die Sie als Warteschlange markieren möchten, und klicken Sie dann auf **Eigenschaften**.

4.  Wählen Sie **im Dialog** Feldeigenschaften die Registerkarte Queue aus.

5.  Aktivieren Sie das Kontrollkästchen mit der Bezeichnung **Warteschlange**.

    > [!Note]  
    > Wenn das Kontrollkästchen in der **Warteschlange abgeblendet** ist, erfüllt die Schnittstelle nicht die oben beschriebenen Warteschlangen Einschränkungen.

     

6.  Klicken Sie auf **OK**.

    Eine in die Warteschlange einsetzbare Komponente kann als solche identifiziert werden, indem dem Schnittstellen Abschnitt der IDL-Quelldatei (Interface Definition Language) für alle Schnittstellen, die in die Warteschlange eingereiht werden können, das queuable-Attribut Makro

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten Warteschlangen erstellen](creating-component-queues.md)
</dt> <dt>

[Entwickeln von Komponenten in der Warteschlange](developing-queued-components.md)
</dt> </dl>

 

 



