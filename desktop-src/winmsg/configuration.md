---
description: Konfiguration
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Konfiguration (Windows und Meldungen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217822"
---
# <a name="configuration-windows-and-messages"></a>Konfiguration (Windows und Meldungen)

*Anzeigeelemente* sind die Teile eines Fensters und die Anzeige, die auf dem Bildschirm System Anzeige angezeigt wird. *Systemmetriken* sind die Dimensionen verschiedener Anzeigeelemente. Typische Systemmetriken umfassen die Fensterrahmen Breite, die Symbol Höhe usw. Systemmetriken beschreiben auch andere Aspekte des Systems, z. b. ob eine Maus installiert ist, Doppelbyte Zeichen unterstützt werden oder eine Debugversion des Betriebssystems installiert ist. Die [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion Ruft die angegebene Systemmetrik ab.

Anwendungen können auch die Farbe von Fensterelementen, z. b. Menüs, Bild Lauf leisten und Schaltflächen, mithilfe der Funktionen " [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) " und " [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) " abrufen und festlegen.

Die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion Ruft verschiedene Systemattribute ab oder legt Sie fest, z. b. Doppelklick Zeit, Bildschirmschoner-Timeout, Fensterrahmen Breite und Desktop Muster. Wenn eine Anwendung **SystemParametersInfo** verwendet, um einen Parameter festzulegen, erfolgt die Änderung sofort. Diese Funktion ermöglicht es Anwendungen auch, das Benutzerprofil zu aktualisieren, sodass Änderungen am System beim Neustart des Systems beibehalten werden.

 

 
