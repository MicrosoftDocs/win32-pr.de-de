---
title: Flow des Steuerelements
description: Flow des Steuerelements
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- Visualisierungen, Programmablauf
- Benutzerdefinierte Visualisierungen, Programmablauf
- Visualisierungen,Ablauf der Steuerung
- Benutzerdefinierte Visualisierungen, Ablauf der Steuerung
- Visualisierungen,Zeitereignisse
- Benutzerdefinierte Visualisierungen, Zeitereignisse
- Visualisierungen,Render-Funktion
- Benutzerdefinierte Visualisierungen, Renderfunktion
- Visualisierungen,RenderWindow-Funktion
- Benutzerdefinierte Visualisierungen,RenderWindow-Funktion
- Renderfunktion, Visualisierungsprogrammfluss
- RenderWindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332d9c907e7c25f81d01bc8adf48c6d4d91a7b17763a1b0daf0007a8534ac4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934739"
---
# <a name="flow-of-control"></a>Flow des Steuerelements

Audiodaten werden kontinuierlich Windows Media Player einer Datei oder einem Stream übertragen. Diese Daten werden an Ihre Visualisierung übergeben. Sie zeichnen auf einer definierten Oberfläche und übergeben diese Oberfläche an Windows Media Player. Dieser Austausch erfolgt mehrmals pro Sekunde, und für den Benutzer ist das Ergebnis eine ansprechende Animation, die sich im Laufe der Zeit zur Musik bewegt.

Dies ist die spezifische Sequenz des Ablaufs des Visualisierungsprogramms:

1.  In einem bestimmten Intervall erstellt Windows Media Player eine Momentaufnahme der Audiodatei, die abspielt.
2.  Windows Media Player stellt die Daten aus dieser Momentaufnahme über die **Render-Funktion** und die **RenderWindowed-Funktion** für Ihre Visualisierung zur Verfügung.
3.  Sie müssen Code schreiben, der ausgeführt wird, **wenn Render** **und RenderWindowed** aufgerufen werden. Der Code zeichnet mithilfe eines Gerätekontexts, der durch Windows Media Player beim rendern ohne Fenster definiert ist, oder mithilfe eines Fensters, das Sie beim Rendern eines Fensters erstellen.
4.  In einem Bereich, der durch die aktuelle Skin angegeben wird, Windows Media Player, was Ihr Code lässige.
5.  Dieser Vorgang wird mehrmals pro Sekunde wiederholt, und es werden grafische Animationen erstellt, für die ein Timer für die Musik verwendet wird. Wenn die Wiedergabe der Musik beendet wird, wird die Visualisierung beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwicklerübersicht**](developer-overview.md)
</dt> </dl>

 

 




