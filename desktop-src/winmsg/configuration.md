---
description: In diesem Referenzabschnitt wird die Konfiguration für Windows und Meldungen beschrieben. Erfahren Sie mehr über Anzeigeelemente und Systemmetriken.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Konfiguration (Windows und Meldungen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406343"
---
# <a name="configuration-windows-and-messages"></a>Konfiguration (Windows und Meldungen)

*Anzeigeelemente* sind die Teile eines Fensters und die Anzeige, die auf dem Systemanzeigebildschirm angezeigt werden. *Systemmetriken* sind die Dimensionen verschiedener Anzeigeelemente. Typische Systemmetriken sind die Fensterrahmenbreite, die Symbolhöhe usw. Systemmetriken beschreiben auch andere Aspekte des Systems, z. B. ob eine Maus installiert ist, Doppel-Byte-Zeichen unterstützt werden oder eine Debugversion des Betriebssystems installiert ist. Die [**GetSystemMetrics-Funktion**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) ruft die angegebene Systemmetrik ab.

Anwendungen können auch die Farbe von Fensterelementen wie Menüs, Scrollleisten und Schaltflächen abrufen und festlegen, indem sie die Funktionen [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) bzw. [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) verwenden.

Die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) ruft verschiedene Systemattribute ab oder legt diese fest, z. B. Doppelklickzeit, Time-Out für Bildschirmschoner, Fensterrahmenbreite und Desktopmuster. Wenn eine Anwendung **SystemParametersInfo** verwendet, um einen Parameter festzulegen, erfolgt die Änderung sofort. Mit dieser Funktion können Anwendungen auch das Benutzerprofil aktualisieren, sodass Änderungen am System beibehalten werden, wenn das System neu gestartet wird.

 

 
