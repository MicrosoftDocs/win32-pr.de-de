---
description: Zusammenfassung des filterthreading
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Zusammenfassung des filterthreading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362974"
---
# <a name="summary-of-filter-threading"></a>Zusammenfassung des filterthreading

Die folgenden Methoden werden im streamingthread aufgerufen:

-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [**Imemzuordcator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

Die folgenden Methoden werden im Anwendungs Thread aufgerufen:

-   Statusänderungen: [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**imediafilter::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)End, [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).
-   Referenzuhr: [**imediafilter:: getsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).
-   PIN-Vorgänge: [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).
-   Zuordnerfunktionen: [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).
-   Leeren: [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).

Diese Liste ist nicht vollständig. Wenn Sie einen Filter implementieren, müssen Sie in Erwägung ziehen, welche Methoden den Filter Zustand ändern und welche Methoden Streamingvorgänge durchführen.

 

 



