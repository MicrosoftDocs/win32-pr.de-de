---
title: Vorbereiten einer Verbindung durch den Server
description: Wenn ein Serverprogramm mit der Ausführung beginnt, muss es zuerst die schnittstelle oder schnittstellen registrieren, die es enthält, bei der RPC-Laufzeitbibliothek.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66314c55ad8e78922f7afcc74c6de3b4afad8234293373cf0cd35a560a1942ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929492"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Vorbereiten einer Verbindung durch den Server

Wenn ein Serverprogramm mit der Ausführung beginnt, muss es zuerst die schnittstelle oder schnittstellen registrieren, die es enthält, bei der RPC-Laufzeitbibliothek. Anschließend werden die erforderlichen Bindungsinformationen erstellt. Das Serverprogramm muss auch den Endpunkt oder die Endpunkte registrieren, an dem bzw. an dem es lausiert. Anschließend kann er mit dem Lauschen auf Clientaufrufe beginnen. Dieser Vorgang wird im folgenden Diagramm veranschaulicht.

![Eine RPC-Serveranwendung bereitet sich auf Clientverbindungen vor.](images/srvrcon.png)

Je nach gewähltem Entwurf kann eine Serveranwendung einen anderen Satz von Schritten auswählen. Das vorherige Beispiel und die Abbildung bieten einen Ansatz.

Dieser Abschnitt enthält Informationen zu den Schritten, die ein Serverprozess ausführen muss, um eine Verbindung vorzubereiten. Die Diskussion ist in die folgenden Abschnitte unterteilt:

-   [Registrieren der Schnittstelle](registering-the-interface.md)
-   [Verfügbar machen des Servers im Netzwerk](making-the-server-available-on-the-network.md)
-   [Registrieren von Endpunkten](registering-endpoints.md)
-   [Lauschen auf Clientaufrufe](listening-for-client-calls.md)

 

 




