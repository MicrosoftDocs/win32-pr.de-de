---
description: Die TAPI-DLLs sind zusammen mit dem TAPI-Server (Tapisvr.exe) wichtige Abstraktionen, die Endbenutzer-oder Server Anwendungen von Dienstanbietern trennen. Eine TAPI-dll in Verbindung mit dem TAPI-Server stellt eine konsistente Schnittstelle zwischen diesen beiden Ebenen bereit.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563736"
---
# <a name="tapi-dll"></a>TAPI-dll

Die TAPI-DLLs sind zusammen mit dem TAPI-Server (Tapisvr.exe) wichtige Abstraktionen, die Endbenutzer-oder Server Anwendungen von Dienstanbietern trennen. Eine TAPI-dll in Verbindung mit dem TAPI-Server stellt eine konsistente Schnittstelle zwischen diesen beiden Ebenen bereit.

Eine TAPI-Anwendung lädt die entsprechende dll in den Prozessbereich. Während der Initialisierung richtet TAPI eine RPC-Verbindung mit Tapisvr.exe ein. Der TAPI-Server wird im Kontext von svchost ausgeführt.

TAPI: Tapi.dll, Tapi32.dll und Tapi3.dll sind drei DLLs zugeordnet. Diese DLLs befinden sich im Verzeichnis% systemroot% \\ system32. In der folgenden Abbildung werden die Rollen ihrer jeweiligen Rollen in Microsoft-telefonietelefoniefunktionen veranschaulicht:

![Rollen der drei TAPI-DLLs](images/dllserv.png)

Vorhandene 16-Bit-Anwendungen können mit Tapi.dll verknüpft werden. Tapi.dll ist einfach eine Thunk-Ebene, die 16-Bit-Adressen 32-Bit-Adressen zuordnet und Anforderungen an Tapi32.dll übergibt.

Vorhandene 32-Bit-TAPI 2. x-Anwendungen können mit Tapi32.dll verknüpft werden. Tapi32.dll ist eine schlanke Marshalling-Ebene, die Funktionsanforderungen an den TAPI-Server (tapisrv) überträgt und bei Bedarf die Medien Dienstanbieter-DLLs im Prozess der Anwendung lädt und aufruft.

TAPI 3. x-Anwendungen können mit Tapi3.dll verknüpft werden.

 

 



