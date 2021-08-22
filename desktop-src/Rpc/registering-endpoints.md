---
title: Registrieren von Endpunkten
description: Durch das Registrieren des Serverprogramms in der Endpunktzuordnung des Serverhostcomputers können Clientprogramme bestimmen, an welchem Endpunkt (in der Regel ein TCP/IP-Port oder eine Named Pipe) das Serverprogramm lauscht.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Remoteprozeduraufruf RPC , Tasks, Registrieren von Endpunkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6674d20eefa9ebd690f618c36f1dfe69f37dcf7743a0830e06cb38bc85ccfd56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926858"
---
# <a name="registering-endpoints"></a>Registrieren von Endpunkten

Durch das Registrieren des Serverprogramms in der Endpunktzuordnung des Serverhostcomputers können Clientprogramme bestimmen, an welchem Endpunkt (in der Regel ein TCP/IP-Port oder eine Named Pipe) das Serverprogramm lauscht. Um sich selbst in der Endpunktzuordnung des Serverhostsystems zu registrieren, ruft ein Serverprogramm die [**RpcEpRegister-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) auf, wie im folgenden Codefragment gezeigt:


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



Der erste Parameter für [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) ist die -Struktur, die die -Schnittstelle darstellt. Sie finden sie in der Headerdatei, die der MIDL-Compiler aus Ihrer MIDL-Datei für diese verteilte Anwendung generiert hat. Weitere Informationen finden Sie [unter Entwickeln der Schnittstelle](developing-the-interface.md). Als Nächstes benötigt **RpcEpRegister,** dass Ihre Anwendung eine Reihe von Bindungshandles übergibt, die in einem Bindungsvektor gespeichert sind.

Neben dem Registrieren von Schnittstellennamen kann Ihre Serveranwendung auch Objekt-UUIDs in der Endpunktzuordnung registrieren. In diesem Beispiel müssen keine Objekt-UUIDs registriert werden, sodass der dritte Parameter auf [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) auf **NULL** festgelegt ist.

Der letzte Parameter ist eine Kommentarzeichenfolge. Obwohl die RPC-Laufzeitbibliothek diese Zeichenfolge nicht verwendet, wird empfohlen, die Zeichenfolge festzulegen, da sie die Verwaltbarkeit des Systems verbessert. Ein Systemadministrator kann die Zeichenfolge verwenden, um zu ermitteln, welche Ports von welchen Anwendungen verwendet werden. Anschließend kann er ermitteln, welche Ports von Firewalls verwaltet werden sollen.

 

 




