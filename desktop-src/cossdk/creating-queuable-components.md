---
description: Eine Komponente mit mindestens einer Warteschlangenschnittstelle ist eine Warteschlangenkomponente.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Erstellen von Queuable-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ca7b4717da44145121508ed3e8b208e8401a240f1a2ceb858be299bf2b32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637840"
---
# <a name="creating-queuable-components"></a>Erstellen von Queuable-Komponenten

Eine Komponente mit mindestens einer Warteschlangenschnittstelle ist eine *Warteschlangenkomponente.* Damit eine Komponente von einer Warteschlange aufgerufen werden kann, müssen die Schnittstellen als Warteschlangenfähig gekennzeichnet sein, und die Komponente muss in einer Anwendung in der Warteschlange installiert werden. Eine Warteschlangenkomponente kann jedoch eine Komponente einer Nicht-Warteschlangenanwendung sein.

Eine Warteschlangenschnittstelle darf nur in Parametern enthalten– keine out-Parameter und keine Rückgabewerte. Diese Merkmale werden überprüft, indem die Typinformationen während der Komponenteninstallation analysiert werden. Wenn die Schnittstelle nicht in die Warteschlange gestellt werden kann, kann die Warteschlange der Anwendung, die die Komponente enthält, nicht aktiviert werden.

Um eine COM+-Schnittstelle als queuable anzugeben, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie in der Konsolenstruktur des Verwaltungstool Komponentendienste unter Komponentendienste den **Ordner COM+-Anwendungen,** der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Öffnen Sie **den Ordner Schnittstellen** der Komponente der COM+-Anwendung, die Sie in die Warteschlange stellen möchten.

3.  Klicken Sie mit der rechten Maustaste auf die Schnittstelle, die Sie als Warteschlangenfähig markieren möchten, und klicken Sie dann auf **Eigenschaften.**

4.  Wählen Sie **im Eigenschaftendialogfeld** die Registerkarte Queuing aus.

5.  Aktivieren Sie das Kontrollkästchen mit der Bezeichnung **Queued**.

    > [!Note]  
    > Wenn das **Kontrollkästchen Queued** (Warteschlange) ausgegraut ist, erfüllt die Schnittstelle die oben beschriebenen Queuable-Einschränkungen nicht.

     

6.  Klicken Sie auf **OK**.

    Eine Warteschlangenkomponente kann als solche identifiziert werden, indem das QUEUEABLE-Attributmakro zum Abschnitt Interface der IDL-Quelldatei (Interface Definition Language) für alle Schnittstellen hinzugefügt wird, die in die Warteschlange gestellt werden können.

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

[Erstellen von Komponentenwarteschlangen](creating-component-queues.md)
</dt> <dt>

[Entwickeln von Komponenten in der Warteschlange](developing-queued-components.md)
</dt> </dl>

 

 



