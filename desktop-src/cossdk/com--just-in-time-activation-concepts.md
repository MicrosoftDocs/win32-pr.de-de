---
description: Der Just-in-time (JIT)-Aktivierungs Dienst ermöglicht com+, ein Objekt zu deaktivieren, während ein Client weiterhin einen aktiven Verweis auf das Objekt enthält.
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: Konzepte für die Just-in-Time-Aktivierung in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344597"
---
# <a name="com-just-in-time-activation-concepts"></a>Konzepte für die Just-in-Time-Aktivierung in com+

Der Just-in-time (JIT)-Aktivierungs Dienst ermöglicht com+, ein Objekt zu deaktivieren, während ein Client weiterhin einen aktiven Verweis auf das Objekt enthält. Wenn der Client das nächste Mal eine Methode für das Objekt aufruft, die für den Client weiterhin aktiv sein soll, wird das Objekt vom com+-JIT-Aktivierungs Dienst auf dem Client, Just-in-Time, erneut transparent auf dem Client aktiviert.

Der Hauptvorteil bei der Verwendung der com + JIT-Aktivierung besteht darin, dass Sie es Clients ermöglichen können, Verweise auf Objekte so lange zu speichern, wie Sie Sie benötigen, ohne notwendigerweise wertvolle Server Ressourcen wie z. b. Arbeitsspeicher zu binden. Weitere wichtige Vorteile sind folgende:

-   Durch die Verwendung des com+-JIT-Aktivierungs Dienstanbieter wird das Programmiermodell für den Client erheblich vereinfacht, da der Client nicht mehr über die Verwendung kostspieliger Server Objekte und Server Ressourcen nachzudenken. Ohne die JIT-Aktivierung können Clients einen erheblichen Nachteil verursachen, wenn Sie häufig-Objekte aufzurufen und freigeben müssen.
    > [!Note]  
    > Sie können diesen Leistungsvorteil weiter verfeinern, indem Sie den [com+-objektpoolingdienst](com--object-pooling.md) verwenden. Durch das Pooling von JIT-aktivierten Objekten können Sie die Objekt Reaktivierung für Clients erheblich beschleunigen, während Sie die Ressourcen wieder verwenden, die Sie möglicherweise aufrechterhalten. so können Sie genau steuern, wie viel Arbeitsspeicher von einem bestimmten Objekt auf dem Server verwendet wird. Weitere Details finden Sie unter [Object Pooling und com+ JIT Activation](object-pooling-and-com--jit-activation.md).

     

-   Bei verteilten Anwendungen ist ein kostspieliger Netzwerkroundtrip erforderlich, um jedes Objekt zu erstellen, und je weiter der Client vom Server entfernt wird, desto höher sind die Kosten für das Aktivieren und Marshalling des Server Objekts, das Öffnen des Kanals und das Einrichten des Proxys und Stubs. Mit dem com+-JIT-Aktivierungs Dienst können Sie die Häufigkeit der Objekt Erstellung minimieren, um die Leistung Ihrer Anwendung erheblich zu verbessern.
-   Wenn Sie die com+-JIT-Aktivierung verwenden, um die Objekte zu aktivieren, auf denen Clients langlebige Verweise enthalten, die jedoch nicht zwangsläufig immer verwendet werden, ist der Server Arbeitsspeicher nicht immer gebunden, damit diese Objekte aktiv bleiben. Dies kann die Skalierbarkeit Ihrer Anwendung erheblich erhöhen. Der einzige Leistungs Treffer, den Clients sehen, ist die Zeit, die com+ benötigt, um das Objekt zu reaktivieren, normalerweise nur geringfügig länger, als es benötigt, um Speicherplatz für das Objekt zuzuweisen, und wesentlich kleiner als die Netzwerkroundtrips für die Remote Objekt Erstellung.

## <a name="enabling-com-jit-activation"></a>Aktivieren der com+-JIT-Aktivierung

Sie können den com+-JIT-Aktivierungs Dienst für eine Komponente aktivieren, indem Sie entweder das Verwaltungs Programmkomponenten Dienste oder die Verwaltungsfunktionen verwenden. Weitere Informationen hierzu finden Sie unter [Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md).

Die com+-JIT-Aktivierung kann mit anderen COM+-Diensten interagieren, z. b. wie folgt:

