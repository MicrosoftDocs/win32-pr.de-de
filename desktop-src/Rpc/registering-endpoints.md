---
title: Registrieren von Endpunkten
description: Wenn Sie das Serverprogramm in der Endpunkt Zuordnung des Server Host Computers registrieren, können Client Programme bestimmen, welcher Endpunkt (in der Regel ein TCP/IP-Port oder eine Named Pipe), an dem das Serverprogramm lauscht.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Registrieren von Endpunkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707326"
---
# <a name="registering-endpoints"></a>Registrieren von Endpunkten

Wenn Sie das Serverprogramm in der Endpunkt Zuordnung des Server Host Computers registrieren, können Client Programme bestimmen, welcher Endpunkt (in der Regel ein TCP/IP-Port oder eine Named Pipe), an dem das Serverprogramm lauscht. Um sich selbst in der Endpunkt Zuordnung des Server Host Systems zu registrieren, Ruft ein Serverprogramm die [**rpcepregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) -Funktion auf, wie im folgenden Code Fragment gezeigt:


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



Der erste Parameter für [**rpcepregiester**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) ist die-Struktur, die die-Schnittstelle darstellt. Sie finden Sie in der Header Datei, die der-Mittelwert Compiler aus der mittleren l-Datei für diese verteilte Anwendung generiert hat. Siehe [entwickeln der-Schnittstelle](developing-the-interface.md). Als nächstes muss die Anwendung von **rpcepregiester** eine Reihe von Bindungs Handles übergeben, die in einem Bindungs Vektor gespeichert werden.

Zusätzlich zum Registrieren von Schnittstellennamen kann die Serveranwendung auch Objekt-UUIDs in der Endpunkt Zuordnung registrieren. In diesem Beispiel sind keine Objekt-UUIDs vorhanden, die registriert werden können, sodass der dritte Parameter für [**rpcepregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) auf **null** festgelegt ist.

Der letzte Parameter ist eine Kommentar Zeichenfolge. Obwohl die RPC-Lauf Zeit Bibliothek diese Zeichenfolge nicht verwendet, wird das Festlegen der Zeichenfolge empfohlen, da dadurch die Verwaltbarkeit des Systems verbessert wird. Ein Systemadministrator kann mithilfe der Zeichenfolge erkennen, welche Ports von welchen-Anwendungen verwendet werden, um zu bestimmen, welche Ports von Firewalls verwaltet werden.

 

 




