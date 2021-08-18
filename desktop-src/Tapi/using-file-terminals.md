---
description: Die Dateiterminals können auf zwei Arten verwendet werden.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Verwenden von Dateiterminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd72a02306efb5503d184b3f4e678df1ab2517928c8c8406d98b1d7d0efb41d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975127"
---
# <a name="using-file-terminals"></a>Verwenden von Dateiterminals

Die Dateiterminals können auf zwei Arten verwendet werden. Die einfachste Methode ist die Verwendung von [**ITBasicCallControl2::SelectTerminalOnCall,**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) um ein Dateiterminal (Wiedergabe oder Datensatz) in einem TAPI-Aufrufobjekt auszuwählen. In diesem Fall stellt TAPI die Verbindung der Audiostreams mit den Trackterminals her.

Mit der zweiten Methode kann eine Anwendung die Zuordnung von Audiostreams zu Spuren feiner steuern. In diesem Szenario listet die Anwendung die beim Aufruf verfügbaren Streams auf, wählt die Datenströme aus, die sie aufzeichnen (oder für die Wiedergabe verwenden) möchte, erstellt (oder sucht für die Wiedergabe) die entsprechenden Spuren im Dateiterminal und wählt die Spuren in Aufrufstreams aus.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Einfache Wiedergabe](simple-playback.md)
-   [Trackgesteuerte Wiedergabe](track-controlled-playback.md)
-   [Einfacher Datensatz](simple-record.md)
-   [Track-Controlled Record](track-controlled-record.md)

 

 



