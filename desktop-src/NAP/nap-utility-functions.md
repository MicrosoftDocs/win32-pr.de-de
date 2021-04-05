---
title: NAP-Hilfsprogrammfunktionen
description: Die folgenden Hilfsprogrammfunktionen unterstützen die NAP-API.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709798"
---
# <a name="nap-utility-functions"></a>NAP-Hilfsprogrammfunktionen

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die folgenden Hilfsprogrammfunktionen unterstützen die NAP-API.

Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicherzuweisung (cotaskmembelegc und CoTaskMemFree).

-   IN Parametern – zugewiesen und von Aufrufer freigegeben.
-   OUT-Parameter – vom aufgerufenen zugewiesen, freigegeben durch Aufrufer mit cotaskmem \* ()
-   IN/out-Parameter – vom Aufrufer zugeordnet, freigegeben und vom Aufrufer freigegeben, letztendlich mithilfe von cotaskmem \* ()

In den freexxx ()-Funktionen werden alle eingebetteten Zeiger ebenfalls freigegeben.

-   [**Zuordnung von Verbindungen**](allocconnections-func.md)
-   [**"Zuweisung"**](alloccountedstring-func.md)
-   [**Zuordnung von "Zuweisung"**](allocfixupinfo-func.md)
-   [**Freeconnections**](freeconnections-func.md)
-   [**Freizähltedstring**](freecountedstring-func.md)
-   [**"Freifixupinfo"**](freefixupinfo-func.md)
-   [**Freeisolationinfo**](freeisolationinfo-func.md)
-   [**Freeisolationinfoex**](freeisolationinfoex.md)
-   [**Freenapcomponentregistrationinfoarray**](freenapcomponentregistrationinfoarray-func.md)
-   [**Freumetworksoh**](freenetworksoh-func.md)
-   [**"Freiprivatedata"**](freeprivatedata-func.md)
-   [**Freesoh**](freesoh-func.md)
-   [**Freesohattributevalue**](freesohattributevalue-func.md)
-   [**Freesystemhealthagentstate**](freesystemhealthagentstate-func.md)
-   [**Initializenapagentnotifier**](initializenapagentnotifier.md)
-   [**Uninitializenapagentnotifier**](uninitializenapagentnotifier.md)

 

 




