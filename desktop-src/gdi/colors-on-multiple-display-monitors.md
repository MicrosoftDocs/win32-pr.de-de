---
description: Jeder Monitor kann über eine eigene Farbtiefe verfügen.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Farben auf mehreren Anzeigemonitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd799599f3818ad002ee8a0fa1e9478f383b3052dd3a2cc3b8a40843e431b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115320"
---
# <a name="colors-on-multiple-display-monitors"></a>Farben auf mehreren Anzeigemonitoren

Jeder Monitor kann über eine eigene Farbtiefe verfügen. Das System passt Farben automatisch an, wenn Fenster sich über Monitore mit unterschiedlichen Farbtiefe bewegen. Im Allgemeinen führt dies zu guten Ergebnissen. Dies ist jedoch nicht immer optimal. Informationen zur Nutzung der Farbfunktionen verschiedener Monitore finden Sie im folgenden Abschnitt [Zeichnen auf mehreren Anzeigemonitoren.](painting-on-multiple-display-monitors.md)

Um zu bestimmen, ob alle Monitore das gleiche Farbformat aufweisen, rufen [**Sie GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ SAMEDISPLAYFORMAT auf.

Wenn der primäre Monitor palettisiert ist, funktionieren [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) genauso wie zuvor, aber auf allen Monitoren. Darüber hinaus werden die Paletten aller palettisierten Geräte synchronisiert. Wenn der primäre Monitor nicht palettisiert ist, **wählen SelectPalette** und **RealizePalette** die Palette im Hintergrund aus, und palettierte Geräte werden nicht synchronisiert.

 

 
