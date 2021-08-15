---
title: Allgemeine Buildprozedur
description: Navigationsseite für den Prozess zum Erstellen einer Client-/Serveranwendung mithilfe des Remoteprozeduraufrufs (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8402a14ceac3b34114e7b40998038a4e09fb7ba1a915c173f2062f7fab9e63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929632"
---
# <a name="general-build-procedure"></a>Allgemeine Buildprozedur

Der Prozess zum Erstellen einer Client-/Serveranwendung mitHilfe von Microsoft RPC ist:

-   Entwickeln Sie die -Schnittstelle.
-   Entwickeln Sie den Server, der die -Schnittstelle implementiert.
-   Entwickeln Sie den Client, der die -Schnittstelle verwendet.

Die folgende Abbildung veranschaulicht diese Schritte.

![Prozess zum Erstellen einer Client-Server-Anwendung mit microsoft rpc](images/appdev.png)

Es ist möglich und üblich, die Client- und Serveranwendungen gleichzeitig zu entwickeln. Da sowohl das Client- als auch das Serverprogramm von der -Schnittstelle abhängig sind, muss die Schnittstelle zwischen ihnen jedoch vor der Entwicklung von Client und Server entwickelt werden, wie im vorherigen Diagramm dargestellt.

In diesem Abschnitt werden die Schritte erläutert, die zum Erstellen einer Client-/Serveranwendung mit RPC erforderlich sind. Die Informationen werden in den folgenden Themen vorgestellt:

-   [Entwickeln der Schnittstelle](developing-the-interface.md)
-   [Entwickeln des Servers](developing-the-server.md)
-   [Entwickeln des Clients](developing-the-client.md)

 

 




