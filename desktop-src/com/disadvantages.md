---
title: Nachteile
description: Nachteile
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516005"
---
# <a name="disadvantages"></a>Nachteile

In-Process-Server bieten den Vorteil der Geschwindigkeit und Größe eines Objekt Handlers mit der Bearbeitungsfunktion eines lokalen Servers. Warum sollten Sie sich also entscheiden, Ihre OLE-Anwendung als lokalen Server und nicht als Prozess interner Server zu implementieren? Es gibt mehrere Gründe:

-   Sicherheit. Nur ein lokaler Server hat seinen Adressraum isoliert von dem des Clients. Ein Prozess interner Server nutzt den Adressraum und den Prozess Kontext des Clients und kann daher bei Fehlern oder böswilliger Programmierung weniger robust sein.
-   Granularität. Ein lokaler Server kann mehrere Instanzen seines Objekts über viele verschiedene Clients hinweg hosten, wobei der Serverstatus zwischen Objekten in mehreren Clients auf eine Weise freigegeben werden kann, die schwierig oder unmöglich wäre, wenn er als Prozess interner Server implementiert wird. dabei handelt es sich einfach um eine DLL, die in jeden Client geladen wird.
-   Kompatibilität. Wenn Sie sich für die Implementierung eines in-Process-Servers entscheiden, wird die Kompatibilität mit OLE 1 aufgegeben, das solche Server nicht unterstützt. Dies ist für viele Entwickler nicht zu berücksichtigen, aber wenn dies der Fall ist, ist es von entscheidender Bedeutung.
-   Keine Unterstützung von Links. Ein Prozess interner Server kann nicht als Verknüpfungs Quelle fungieren. Da eine DLL nicht eigenständig ausgeführt werden kann, kann Sie kein Datei Objekt erstellen, mit dem eine Verknüpfung erstellt werden kann.

Trotz dieser Nachteile kann ein Prozess interner Server eine hervorragende Wahl für seine Geschwindigkeit und Größe sein – wenn er alle Ihre anderen Anforderungen erfüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorteile](advantages.md)
</dt> <dt>

[Prozess interne Server](in-process-servers.md)
</dt> </dl>

 

 




