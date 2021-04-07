---
title: Öffnen und Schließen von Mischungs Geräten
description: Öffnen und Schließen von Mischungs Geräten
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- Multimedia-Audiodatei, Öffnen von Mixer-Geräten
- Audiodatei, Öffnen von Mixer-Geräten
- Audiomixer, öffnen
- Mixer, öffnen
- Multimedia-Audiodaten, schließen von Mischungs Geräten
- Audiodatei, schließen von Mischungs Geräten
- Audiomixer, schließen
- Mixer, schließen
- Öffnen von Mischgerät Geräten
- Schließen von Mischungs Geräten
- Geräte Bezeichner im Vergleich zu Geräte Handles
- audiomischern, Geräte Bezeichner und Geräte Handles
- Mischern, Geräte Bezeichner und Geräte Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038838"
---
# <a name="opening-and-closing-mixer-devices"></a>Öffnen und Schließen von Mischungs Geräten

Wenn Sie ein Mischgerät verwenden möchten, können Sie es entweder einfach verwenden, oder Sie können das Gerät explizit öffnen, bevor Sie es verwenden. Das explizite Öffnen eines Mischgerät bietet zwei wesentliche Vorteile:

-   Dadurch wird sichergestellt, dass dieses Mischungs Gerät weiterhin vorhanden ist.
-   Es ermöglicht Ihnen das Empfangen von Benachrichtigungen über audiozeilen und das Steuern von Änderungen.

Sie können die [**mixeropen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) -Funktion verwenden, um ein Mischgerät explizit zu öffnen. Diese Funktion übernimmt als Parameter einen Geräte Bezeichner, einen Zeiger auf einen Speicherort und andere Werte, die für die einzelnen Gerätetypen eindeutig sind. Der Speicherort wird mit einem Geräte handle gefüllt. Verwenden Sie dieses Geräte handle, um das Open-Mixer-Gerät zu identifizieren, wenn andere audiomischfunktionen aufgerufen werden. Solange ein Handle eines Mixer-Geräts vorhanden ist, ist das Gerät weiterhin im System vorhanden. Wenn eine Konfigurationsänderung für das Mischgerät erfolgt und es nicht explizit geöffnet wurde, kann die Anwendung plötzlich nicht mehr darauf zugreifen.

> [!Note]  
> Der Unterschied zwischen Geräte bezeichatoren und Geräte Handles ist wichtig. Geräte Handles werden zurückgegeben, wenn Sie einen Gerätetreiber mithilfe von **mixeropen** öffnen. Geräte Bezeichner werden implizit von der Anzahl von Geräten, die in einem System vorhanden sind, bestimmt. Diese Zahl wird mithilfe der Funktion [**mixergetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) abgerufen.

 

Sie können die [**mixerclose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) -Funktion verwenden, um ein Mischgerät zu schließen. Sie sollten das Gerät schließen, nachdem Sie es verwendet haben.

 

 