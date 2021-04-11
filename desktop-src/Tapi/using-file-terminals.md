---
description: Die Datei Terminals können auf zwei Arten verwendet werden.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Verwenden von Datei Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131925"
---
# <a name="using-file-terminals"></a>Verwenden von Datei Terminals

Die Datei Terminals können auf zwei Arten verwendet werden. Die einfachste Methode ist die Verwendung von [**ITBasicCallControl2:: selectterminaloncallzum**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) auswählen eines Datei Terminals (Wiedergabe oder Datensatz) für ein TAPI-calltobjekt. In diesem Fall übernimmt TAPI das Verbinden der Audiodatenströme mit den Track-Terminals.

Die zweite Methode ermöglicht einer Anwendung eine präzisere Kontrolle über die Zuordnung von Audiostreams zu den nach Titeln. In diesem Szenario listet die Anwendung die für den-Befehl verfügbaren Streams auf, wählt diejenigen aus, die Sie aufzeichnen möchten (oder für die Wiedergabe zu verwenden), erstellt (oder sucht nach der Wiedergabe) die entsprechenden Spuren im dateiterminal und wählt die Spuren in callstreams aus.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Einfache Wiedergabe](simple-playback.md)
-   [Nachverfolgung gesteuerte Wiedergabe](track-controlled-playback.md)
-   [Einfacher Datensatz](simple-record.md)
-   [Nachverfolgung gesteuerter Datensatz](track-controlled-record.md)

 

 



