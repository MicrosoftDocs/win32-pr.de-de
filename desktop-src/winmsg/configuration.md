---
description: In diesem Referenzabschnitt wird die Konfiguration für Windows und Nachrichten beschrieben. Erfahren Sie mehr über Anzeigeelemente und Systemmetriken.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Konfiguration (Windows und Nachrichten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5c910fd9614d4d0e8fe9f6ba38d9dd59a0fd5649e836c3629427cde5d8617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028468"
---
# <a name="configuration-windows-and-messages"></a>Konfiguration (Windows und Nachrichten)

*Anzeigeelemente* sind die Teile eines Fensters und die Anzeige, die auf dem Systemanzeigebildschirm angezeigt werden. *Systemmetriken* sind die Dimensionen verschiedener Anzeigeelemente. Typische Systemmetriken sind die Fensterrahmenbreite, symbolhöhe und so weiter. Systemmetriken beschreiben auch andere Aspekte des Systems, z. B. ob eine Maus installiert, Doppel bytezeichen unterstützt oder eine Debugversion des Betriebssystems installiert ist. Die [**GetSystemMetrics-Funktion**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) ruft die angegebene Systemmetrik ab.

Anwendungen können die Farbe von Fensterelementen wie Menüs, Scrollleisten und Schaltflächen auch mithilfe der [**Funktionen GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) bzw. [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) abrufen und festlegen.

Die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) ruft verschiedene Systemattribute ab oder legt sie fest, z. B. Doppelklickzeit, Time out des Bildschirmschoners, Breite des Fensterrahmens und Desktopmuster. Wenn eine Anwendung **SystemParametersInfo zum** Festlegen eines Parameters verwendet, erfolgt die Änderung sofort. Mit dieser Funktion können Anwendungen auch das Benutzerprofil aktualisieren, sodass Änderungen am System beim Neustart des Systems beibehalten werden.

 

 
