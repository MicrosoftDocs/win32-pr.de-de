---
title: RPC-Komponenten
description: RPC-Komponenten (Remote Procedure Call).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Remoteprozeduraufruf RPC , beschrieben, Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b3416589eccf865b70d3da82fa7494631ab7592f172bb46c10eccb1d96fad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928119"
---
# <a name="rpc-components"></a>RPC-Komponenten

RPC umfasst die folgenden Hauptkomponenten:

-   MIDL-Compiler
-   Laufzeitbibliotheken und Headerdateien
-   Name-Dienstanbieter (manchmal auch als Locator bezeichnet)
-   Endpunktzuordnung (manchmal auch als Portzuordnung bezeichnet)

Im RPC-Modell können Sie formell eine Schnittstelle zu den Remoteprozeduren angeben, indem Sie eine für diesen Zweck entwickelte Sprache verwenden. Diese Sprache wird als Schnittstellendefinitionssprache (Interface Definition Language, IDL) bezeichnet. Die Microsoft-Implementierung dieser Sprache wird als Microsoft Interface Definition Language oder MIDL bezeichnet.

Nachdem Sie eine Schnittstelle erstellt haben, müssen Sie sie über den MIDL-Compiler übergeben. Dieser Compiler generiert die Stubs, die lokale Prozeduraufrufe in Remoteprozeduraufrufe übersetzen. Stubs sind Platzhalterfunktionen, die die Aufrufe der Laufzeitbibliotheksfunktionen ausführen, die den Remoteprozeduraufruf verwalten. Der Vorteil dieses Ansatzes besteht darin, dass das Netzwerk für Ihre verteilte Anwendung nahezu vollständig transparent wird. Ihr Clientprogramm ruft scheinbar lokale Prozeduren auf. die Umwandlung in Remoteaufrufe erfolgt automatisch für Sie. Der gesamte Code, der Daten übersetzt, auf das Netzwerk zugreift und Ergebnisse abruft, wird vom MIDL-Compiler für Sie generiert und ist für Ihre Anwendung nicht sichtbar.

 

 




