---
title: Ablauf Steuerung
description: Ablauf Steuerung
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- Visualisierungen, Programmfluss
- benutzerdefinierte Visualisierungen, Programmfluss
- Visualisierungen, Ablauf Steuerung
- benutzerdefinierte Visualisierungen, Ablauf Steuerung
- Visualisierungen, zeitgesteuerte Ereignisse
- benutzerdefinierte Visualisierungen, zeitgesteuerte Ereignisse
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Visualisierungen, renderwindow-Funktion
- benutzerdefinierte Visualisierungen, renderwindow-Funktion
- Renderfunktion, Visualisierungsprogramm Fluss
- Renderwindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947476"
---
# <a name="flow-of-control"></a>Ablauf Steuerung

Audiodaten kommen in Windows Media Player fortlaufend über eine Datei oder einen Stream. Diese Daten werden an ihre Visualisierung übermittelt. Sie zeichnen eine definierte Oberfläche und übergeben diese wieder an Windows Media Player. Dieser Austausch erfolgt mehrmals pro Sekunde, und für den Benutzer ist das Ergebnis eine angenehme Animation, die sich in der Zeit auf die Musik verschiebt.

Im folgenden finden Sie eine bestimmte Abfolge des Visualisierungsprogramm Flusses:

1.  In einem zeitgesteuerten Intervall nimmt Windows Media Player eine Momentaufnahme der wiedergegebenen Audiodatei an.
2.  Windows Media Player stellt die Daten aus dieser Momentaufnahme über die Funktion " **Rendering** " und die **renderwindowed** -Funktion für die Visualisierung bereit.
3.  Sie müssen Code schreiben, der ausgeführt wird, wenn " **Rendering** " und " **renderwindowed** " aufgerufen werden. Der Code zeichnet mithilfe eines Geräte Kontexts, der von Windows Media Player beim Rendern von fensterlosen Funktionen definiert wird, oder mithilfe eines Fensters, das Sie beim Rendern des Fensters erstellen.
4.  In einer von der aktuellen Skin angegebenen Region zeigt Windows Media Player an, was Ihr Code gezeichnet hat.
5.  Dieser Vorgang wird mehrmals pro Sekunde wiederholt, wobei grafische Animationen erstellt werden, für die die Musik Zeitüberschreitung hat. Wenn die Musik angehalten wird, wird die Visualisierung angehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwickler Übersicht**](developer-overview.md)
</dt> </dl>

 

 




