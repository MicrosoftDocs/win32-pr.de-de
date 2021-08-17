---
description: In TAPI Version 3.0 und höher verwendet das TAPI-Objektmodell Terminalobjekte, um die Quelle oder Senke eines Einem Aufruf oder einer Kommunikationssitzung zugeordneten Medienstreams zu darstellen.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Terminalobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe85dcf2643cbf60835a7df9e8b20de8287da2c752ed6555f480609d9b79873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476260"
---
# <a name="terminal-object"></a>Terminalobjekt

In TAPI Version 3.0 und höher verwendet das TAPI-Objektmodell Terminalobjekte, um die Quelle oder Senke eines Einem Aufruf oder einer Kommunikationssitzung zugeordneten Medienstreams zu darstellen. Mit diesem Objektmodell kann eine Anwendung auf detaillierter Ebene angeben, wie Medien bei einem Aufruf verarbeitet werden. Dieses Modell ermöglicht auch die gleichzeitige Auswahl mehrerer Terminals, sodass beispielsweise ein Anruf an einen Audiolautlauter ausgegeben und gleichzeitig aufgezeichnet werden kann.

Das Terminal-Objekt stellt eine Quelle oder einen Renderer dar, z. B. ein Mikrofon oder einen Lautsprecher. Eine Anwendung wählt basierend auf der Medienrichtung und dem Typ oder den Typen, die an einer Kommunikationssitzung beteiligt sind, zwischen verfügbaren Terminals aus. Jeder zugeordnete Medienstream wird dann auf dem entsprechenden Terminal ausgewählt, um mit dem Streaming zu beginnen.

Terminals werden normalerweise von einem Mediendienstanbieter (Media Service Provider, MSP) implementiert, und Terminalobjekte sind nicht verfügbar, wenn einer Kommunikationssitzung kein MSP zugeordnet ist. Eine Ausnahme ist, dass mit Windows 2000 SP1 und höher eine Anwendung eine Form von anschlussbarem [Terminal implementieren kann.](pluggable-terminals.md) Dadurch kann ein Konferenzserver Bridgingterminals erstellen, sodass Nicht-Windows 2000 SP1- oder Nicht-Multicast-H323-Clients zu TAPI 3-Multicastkonferenzen mit mehrstufigem SDP/IP hinzugefügt werden können.

Jedes Terminal gehört zu einer [Terminalklasse.](terminal-class.md) Eine Terminalklasse stellt einen Satz von Quell- oder Renderfeatures dar. Beispielsweise würde ein Terminal, das einem Satz von Audioreferenten zugerechnet wird, als CLSID SpeakersTerminal identifiziert, und vom Dienstanbieter wird erwartet, dass er die \_ Lautstärkesteuerung implementiert. TAPI 3 definiert eine Reihe von Terminalklassen, ein MSP kann zusätzliche Klassen definieren, und eine Anwendung kann neue Terminalklassen registrieren. Jeder Terminalklasse wird ein global eindeutiger Bezeichner (GLOBALLY UNIQUE IDENTIFIER, GUID) zugewiesen.

Aus Sicht einer Anwendung wird ein Terminal durch seinen Terminaltyp und die [Richtung](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) [beschrieben.](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) Der Typ kann entweder statisch oder dynamisch sein. Ein statisches Terminal ist hardwarebeschleunbar, z. B. einem Telefon oder Mikrofon. Ein dynamisches Terminal wird einem vorübergehenden Objekt wie einer Datei oder einem Videofenster zuordnen. Die Richtung beschreibt, ob ein bestimmtes Terminal eine Quelle oder ein Renderer ist.

Die Funktionen eines bestimmten Terminalobjekts können je nach dem aktuell verwendeten Dienstanbieterpaar erheblich variieren. Der MSP für ein spezialisiertes Gerät könnte eine Schnittstelle mit Methoden implementieren, die für dieses Gerät geeignet sind. Diese Schnittstelle könnte auf dem Terminalobjekt aggregiert werden, und die Methoden, die einer Anwendung zur Verfügung gestellt werden, können aggregiert werden. Weitere Informationen und Referenzmaterial finden Sie in der Dokumentation zum Mediendienstanbieter.

Weitere Informationen zu Terminalschnittstellen und -methoden, die von TAPI 3 implementiert werden, finden Sie unter [TerminalObjektschnittstellen](terminal-object-interfaces.md).

Wenn die Autoren eines Mediendienstanbieters die MSP-Basisklassen verwenden, können sie einige der Media Streaming Terminal-Features implementieren.

Weitere Informationen und Codebeispiele, die Abbildungen zur Verwendung eines Terminal-Objekts zeigen, finden Sie unter [Make a Call](make-a-call.md) and Receive a [Call](receive-a-call.md).

**Windows XP:** Weitere Informationen dazu, wie das Terminalobjekt in Windows XP [](file-terminals.md)erweitert wurde, finden Sie unter Dateiterminals, [Multitrack-Terminals](multitrack-terminals.md)und [Pluggable-Terminals.](pluggable-terminals.md)

Weitere Informationen und Codebeispiele finden Sie unter [Verwenden](using-file-terminals.md)von Dateiterminals, [Verwenden von Multitrack-Terminals](using-multitrack-terminals-and-the-default-selection-mechanism.md)und dem Standardauswahlmechanismus und [Pluggable Terminal Registration](pluggable-terminal-registration.md).

 

 



