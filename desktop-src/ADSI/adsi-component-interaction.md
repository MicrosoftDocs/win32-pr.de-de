---
title: ADSI-Komponenten Interaktion
description: Die Active Directory Routerkomponente füllt eine ADSI-Anbieter Tabelle aus den installierten ADSI-Anbietern auf, die in der Registrierung aufgeführt sind, wenn Sie die erste Anforderung von der Client Anwendung empfängt.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730208"
---
# <a name="adsi-component-interaction"></a>ADSI-Komponenten Interaktion

Die Active Directory Routerkomponente füllt eine ADSI-Anbieter Tabelle aus den installierten ADSI-Anbietern auf, die in der Registrierung aufgeführt sind, wenn Sie die erste Anforderung von der Client Anwendung empfängt. Weitere Informationen zur Registrierung finden Sie unter [Installieren der Beispiel Anbieter Komponente](installing-the-example-provider-component.md).

Vorgänge, die eine Anforderung von einem Verzeichnis für einen Zeiger auf eine Schnittstelle in einem Active Directory Objekt vornehmen, werden über eine Funktion (**GetObject** in Visual Basic oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C oder C++) oder eine Schnittstellen Methode ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)) durchlaufen. In der folgenden Abbildung übergibt die ADSI-Client Anwendung eine solche Bindungs Anforderung an die ADSI-Routerkomponente (1). Die Routerkomponente identifiziert die ProgID für den Anbieter aus dem ersten Teil des ADsPath und verwendet [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) zum Suchen der passenden CLSID in der Registrierung (2) und lädt die entsprechende Anbieter Komponente (3).

![Interaktionen von ADSI-Komponenten im Beispiel Anbieter](images/dscspr.png)

In der obigen Abbildung erstellt die Anbieter Komponente ein Active Directory Objekt, das das benannte Verzeichnis Element darstellt. Die ADSI-Unterstützungs Komponente führt eine **QueryInterface-Schnittstelle** für den angeforderten Schnittstellen Bezeichner aus. Wenn ein Zeiger auf diese Schnittstelle abgerufen wird (4), wie bei allen com-Client-/Server-Implementierungen, wird Sie an den Client zurückgegeben (5), und von dann aus wird die Client Anwendung direkt mit der Anbieter Komponente (6) ausgeführt.

 

 