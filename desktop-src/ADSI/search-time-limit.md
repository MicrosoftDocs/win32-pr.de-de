---
title: Such Zeitlimit
description: Wenn Sie eine Suche auf einem Server mit hoher Arbeitsauslastung anfordern, empfiehlt es sich, den Server anzuweisen, die Suche auf ein bestimmtes Zeitlimit zu beschränken.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Such Zeit Limit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342029"
---
# <a name="search-time-limit"></a>Such Zeitlimit

Wenn Sie eine Suche auf einem Server mit hoher Arbeitsauslastung anfordern, empfiehlt es sich, den Server anzuweisen, die Suche auf ein bestimmtes Zeitlimit zu beschränken. Wenn Sie z. b. eine Anwendung ausführen möchten, um einen wöchentlichen Bericht auf einem Server zu generieren, auf dem die Kapazität fast erreicht ist, und um zu vermeiden, dass die CPU-Zeit maximiert und andere Aufträge nicht ausgeführt werden, können Sie die Suchzeit auf einen kleinen Wert festlegen und die Anwendung später erneut ausführen, wenn der Bericht nicht generiert werden kann.

Einige Server können Ihr eigenes Verwaltungszeit Limit erzwingen. Wenn Sie in diesen Fällen einen Wert für das Limit für die Suche angeben, der größer ist als das administrative Zeit Limit, ignoriert der Server Ihre Spezifikation und verwendet stattdessen die interne administrative Zeitbegrenzung.

Weitere Informationen zur Verwendung der Option für das Suchen von Zeitlimits mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Server Zeit Limit bei idirector ysearch](server-time-limit-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




