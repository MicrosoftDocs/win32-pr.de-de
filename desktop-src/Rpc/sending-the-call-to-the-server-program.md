---
title: Senden des Aufrufes an das Server Programm
description: Sobald die Client seitige RPC-Laufzeit eine Verbindung mit dem Server Endpunkt hergestellt hat, Marshalls Sie die Argumente und sendet Sie an den Server.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Senden des Aufrufs an den Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310932"
---
# <a name="sending-the-call-to-the-server-program"></a>Senden des Aufrufes an das Server Programm

Sobald die Client seitige RPC-Laufzeit eine Verbindung mit dem Server Endpunkt hergestellt hat, Marshalls Sie die Argumente und sendet Sie an den Server. Die RPC-Laufzeit des Servers übergibt die marshallte Argumente an den Stub, der Sie unmarshallt und dann an die Server Routinen übergibt. Beim Zurückgeben der Server Routinen übernimmt der Stub die \[ out \] -und \[ in-out- \] Parameter und den Rückgabewert, marshallt Sie und sendet die marshallte Daten an die RPC-Laufzeit des Servers. Die RPC-Laufzeit sendet die Daten an den Client zurück, wobei die RPC-Laufzeit des Clients Sie an den Client seitigen Stub übergibt, der Sie unmarshalls und an den Aufrufer zurückgibt.

 

 




