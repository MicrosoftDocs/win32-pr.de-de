---
title: URL-Moniker
description: Die OLE-monikerarchitektur bietet ein komfortables Programmiermodell zum Arbeiten mit URLs.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104218899"
---
# <a name="url-monikers"></a>URL-Moniker

Die OLE-monikerarchitektur bietet ein komfortables Programmiermodell zum Arbeiten mit URLs. Die monikerarchitektur unterstützt eine erweiterbare und umfassende Namensanalyse über die Funktion " [**mksammendisplayname**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) " sowie die Schnittstellen " [**icandisplayname**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) " und " [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) " sowie Druck Bare Namen über die [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) -Methode. Die **IMoniker** -Schnittstelle ist die Art und Weise, wie Sie URLs verwenden, die auftreten, und das Entwickeln von Komponenten, die in die monikerarchitektur passen, ist die Möglichkeit, URL-Namespaces in der Praxis zu erweitern.

Eine vom System bereitgestellte Monikerklasse, der URL-Moniker, stellt ein Framework zum entwickeln und Verwenden bestimmter URLs bereit. Da in den URLs häufig Ressourcen für Netzwerke mit hoher Latenzzeit angezeigt werden, unterstützt der URL-Moniker asynchrone und synchrone Bindungen. Der URL-Moniker unterstützt derzeit keinen [asynchronen Speicher](/windows/desktop/Stg/asynchronous-storage).

Das folgende Diagramm zeigt die Komponenten, die bei der Verwendung von URL-Monikern beteiligt sind. Alle diese Komponenten sollten vertraut sein. (Weitere Informationen finden Sie unter [asynchrone Moniker](asynchronous-monikers.md).)

![Diagramm mit den Komponenten, die bei der Verwendung von U R L-Monikern beteiligt sind.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Wie alle monikerclients erstellt ein Benutzer von URL-Monikern i. a. einen Verweis auf den Moniker sowie auf den Bindungs Kontext, der während der Bindung verwendet werden soll ([**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) oder [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Zur Unterstützung der asynchronen Bindung kann der Client ein BIND-Status-Callback-Objekt implementieren, das die [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) -Schnittstelle implementiert, und es mithilfe der [**registerbindstatuscallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) -Funktion beim Bindungs Kontext registrieren. Dieses Objekt empfängt die [**ibinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) -Schnittstelle des Transports bei Aufrufen von [**ibindstatus-Callback:: onstartbinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

Der URL-Moniker identifiziert das verwendete Protokoll, indem er das URL-Präfix verarbeitet und dann die [**ibinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) -Schnittstelle aus der Transportschicht abruft. Der Client verwendet **ibinding** , um das Anhalten, Abbrechen und Priorisierung des Bindungs Vorgangs zu unterstützen. Das Rückruf Objekt empfängt außerdem eine Status Benachrichtigung über [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), Daten Verfügbarkeits Benachrichtigung über [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))und verschiedene andere Benachrichtigungen über die Transportschicht über den Status der Bindung. Der URL-Moniker oder bestimmte Transportschichten können auch erweiterte Informationen vom Client über **ibindstatus-Callback:: QueryInterface** anfordern, sodass der Client Protokoll spezifische Informationen bereitstellen kann, die sich auf den Bindungs Vorgang auswirken.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Rückruf Synchronisierung](callback-synchronization.md)
-   [Medientyp Aushandlung](media-type-negotiation.md)
-   [URL-monikerfunktionen](url-moniker-api-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> <dt>

[Informationen über URL-Moniker](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 