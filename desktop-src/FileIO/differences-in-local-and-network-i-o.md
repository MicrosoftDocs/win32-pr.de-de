---
description: Unterschiede zwischen lokalem e/a und Netzwerk-e/a unter Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Unterschiede in lokalen und Netzwerk-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363544"
---
# <a name="differences-in-local-and-network-io"></a>Unterschiede in lokalen und Netzwerk-e/a

Es gibt einige wichtige Unterschiede zwischen lokalem e/a und Netzwerk-e/a unter Windows:

-   Die Netzwerk-e/a-Unterstützung ist abhängig vom Redirector und dem Netzwerkprotokoll.
-   Die Netzwerk-e/a-Leistung hängt von der Anzahl der Netzwerk-e/a-Vorgänge und der Geschwindigkeit der Netzwerkverbindung ab. Ihre Anwendung muss in der Lage sein, Netzwerk-e/a-Vorgänge mit Servern zu verarbeiten, die viel schneller oder langsamer als der lokale Computer sein können, sowie vorübergehende Änderungen an der Netzwerkkapazität. In diesen Fällen muss Ihre Anwendung möglicherweise mehr Zeit für den Abschluss des Vorgangs zulassen.
-   Die Funktionen, die Sie verwenden, um lokale Datei-e/a auszuführen, können sich über das Netzwerk anders Verhalten. Beispielsweise kann bei einem Netzwerk-e/a-Vorgang, der lange dauert, ein Timeout auftreten. In einigen Situationen kann es sein, dass Datei Handles unbegrenzt offen bleiben. Ein weiteres Beispiel ist, dass Functions Fehlercodes zurückgeben kann, die Ihre Anwendung für die Netzwerk-e/a-Vorgänge spezifisch verarbeitet.

 

 



