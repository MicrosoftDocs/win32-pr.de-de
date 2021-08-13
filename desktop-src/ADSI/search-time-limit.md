---
title: Suchzeitlimit
description: Wenn Sie eine Suche auf einem Server mit starker Arbeitsauslastung anfordern, sollten Sie den Server anweisen, die Suche auf ein bestimmtes Zeitlimit zu beschränken.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Suchzeitlimit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b666b41db67872cd418cca2d4ef2e3d766fbc1a1d1c1a2d9945eec7dfceb2429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690515"
---
# <a name="search-time-limit"></a>Suchzeitlimit

Wenn Sie eine Suche auf einem Server mit starker Arbeitsauslastung anfordern, sollten Sie den Server anweisen, die Suche auf ein bestimmtes Zeitlimit zu beschränken. Wenn Sie z. B. eine Anwendung ausführen möchten, um einen wöchentlichen Bericht auf einem Server zu generieren, der nahezu die Kapazität hat, und um zu vermeiden, dass die CPU-Zeit maximiert und die Ausführung anderer Aufträge verhindert wird, können Sie die Suchzeit auf einen kleinen Wert festlegen und die Anwendung später erneut ausführen, wenn der Bericht nicht generiert werden kann.

Einige Server können ihr eigenes Verwaltungszeitlimit erzwingen. Wenn Sie in diesen Fällen einen Suchzeitgrenzwert angeben, der das Verwaltungszeitlimit überschreitet, ignoriert der Server Ihre Spezifikation und verwendet stattdessen das interne Verwaltungszeitlimit.

Weitere Informationen zur Verwendung der Option "Suchzeitlimit" mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Serverzeitlimit mit IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




