---
title: Informationen zur MCIWnd Window-Klasse
description: Informationen zur MCIWnd Window-Klasse
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- MCIWnd-Fensterklasse,about
- MCIWndCreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a75f9798c1bfe0ec4f67da0f990018143efd0285541b49a9035b9749a36de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065660"
---
# <a name="about-the-mciwnd-window-class"></a>Informationen zur MCIWnd Window-Klasse

Die MCIWnd Window-Klasse ist einfach zu verwenden. Mithilfe einer einzelnen Funktion kann [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Ihre Anwendung ein Steuerelement erstellen, das jedes Gerät abspielt, das die Mediensteuerungsschnittstelle (Media Control Interface, MCI) verwendet. Zu diesen Geräten gehören CD-Audio, Waveform-Audio, WAVE und Videogeräte.

Die Automatisierung der Wiedergabe ist auch schnell und einfach. Mit nur einer Funktion und zwei Makros kann eine Anwendung ein MCIWnd-Fenster mit dem entsprechenden Mediengerät erstellen, das Gerät wieder abspielen und sowohl das Gerät als auch das Fenster schließen, wenn die Wiedergabe des Inhalts abgeschlossen ist.

> [!Note]  
> Einige Geräte geben Inhalte wieder, die in Dateien gespeichert sind. Andere Geräte, z. B. CD-Audiogeräte, geben Inhalte wieder, die auf einem anderen Medium gespeichert sind. Aus Gründen der Übersichtlichkeit bezieht sich diese Übersicht auf beide Umstände als "Wiedergabe des Geräts".

 

 

 




