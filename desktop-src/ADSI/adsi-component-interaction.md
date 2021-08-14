---
title: ADSI-Komponenteninteraktion
description: Die Active Directory-Routerkomponente füllt eine ADSI-Anbietertabelle von den installierten ADSI-Anbietern auf, die in der Registrierung aufgeführt sind, wenn sie die erste Anforderung von der Clientanwendung empfängt.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec82573c23564c964ebe310cd7eceb917a4565ed2d6fa8aa40b4dc03d1db2d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181108"
---
# <a name="adsi-component-interaction"></a>ADSI-Komponenteninteraktion

Die Active Directory-Routerkomponente füllt eine ADSI-Anbietertabelle von den installierten ADSI-Anbietern auf, die in der Registrierung aufgeführt sind, wenn sie die erste Anforderung von der Clientanwendung empfängt. Weitere Informationen zur Registrierung finden Sie unter [Installieren der Beispielanbieterkomponente](installing-the-example-provider-component.md).

Vorgänge, die eine Anforderung von einem Verzeichnis für einen Zeiger auf eine Schnittstelle in einem Active Directory-Objekt senden, werden über eine Funktion (**GetObject** in Visual Basic oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C oder C++) oder eine Schnittstellenmethode ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)) übergeben. In der folgenden Abbildung übergibt die ADSI-Clientanwendung eine solche Bindungsanforderung an die ADSI-Routerkomponente (1). Die Routerkomponente identifiziert die ProgID für den Anbieter aus dem ersten Teil des ADsPath und verwendet [**CLSIDFromProgID,**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) um die entsprechende CLSID in der Registrierung zu finden (2) und lädt die richtige Anbieterkomponente (3).

![Adsi-Komponenteninteraktionen im Beispielanbieter](images/dscspr.png)

In der obigen Abbildung erstellt die Anbieterkomponente ein Active Directory-Objekt, das das benannte Verzeichniselement darstellt. Die ADSI-Unterstützungskomponente führt eine **QueryInterface** für den angeforderten Schnittstellenbezeichner aus. Wenn ein Zeiger auf diese Schnittstelle abgerufen wird (4), wie bei allen COM-Client-/Serverimplementierungen, wird er dann an den Client (5) übergeben, und von diesem Zeitpunkt an arbeitet die Clientanwendung direkt mit der Anbieterkomponente (6).

 

 