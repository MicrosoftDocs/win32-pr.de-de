---
title: Senden des Aufrufs an das Serverprogramm
description: Nachdem die clientseitige RPC-Laufzeit mit dem Serverendpunkt verbunden wurde, marshallt sie die Argumente und sendet sie an den Server.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Rpc für Remoteprozeduraufruf , Tasks, Senden des Aufrufs an den Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a02d4fc1d69ba45cc6de3d43fba62724de1277471992790e3098225f579d305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017910"
---
# <a name="sending-the-call-to-the-server-program"></a>Senden des Aufrufs an das Serverprogramm

Nachdem die clientseitige RPC-Laufzeit mit dem Serverendpunkt verbunden wurde, marshallt sie die Argumente und sendet sie an den Server. Die RPC-Laufzeit des Servers gibt die marshallten Argumente an den Stub zurück, der sie entmarshallt, und übergibt sie dann an die Serverroutinen. Wenn die Serverroutinen zurückgeben, nimmt der Stub die Out- und \[ \] In-Out-Parameter und den Rückgabewert auf, marshallt sie und sendet die marshallten Daten an die RPC-Laufzeit des \[ \] Servers. Die RPC-Laufzeit sendet die Daten zurück an den Client, wobei die RPC-Laufzeit des Clients sie an den clientseitigen Stub übergibt, der sie entmarshallt und an den Aufrufer zurückgibt.

 

 




