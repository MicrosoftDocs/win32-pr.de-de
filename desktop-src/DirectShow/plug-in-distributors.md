---
description: Plug-In-Verteiler
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Plug-In-Verteiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70d253066fdde4f082a964c56a221331cfd127c0984db2a7b1933a0bb352425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583660"
---
# <a name="plug-in-distributors"></a>Plug-In-Verteiler

Plug-In-Verteiler (PIDs) sind eine Möglichkeit, die Funktionalität des Filtergraph-Managers zu erweitern. Ein Plug-In-Verteiler ist ein COM-Objekt, das der Filtergraph-Manager zur Laufzeit aggregiert. Anwendungen erhalten über den Filtergraph-Manager Zugriff auf die PID.

Wenn der Filtergraph-Manager nach einer Schnittstelle abgefragt wird, die er nicht unterstützt, durchsucht er die Registrierung nach einem Schlüssel in der folgenden Form:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` ist eine Zeichenfolge, die den Schnittstellenbezeichner enthält. Wenn der Registrierungseintrag vorhanden ist, definiert der Wert des Eintrags den Klassenbezeichner (CLSID) einer PID, die die Schnittstelle unterstützt. Der Filtergraph-Manager aggregiert die PID und gibt einen Schnittstellenzeiger zurück, der als **äußerer IUnknown** für die PID fungiert. Wenn die Anwendung Methoden für die Schnittstelle aufruft, werden sie tatsächlich auf der PID aufgerufen. Das Vorhandensein der PID ist für die Anwendung jedoch transparent.

Der Begriff *Verteiler* stammt aus der Tatsache, dass eine PID ihren **äußeren IUnknown-Zeiger** nach Schnittstellen im Filtergraph-Manager abfragen kann. Durch Aufrufen der [**IFilterGraph::EnumFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) kann die PID die Filter im Diagramm aufzählen und Methodenaufrufe an diese Filter verteilen. Auf diese Weise kann eine PID als einzelner Steuerungspunkt für die Anwendung dienen, um Methoden für Filter aufzurufen.

Wenn der Filtergraph-Manager eine PID aggregiert, fragt er die PID nach der [**IDistributorNotify-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) ab. Wenn die PID diese Schnittstelle unterstützt, verwendet der Filtergraph-Manager sie, um die PID über Änderungen im Diagramm zu benachrichtigen:

-   Wenn das Filterdiagramm zwischen ausführungs-, angehaltenen und beendeten Zuständen wechselt, ruft es [**IDistributorNotify::Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)oder [**IDistributorNotify::Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop)auf.
-   Wenn eine Verweisuhr festgelegt ist, ruft der Filtergraph-Manager [**IDistributorNotify::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource)auf.
-   Wenn Filter hinzugefügt oder entfernt oder Stecknadelverbindungen geändert werden, ruft der Filtergraph-Manager [**IDistributorNotify::NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange)auf.

Um eine benutzerdefinierte PID zu implementieren, erstellen Sie ein COM-Objekt, das Aggregation unterstützt. Sie muss eine Schnittstelle unterstützen, die der Filtergraph-Manager nicht bereits unterstützt. Optional kann die **IDistributorNotify-Schnittstelle** unterstützt werden.

Wenn die PID Schnittstellenzeiger vom Filtergraph-Manager erhält, sollte sie sofort losgelassen werden. Andernfalls wird möglicherweise ein Zirkelverweiszähler erstellt, der verhindern kann, dass der Filtergraph-Manager zerstört wird. Das Halten eines Verweiszählers auf dem Filterdiagramm-Manager ist in jedem Fall nicht erforderlich, da der Filtergraph-Manager die Lebensdauer der PID steuert.

Da eine PID speziell für die Aggregation durch den Filtergraph-Manager entwickelt wurde, sollten Sie dies in der Konstruktormethode der PID erzwingen. Überprüfen Sie, ob der äußere **IUnknown-Zeiger** **NULL** ist, und geben Sie in diesem Falle den Fehlercode VFW \_ E NEED OWNER \_ \_ zurück. (Siehe [Fehler- und Erfolgscodes.)](error-and-success-codes.md) Außerdem können Sie den **äußeren IUnknown-Zeiger** für die [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) abfragen, um zu verhindern, dass andere Objekte die PID aggregieren. Gibt einen Fehlercode zurück, wenn das Objekt **IGraphBuilder** nicht verfügbar macht.

 

 



