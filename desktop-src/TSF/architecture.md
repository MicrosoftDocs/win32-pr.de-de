---
title: Architektur (Text Dienste-Framework)
description: Architektur
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Text Services-Framework (TSF), Architektur
- TSF (Text Dienst Framework), Architektur
- Text Dienste, Architektur
- TSF-aktivierte Anwendungen, Architektur
- Text Dienst Framework (TSF), Komponenten
- TSF (Text Dienst Framework), Komponenten
- Text Dienste, Komponenten
- TSF-aktivierte Anwendungen, Komponenten
- Text Dienst Framework (TSF), Anwendungen
- TSF (Text Dienst Framework), Anwendungen
- Text Dienste, Anwendungen
- TSF-aktivierte Anwendungen, Informationen zu
- Text Dienste-Framework (TSF), Text Dienste
- TSF (Text Dienst Framework), Text Dienste
- Text Dienste, Info
- TSF-aktivierte Anwendungen, Text Dienste
- Text Services-Framework (TSF), TSF Manager
- TSF (Text Dienst Framework), TSF Manager
- Text Dienste, TSF Manager
- TSF-aktivierte Anwendungen, TSF-Manager
- TSF-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555922"
---
# <a name="architecture-text-services-framework"></a>Architektur (Text Dienste-Framework)

Das Text Dienst-Framework umfasst drei Hauptkomponenten:

-   **Anwendungen:** Anwendungs Vorgänge umfassen in der Regel Anzeige, direkte Bearbeitung und Text Speicherung. Eine Anwendung ermöglicht den Zugriff auf Text durch Implementieren eines COM-Servers, der bestimmte Schnittstellen unterstützt und über Schnittstellen kommuniziert, die der TSF-Manager verfügbar macht. In dieser Dokumentation bezieht sich der Begriff "Anwendung" auf eine TSF-fähige Anwendung, sofern nicht anders angegeben.
-   **Text Dienste:** Ein Text Dienst fungiert als Text Anbieter für eine Anwendung. Ein Text Dienst kann Text aus einer Anwendung abrufen und Text in diese schreiben. Ein Text Dienst kann auch Daten und Eigenschaften einem TextBlock zuordnen. Ein Text Dienst wird als com-in-proc-Server implementiert, der sich bei TSF registriert. Bei der Registrierung interagiert der Benutzer mit dem Text Dienst über die sprach Leiste oder über Tastenkombinationen. Es können mehrere Text Dienste installiert werden.
-   **TSF-Manager:** Der TSF-Manager fungiert als Vermittler zwischen einer Anwendung und mindestens einem Text Dienst. Ein Text Dienst interagiert niemals direkt mit einer Anwendung. Die gesamte Kommunikation verläuft über den TSF-Manager. Der TSF-Manager wird vom Betriebssystem implementiert und kann nicht ersetzt werden. In dieser Dokumentation bezieht sich der Begriff Manager auf den TSF-Manager, sofern nicht anders angegeben.

Die folgende Abbildung zeigt die primären Architektur Elemente von TSF.

![Architektur des Frameworks für Text Dienste](images/tsf-arch.gif)

Mit dieser Architektur stellt der TSF-Manager eine Abstraktionsschicht zwischen Anwendungen und Text Diensten bereit. Diese Abstraktions Ebene ermöglicht einer Anwendung und einem oder mehreren Text Diensten das Freigeben von Text, und der TSF-Manager kann Text Dienste verwalten.

 

 




