---
description: Com+-Visual Basic Debugunterstützung im Vergleich zu MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Com+-Visual Basic Debugunterstützung im Vergleich zu MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343608"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Com+-Visual Basic Debugunterstützung im Vergleich zu MTS

Durch com+ werden mehrere Einschränkungen beim Debuggen mit Microsoft Visual Basic 6,0 und MTS entfernt oder reduziert. In der folgenden Liste werden die Änderungen zusammengefasst, die Sie mit com+ erwarten können:

-   Debuggen mehrerer Komponenten – in com+ können Sie Szenarios Debuggen, bei denen ein Client, der in einer Instanz der IDE ausgeführt wird, Aufrufe an eine beliebige Anzahl von DLLs ausführt, die in einer anderen als Projektgruppe ausgeführt werden. Die Objekte in den gruppierten DLL-Projekten können einander beliebig aufzurufen, wobei der Kontext nach Bedarf fließt. Dies funktioniert natürlich auch, wenn sich die DLLs und der Client in derselben Projektgruppe in derselben Instanz der IDE befinden.

-   Debuggrenzen bei Klassen \_ Initialisierungs-und Beendigungs \_ Ereignissen – mit com+ können Sie Code in der Klasse \_ initialisieren und \_ Beenden Ereignisse einer com+-Anwendungs Komponente einfügen, auch wenn dieser Code versucht, auf das Objekt oder das zugehörige Kontext Objekt zuzugreifen. Haltepunkte können dort festgelegt und Uhren verwendet werden. Sie können auch Breakpoints im Class-Ereignis für die \_ Beendigung festlegen.

    Obwohl Sie nicht mehr als Problem Umgehung benötigt wird, können Sie die [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) -Schnittstelle implementieren und deren Aktivierungs- [**und**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) [**Deaktivierungs**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) Methoden verwenden, wenn Sie beim Starten und Herunterfahren der Komponente Code ausführen müssen. Sie können jetzt auch Haltepunkte für die Methoden " **Deaktivieren** " oder " [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) " in den Code einfügen.

-   Überwachen von MTS-Objekten – mit com+ können Sie Überwachungen für Objektvariablen hinzufügen, die von com+ zurückgegeben werden, einschließlich Rückgabewerte der Methoden " [**saferef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)", " [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)" und " [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) ".

-   Höhere Stabilität bei Komponenten Fehlern – in com+ wird ein Komponenten Fehler nicht mehr immer beendet Visual Basic (die im selben Prozess wie die Komponente mit debuggt ausgeführt wird). Beispielsweise können Sie mit der Unterstützung für Just-in-time (JIT)-Reaktivierungs Fehler jetzt den Objekt Kontext beim Debuggen überprüfen.

-   Der Debugger kann die von com+ – freigegebenen Objekte reaktivieren, wie bei MTS, Visual Basic 6,0 COM+-Objekte reaktivieren, während Sie einen Einzelschritt über einen Client debuggen. Aufgrund der Art und Weise, wie Visual Basic 6,0 Informationen zu Objekten entdeckt, ist dies das erwartete Verhalten. Beachten Sie z. B. folgenden Code:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Wenn die obj. Die Test Methode ruft [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)auf, com+ gibt obj umgehend aus dem Arbeitsspeicher frei, aber obj wurde noch nicht auf "Nothing" festgelegt. Wenn obj. Wenn der Test zurückgegeben wird, ruft der Visual Basic Debugger [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für obj für die [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) -Schnittstelle auf. Der Kontext Wrapper, der obj zugeordnet ist, erstellt eine neue Instanz von MyApp. MyClass, um den **QueryInterface** -Aufrufe zu bedienen. Daher wird dieses nicht initialisierte Objekt im Debugger nach obj angezeigt. Der Test hat zurückgegeben. Dieses Objekt wird nur im Debugger angezeigt und wird von der nachfolgenden Anweisung entfernt, um obj auf "Nothing" festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen kompilierter Visual Basic Komponenten](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Debuggen in der Visual Basic IDE](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
