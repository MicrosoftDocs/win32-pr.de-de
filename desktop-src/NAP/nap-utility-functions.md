---
title: NAP-Hilfsprogrammfunktionen
description: Die folgenden Hilfsprogrammfunktionen unterstützen die NAP-API.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b421069804a4047b511b775c7ffafe5b4b987eb0b0ad5105f48df0ed990e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620781"
---
# <a name="nap-utility-functions"></a>NAP-Hilfsprogrammfunktionen

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die folgenden Hilfsprogrammfunktionen unterstützen die NAP-API.

Alle com-Schnittstellen, die vom NAP-System unterstützt werden, verwenden standardmäßige COM-Speicherverwaltungsregeln und die COM-Speicherzuweisung (CoTaskMemAlloc und CoTaskMemFree).

-   IN-Parameter – zugeordnet und vom Aufrufer frei.
-   OUT-Parameter – durch den Aufrufer zugeordnet, vom Aufrufer mithilfe von CoTaskMem \* () frei
-   IN/OUT-Parameter– vom Aufrufer zugeordnet, vom Aufrufer frei und neu zugeordnet, schließlich vom Aufrufer mithilfe von CoTaskMem \* () frei

In den FreeXxx()-Funktionen werden auch alle eingebetteten Zeiger frei.

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**FreeConnections**](freeconnections-func.md)
-   [**FreeCountedString**](freecountedstring-func.md)
-   [**FreeFixupInfo**](freefixupinfo-func.md)
-   [**FreeIsolationInfo**](freeisolationinfo-func.md)
-   [**FreeIsolationInfoEx**](freeisolationinfoex.md)
-   [**FreeNapComponentRegistrationInfoArray**](freenapcomponentregistrationinfoarray-func.md)
-   [**FreeNetworkSoH**](freenetworksoh-func.md)
-   [**FreePrivateData**](freeprivatedata-func.md)
-   [**FreeSoH**](freesoh-func.md)
-   [**FreeSoHAttributeValue**](freesohattributevalue-func.md)
-   [**FreeSystemHealthAgentState**](freesystemhealthagentstate-func.md)
-   [**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
-   [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)

 

 