-   Wenn für Ihre Komponente Transaktionen erforderlich sind, ist die JIT-Aktivierung automatisch aktiviert. Ausführlichere Informationen finden [Sie unter Transaktionen und com+-JIT-Aktivierung](transactions-and-com--jit-activation.md).
-   Wenn die Komponente für die JIT-Aktivierung aktiviert ist, wird die Synchronisierung automatisch auf Required festgelegt. Dies bedeutet Folgendes: Wenn zwei Clients gleichzeitig eine JIT-aktivierte Komponente aufzurufen und ein Methodenaufrufe für eine von Ihnen zurückgibt, wodurch das Objekt deaktiviert wird, bleibt das andere nicht gestrandet.

## <a name="how-deactivation-is-triggered"></a>Auslösen der decoaktivierung

Com+ deaktiviert ein Objekt basierend auf dem Status des doneness-Bits im Objekt Kontext. Das-Objekt kann dieses Bit verwenden, um zu signalisieren, ob es abgeschlossen ist – d. h., es kann während eines bestimmten Methoden Aufrufes deaktiviert werden –. Weitere Informationen finden Sie unter [Festlegen des done-Bits](setting-the-done-bit.md).

## <a name="using-the-auto-done-property"></a>Verwenden der Auto-done-Eigenschaft

Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie eine Methode so konfigurieren, dass das Objekt bei der Rückgabe der Methode automatisch deaktiviert wird. (Informationen zum Festlegen dieser Eigenschaft finden Sie unter [Aktivieren der automatischen Ausführung für eine Methode](enabling-auto-done-for-a-method.md) .) Wenn Sie diese Option auswählen, können Sie die sich wiederholenden Methodenaufrufe für die Abstimmung in Transaktionen vermeiden. Da die Standardeinstellung für das Konsistenz Bit true ist, wenn Sie das done-Bit ebenfalls in true geändert haben und keine Aktion zum Ändern dieser Einstellungen durchführen, wird [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) automatisch aufgerufen, nachdem die-Methode zurückgegeben wurde.

Es gibt jedoch einen Nachteil für dieses Verhalten: com+ prüft das HRESULT, das von der Methode zurückgegeben wird. Wenn dieses HRESULT einen Fehler anzeigt, wird das Konsistenz Bit auf false festgelegt, und das Ergebnis ist das gleiche wie, wenn Sie [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)aufgerufen hätten.

Zusammenfassend gilt: Wenn Sie für eine Methode "automatisch abgeschlossen" auswählen und keine Aktion zum Festlegen von Bits ausführen und ein HRESULT (HR) zurückgegeben wird, gilt Folgendes:

-   Wenn erfolgreich (HR) ist, ist es so, als ob Sie [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)aufgerufen haben.
-   Wenn ein Fehler aufgetreten ist, ist dies so [**, als ob**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)Sie "" "" "" "

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a>Verwenden von IObjectControl zum Verwalten der Objekt Aktivierung und-Aktivierung

Sie können die [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) -Schnittstelle implementieren, sodass die com+-Laufzeit die Aktivierung und erneute Aktivierung der Objekte automatisch verwaltet. Wenn ein Objekt diese Schnittstelle implementiert, ruft com+ [**IObjectControl::D ereaktivierung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) auf, wenn das Objekt deaktiviert wird, und [**IObjectControl:: Aktivierung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) , wenn es reaktiviert wird. Diese Methoden ermöglichen die automatische kontextinitialisierung bei der Objekt Aktivierung und beim Bereinigung des Zustands bei der Deaktivierung.

Wenn Sie Objekte mit der com+-JIT-Aktivierung bündeln, wird dringend empfohlen, [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)zu implementieren. Weitere Details finden Sie unter [Object Pooling und com+ JIT Activation](object-pooling-and-com--jit-activation.md).

## <a name="statelessness-and-jit-activation"></a>Status losigkeit und JIT-Aktivierung

Transaktionale Objekte sind notwendigerweise zustandslos, da Sie den Zustand nicht über eine Transaktionsgrenze hinweg freigeben können. Daher verwenden Sie die JIT-Aktivierung nur dann, wenn das Objekt keinen Zustand enthält, der bei der Aktivierung verloren gehen würde. andernfalls verstoßen Sie gegen die Isolation der Transaktionen. Aufgrund der natürlichen Verwendungs Muster von transaktionalen Objekten – Sie führen einige Arbeitseinheiten aus und geben das Objekt frei, wenn die Transaktion ein Commit oder abbricht – JIT-Aktivierung und automatische Transaktionen sind eng miteinander verknüpft. Durch das Konfigurieren eines Objekts, das Transaktionen erfordert, wird die com+-JIT-Aktivierung automatisch

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Just-in-Time-Aktivierungs Tasks](com--just-in-time-activation-tasks.md)
</dt> <dt>

[Objekt Pooling und com+-JIT-Aktivierung](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transaktionen und com+-JIT-Aktivierung](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



