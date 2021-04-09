---
title: Allgemeine buildprozedur
description: Navigationsseite für den Prozess zum Erstellen einer Client/Server-Anwendung mithilfe eines Remote Prozedur Aufrufs (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036837"
---
# <a name="general-build-procedure"></a>Allgemeine buildprozedur

Der Prozess zum Erstellen einer Client-/Serveranwendung mithilfe von Microsoft RPC lautet wie folgt:

-   Entwickeln Sie die-Schnittstelle.
-   Entwickeln Sie den Server, der die-Schnittstelle implementiert.
-   Entwickeln Sie den Client, der die-Schnittstelle verwendet.

Diese Schritte werden in der folgenden Abbildung veranschaulicht.

![Prozess zum Erstellen einer Client-/Serveranwendung mithilfe von Microsoft RPC](images/appdev.png)

Es ist möglich und üblich, die Client-und Server Anwendungen gleichzeitig zu entwickeln. Da sowohl das Client-als auch das Serverprogramm von der-Schnittstelle abhängig sind, muss die Schnittstelle zwischen Ihnen jedoch vor der Entwicklung des Clients und des Servers entwickelt werden, wie im obigen Diagramm gezeigt.

In diesem Abschnitt werden die erforderlichen Schritte zum Aufbauen einer Client/Server-Anwendung mit RPC erläutert. Die Informationen finden Sie in den folgenden Themen:

-   [Entwickeln der Schnittstelle](developing-the-interface.md)
-   [Entwickeln des Servers](developing-the-server.md)
-   [Entwickeln des Clients](developing-the-client.md)

 

 




