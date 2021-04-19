---
description: TAPI 3,1 führt das Konzept eines Multitrack-Terminals ein, ein Terminal, das im Wesentlichen eine Sammlung von &\# 0034, Track&\# 0034; Terminals ist.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Multitrack-Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348819"
---
# <a name="multitrack-terminals"></a>Multitrack-Terminals

TAPI 3,1 führt das Konzept eines Multitrack-Terminals ein, ein Terminal, bei dem es sich im Wesentlichen um eine Sammlung von "Track"-Terminals handelt. Multitrack-Terminals vereinfachen die Auslastung des Programmierers in Situationen, in denen mehrere Medienströme an einer Kommunikationssitzung beteiligt sind.

Das [Datei Aufzeichnungs Terminal](file-playback-terminal-and-file-recording-terminal.md) ist ein Beispiel für ein Multitrack-Terminal. Er besteht aus "Track", wobei jeder "Track" ein Terminal ist, das einem Stream in der aufgezeichneten Datei entspricht.

Ein [Track-Terminal](track-terminals.md) kann ein anderes Multitrack-Terminal oder ein Single-Track-Terminal sein. Ein Single-Track-Terminal ist ein Terminal, das keine Nachverfolgung von Terminals hat. Ein Single-Track-Terminal ist ein Terminal im TAPI 3-Sinne des Worts.

Weitere Informationen zu Multitrack-Terminals finden Sie in den folgenden Themen:

-   [Informationen zu Multitrack-Terminals](about-multitrack-terminals.md)
-   [Standardmäßiger Terminal Auswahlmechanismus](default-terminal-selection-mechanism.md)
-   [Manuelle Terminal Auswahl](manual-terminal-selection.md)
-   [Verwenden von Multitrack-Terminals und dem Standardauswahl Mechanismus](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



