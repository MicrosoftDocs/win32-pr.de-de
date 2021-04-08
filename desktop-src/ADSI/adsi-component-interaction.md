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
# <a name="adsi-component-interaction"></a><span data-ttu-id="b00f6-103">ADSI-Komponenten Interaktion</span><span class="sxs-lookup"><span data-stu-id="b00f6-103">ADSI Component Interaction</span></span>

<span data-ttu-id="b00f6-104">Die Active Directory Routerkomponente füllt eine ADSI-Anbieter Tabelle aus den installierten ADSI-Anbietern auf, die in der Registrierung aufgeführt sind, wenn Sie die erste Anforderung von der Client Anwendung empfängt.</span><span class="sxs-lookup"><span data-stu-id="b00f6-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="b00f6-105">Weitere Informationen zur Registrierung finden Sie unter [Installieren der Beispiel Anbieter Komponente](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="b00f6-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="b00f6-106">Vorgänge, die eine Anforderung von einem Verzeichnis für einen Zeiger auf eine Schnittstelle in einem Active Directory Objekt vornehmen, werden über eine Funktion (**GetObject** in Visual Basic oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C oder C++) oder eine Schnittstellen Methode ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)) durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b00f6-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="b00f6-107">In der folgenden Abbildung übergibt die ADSI-Client Anwendung eine solche Bindungs Anforderung an die ADSI-Routerkomponente (1).</span><span class="sxs-lookup"><span data-stu-id="b00f6-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="b00f6-108">Die Routerkomponente identifiziert die ProgID für den Anbieter aus dem ersten Teil des ADsPath und verwendet [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) zum Suchen der passenden CLSID in der Registrierung (2) und lädt die entsprechende Anbieter Komponente (3).</span><span class="sxs-lookup"><span data-stu-id="b00f6-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![Interaktionen von ADSI-Komponenten im Beispiel Anbieter](images/dscspr.png)

<span data-ttu-id="b00f6-110">In der obigen Abbildung erstellt die Anbieter Komponente ein Active Directory Objekt, das das benannte Verzeichnis Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="b00f6-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="b00f6-111">Die ADSI-Unterstützungs Komponente führt eine **QueryInterface-Schnittstelle** für den angeforderten Schnittstellen Bezeichner aus.</span><span class="sxs-lookup"><span data-stu-id="b00f6-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="b00f6-112">Wenn ein Zeiger auf diese Schnittstelle abgerufen wird (4), wie bei allen com-Client-/Server-Implementierungen, wird Sie an den Client zurückgegeben (5), und von dann aus wird die Client Anwendung direkt mit der Anbieter Komponente (6) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b00f6-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 