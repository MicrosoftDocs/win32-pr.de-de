---
title: Informationen zur mciwnd-Fenster Klasse
description: Informationen zur mciwnd-Fenster Klasse
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Mciwnd-Fenster Klasse, Informationen zu
- Mciwndcreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388352"
---
# <a name="about-the-mciwnd-window-class"></a>Informationen zur mciwnd-Fenster Klasse

Die mciwnd-Fenster Klasse ist einfach zu verwenden. Durch die Verwendung einer einzelnen Funktion kann [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Ihre Anwendung ein Steuerelement erstellen, das jedes Gerät wieder gibt, das die Media Control Interface (MCI) verwendet. Zu diesen Geräten gehören CD-Audiodaten, Waveform-Audiodaten, MIDI und Videogeräte.

Die Automatisierung der Wiedergabe ist auch schnell und einfach. Wenn Sie nur eine Funktion und zwei Makros verwenden, kann eine Anwendung ein mciwnd-Fenster mit dem entsprechenden Medien Gerät erstellen, das Gerät wiedergeben und sowohl das Gerät als auch das Fenster schließen, wenn die Wiedergabe des Inhalts beendet ist.

> [!Note]  
> Einige Geräte spielen Inhalt, der in Dateien gespeichert ist. Andere Geräte, z. b. CD-Audiogeräte, geben Inhalte wieder, die auf einem anderen Medium gespeichert sind. Aus Gründen der Übersichtlichkeit bezieht sich diese Übersicht auf beide Umstände als "Wiedergabe des Geräts".

 

 

 




