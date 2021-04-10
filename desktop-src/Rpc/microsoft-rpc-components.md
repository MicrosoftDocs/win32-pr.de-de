---
title: RPC-Komponenten
description: Remote Prozedur Aufruf-Komponenten (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947770"
---
# <a name="rpc-components"></a>RPC-Komponenten

RPC umfasst die folgenden Hauptkomponenten:

-   Mittlerer l-Compiler
-   Laufzeitbibliotheken und Header Dateien
-   Name Service Provider (manchmal auch als Locator bezeichnet)
-   Endpunkt Zuordnung (manchmal auch als Port-Mapper bezeichnet)

Im RPC-Modell können Sie eine Schnittstelle für die Remote Prozeduren formal mithilfe einer für diesen Zweck entworfenen Sprache angeben. Diese Sprache wird als Schnittstellen Definitions Sprache oder IDL bezeichnet. Die Microsoft-Implementierung dieser Sprache wird als Microsoft Interface Definition Language oder als Mittelwert bezeichnet.

Nachdem Sie eine Schnittstelle erstellt haben, müssen Sie Sie über den Mittelwert Compiler übergeben. Dieser Compiler generiert die stubweise, die Aufrufe von lokalen Prozeduren in Remote Prozedur Aufrufe übersetzen. Stubel sind Platzhalter Funktionen, die Aufrufe an die Lauf Zeit Bibliotheksfunktionen durchführen, die den Remote Prozedur Aufruf verwalten. Der Vorteil dieses Ansatzes besteht darin, dass das Netzwerk für Ihre verteilte Anwendung fast vollständig transparent wird. Ihr Client Programm ruft auf, was als lokale Prozeduren erscheinen soll. die Arbeit, Sie in Remote aufrufen umzuwandeln, erfolgt automatisch. Der gesamte Code, der Daten übersetzt, auf das Netzwerk zugreift und Ergebnisse abruft, wird vom Mittelwert Compiler generiert und ist für Ihre Anwendung nicht sichtbar.

 

 




