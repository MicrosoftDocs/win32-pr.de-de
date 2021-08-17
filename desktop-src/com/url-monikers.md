---
title: URL-Moniker
description: Die OLE-Monikerarchitektur bietet ein praktisches Programmiermodell für die Arbeit mit URLs.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92e952e2d9bdd8ae70108e34845a3e920228b1b68f1db061977dff36e942254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129486"
---
# <a name="url-monikers"></a>URL-Moniker

Die OLE-Monikerarchitektur bietet ein praktisches Programmiermodell für die Arbeit mit URLs. Die Monikerarchitektur unterstützt erweiterbare und vollständige Namensparsing über die [**MkParseDisplayName-Funktion**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) und die [**Schnittstellen IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) und [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) sowie druckbare Namen über die [**IMoniker::GetDisplayName-Methode.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) Die **IMoniker-Schnittstelle** ist die Art und Weise, wie Sie URLs tatsächlich verwenden, auf die Sie stoßen, und das Erstellen von Komponenten, die in die Monikerarchitektur passen, ist die Möglichkeit, URL-Namespaces tatsächlich in der Praxis zu erweitern.

Eine vom System bereitgestellte Monikerklasse, der URL-Moniker, stellt ein Framework zum Erstellen und Verwenden bestimmter URLs zur Verfügung. Da URLs häufig Ressourcen in Netzwerken mit hoher Latenz sehen, unterstützt der URL-Moniker sowohl asynchrone als auch synchrone Bindungen. Der URL-Moniker unterstützt derzeit keinen [asynchronen Speicher.](/windows/desktop/Stg/asynchronous-storage)

Das folgende Diagramm zeigt die Komponenten, die an der Verwendung von URL-Monikern beteiligt sind. Alle diese Komponenten sollten vertraut sein. (Siehe [Asynchrone Moniker](asynchronous-monikers.md).)

![Diagramm, das die Komponenten zeigt, die an der Verwendung von U R L-Monikern beteiligt sind.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Wie alle Monikerclients erstellt und enthält ein Benutzer von URL-Monikern in der Regel einen Verweis auf den Moniker sowie auf den Bindungskontext, der während der Bindung verwendet werden soll ([**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) oder [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Zur Unterstützung der asynchronen Bindung kann der Client ein bind-status-callback-Objekt implementieren, das die [**IBindStatusCallback-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) implementiert, und es mithilfe der [**RegisterBindStatusCallback-Funktion**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) beim Bindungskontext registrieren. Dieses Objekt erhält die [**IBinding-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) des Transports bei Aufrufen von [**IBindStatusCallback::OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

Der URL-Moniker identifiziert das verwendete Protokoll durch Analyse des URL-Präfixes und ruft dann die [**IBinding-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) von der Transportebene ab. Der Client verwendet **IBinding,** um das Anhalten, Abbruch und Priorisieren des Bindungsvorgang zu unterstützen. Das Rückrufobjekt empfängt auch Statusbenachrichtigungen über [**IBindStatusCallback::OnProgress, Datenverfügbarkeitsbenachrichtigungen**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))über [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))und verschiedene andere Transportebenenbenachrichtigungen zum Status der Bindung. Der URL-Moniker oder bestimmte Transportebenen können auch erweiterte Informationen vom Client über **IBindStatusCallback::QueryInterface** anfordern, sodass der Client protokollspezifische Informationen bereitstellen kann, die sich auf den Bindungsvorgang auswirken.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Rückrufsynchronisierung](callback-synchronization.md)
-   [Medientypaushandlung](media-type-negotiation.md)
-   [URL-Monikerfunktionen](url-moniker-api-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> <dt>

[Informationen zu URL-Monikern](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 