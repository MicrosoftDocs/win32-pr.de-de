---
description: Die TAPI-DLLs sind zusammen mit dem TAPI-Server (Tapisvr.exe) wichtige Abstraktionen, die Endbenutzer- oder Serveranwendungen von Dienstanbietern trennen. Eine TAPI-DLL in Verbindung mit dem TAPI-Server stellt eine konsistente Schnittstelle zwischen diesen beiden Ebenen bereit.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff26274baf25047212a3f9f8e15c2211d90cbaa10db23674ae54dbb97bbfdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012204"
---
# <a name="tapi-dll"></a>TAPI-DLL

Die TAPI-DLLs sind zusammen mit dem TAPI-Server (Tapisvr.exe) wichtige Abstraktionen, die Endbenutzer- oder Serveranwendungen von Dienstanbietern trennen. Eine TAPI-DLL in Verbindung mit dem TAPI-Server stellt eine konsistente Schnittstelle zwischen diesen beiden Ebenen bereit.

Eine TAPI-Anwendung lädt die entsprechende DLL in ihren Prozessbereich. Während der Initialisierung richtet TAPI eine RPC-Verknüpfung mit Tapisvr.exe ein. Der TAPI-Server wird im Kontext von SVCHOST ausgeführt.

TAPI sind drei DLLs zugeordnet: Tapi.dll, Tapi32.dll und Tapi3.dll. Diese DLLs befinden sich in %SystemRoot% \\ system32. Die folgende Abbildung veranschaulicht die Rollen ihrer jeweiligen Rollen in Microsoft-Telefonie:

![Rollen der drei Tapi-DLLs](images/dllserv.png)

Vorhandene 16-Bit-Anwendungen sind mit Tapi.dll verknüpft. Tapi.dll ist einfach eine Thunkebene, die 16-Bit-Adressen 32-Bit-Adressen zu ordnet und Anforderungen an Tapi32.dll übergibt.

Vorhandene 32-Bit-TAPI 2.x-Anwendungen sind mit Tapi32.dll verknüpft. Tapi32.dll ist eine schlanke Marshallingebene, die Funktionsanforderungen an den TAPI-Server (TAPISRV) überträgt und bei Bedarf DLLs des Mediendienstanbieters im Prozess der Anwendung lädt und aufruft.

TAPI 3.x-Anwendungen sind mit Tapi3.dll verknüpft.

 

 



