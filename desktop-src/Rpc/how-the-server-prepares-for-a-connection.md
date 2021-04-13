---
title: Wie der Server eine Verbindung vorbereitet
description: Wenn ein Serverprogramm mit der Ausführung beginnt, muss es zuerst die Schnittstelle oder die darin enthaltenen Schnittstellen mit der RPC-Lauf Zeit Bibliothek registrieren.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310352"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Wie der Server eine Verbindung vorbereitet

Wenn ein Serverprogramm mit der Ausführung beginnt, muss es zuerst die Schnittstelle oder die darin enthaltenen Schnittstellen mit der RPC-Lauf Zeit Bibliothek registrieren. Anschließend werden die erforderlichen Bindungs Informationen erstellt. Das Serverprogramm muss auch den Endpunkt oder die Endpunkte registrieren, an dem er lauscht. Er kann dann mit dem lauschen auf Client Aufrufe beginnen. Dieser Vorgang wird in der folgenden Abbildung veranschaulicht.

![eine RPC-Serveranwendung bereitet Clientverbindungen vor](images/srvrcon.png)

Je nach ausgewähltem Entwurf kann eine Serveranwendung eine andere Gruppe von Schritten auswählen. im vorherigen Beispiel und in der Abbildung ist ein Ansatz enthalten.

Dieser Abschnitt enthält Informationen zu den Schritten, die ein Server Prozess ausführen muss, um eine Verbindung vorzubereiten. Die Diskussion ist in die folgenden Abschnitte unterteilt:

-   [Registrieren der-Schnittstelle](registering-the-interface.md)
-   [Verfügbar machung des Servers im Netzwerk](making-the-server-available-on-the-network.md)
-   [Registrieren von Endpunkten](registering-endpoints.md)
-   [Lauschen auf Client Anrufe](listening-for-client-calls.md)

 

 




