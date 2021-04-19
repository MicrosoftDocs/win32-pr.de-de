---
description: In TAPI-Version 3,0 und höher verwendet das TAPI-Objektmodell Terminal Objekte zur Darstellung der Quelle oder Senke eines Mediendaten Stroms, der einer Telefon-oder Kommunikationssitzung zugeordnet ist.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Terminal Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2568d3c6f047fec8ca46b3b7d56e5026b61a1113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369902"
---
# <a name="terminal-object"></a>Terminal Objekt

In TAPI-Version 3,0 und höher verwendet das TAPI-Objektmodell Terminal Objekte zur Darstellung der Quelle oder Senke eines Mediendaten Stroms, der einer Telefon-oder Kommunikationssitzung zugeordnet ist. Dieses Objektmodell ermöglicht es einer Anwendung, auf einer detaillierten Ebene anzugeben, wie Medien bei einem-Befehl verarbeitet werden. Dieses Modell ermöglicht außerdem die gleichzeitige Auswahl mehrerer Terminals, sodass z. b. ein-Rückruf an einen audioredner ausgegeben und gleichzeitig aufgezeichnet werden kann.

Das Terminal Objekt stellt eine Quelle oder einen Renderer dar, z. b. ein Mikrofon oder ein Redner. Eine Anwendung wählt basierend auf der Medien Richtung und dem Typ oder den Typen, die an einer Kommunikationssitzung beteiligt sind, unter Verfügbare Terminals aus. Jeder zugeordnete Mediendaten Strom wird dann auf dem entsprechenden Terminal ausgewählt, um das Streaming zu starten.

Terminals werden normalerweise von einem Medien Dienstanbieter (MSP) implementiert, und Terminal Objekte sind nicht verfügbar, wenn einer Kommunikationssitzung kein MSP zugeordnet ist. Eine Ausnahme besteht darin, dass eine Anwendung mit Windows 2000 SP1 und höher eine Form des [austauschbaren Terminal](pluggable-terminals.md)implementieren kann. Dies ermöglicht es einem Konferenz Server, Bridging-Terminals zu erstellen, sodass nicht-Windows 2000 SP1-oder nicht-Multicast-h323-Clients zu TAPI 3 Multi-Party-SDP/IP-Multicast Konferenzen hinzugefügt werden können.

Jedes Terminal gehört zu einer [Terminal Klasse](terminal-class.md). Eine Terminal Klasse stellt einen Satz von Quell-oder Rendering-Funktionen dar. Beispielsweise würde ein Terminal, das einem Satz von audioreferenten zugeordnet ist, als CLSID \_ speakersterminal identifiziert werden, und der Dienstanbieter wird die Implementierung der volumesteuerung erwarten. TAPI 3 definiert einen Satz von Terminal Klassen, ein MSP kann zusätzliche Klassen definieren, und eine Anwendung kann neue Terminal Klassen registrieren. Jeder Terminal Klasse wird eine Globally Unique Identifier (GUID) zugewiesen.

Aus der Sicht einer Anwendung wird ein Terminal durch den [Terminaltyp](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) und die [Richtung](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)beschrieben. Der Typ kann entweder statisch oder dynamisch sein. Ein statisches Terminal ist Hardware zugeordnet, z. b. ein Telefon oder Mikrofon. Ein dynamisches Terminal ist einem vorübergehenden Objekt zugeordnet, z. b. einer Datei oder einem Videofenster. Richtung beschreibt, ob ein bestimmtes Terminal eine Quelle oder ein Renderer ist.

Die Funktionen eines bestimmten Terminal Objekts können sich je nach verwendetem aktuellen Dienstanbieter paar erheblich unterscheiden. Der MSP für ein spezielles Gerät kann eine Schnittstelle mit Methoden implementieren, die für dieses Gerät geeignet sind. Diese Schnittstelle kann auf dem Terminal Objekt und den Methoden, die einer Anwendung zur Verfügung gestellt werden, aggregiert werden. Weitere Informationen und Referenzmaterial finden Sie in der Media Service Provider-Dokumentation.

Weitere Informationen zu den von TAPI 3 implementierten Terminal Schnittstellen und Methoden finden Sie unter [Terminal Objekt Schnittstellen](terminal-object-interfaces.md).

Wenn die Autoren eines Media Service-Anbieters die MSP-Basisklassen verwenden, implementieren Sie möglicherweise einige der endfeatures für das Medien Streaming.

Weitere Informationen und Codebeispiele, die Abbildungen der Verwendung eines Terminal Objekts darstellen, finden Sie unter [tätigen eines Aufrufes](make-a-call.md) und [empfangen eines Aufrufes](receive-a-call.md).

**Windows XP:** Weitere Informationen darüber, wie das Terminal Objekt in Windows XP erweitert wurde, finden Sie unter [Datei Terminals](file-terminals.md), [Multitrack-Terminals](multitrack-terminals.md)und [austauschbare Terminals](pluggable-terminals.md).

Weitere Informationen und Codebeispiele finden Sie unter [Verwenden von Datei Terminals](using-file-terminals.md), [Verwenden von Multitrack-Terminals und dem Standardauswahl Mechanismus](using-multitrack-terminals-and-the-default-selection-mechanism.md)sowie [austauschbare Terminal Registrierung](pluggable-terminal-registration.md).

 

 



