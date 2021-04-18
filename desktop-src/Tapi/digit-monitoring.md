---
description: Die Ziffern Überwachung überwacht den-Befehl für Ziffern.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Ziffern Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341199"
---
# <a name="digit-monitoring"></a>Ziffern Überwachung

Die Ziffern Überwachung überwacht den-Befehl für Ziffern. TAPI ermöglicht, dass Ziffern gemäß zwei Methoden (Ziffern Modi) signalisiert werden:

-   Pulsziffern werden als Pulse oder als Dreh Sequenzen signalisiert. Zur Erkennung werden diese Pulse selbst als nicht mehr als Sequenzen von hörbaren Klicks angezeigt. Gültige Pulse-Ziffern sind "0" bis "9".
-   DTMF-Ziffern werden als DTMF-Töne (Dual Ton Multiple Frequency) signalisiert. Gültige DTMF-Ziffern sind "0" bis "9", "A". "B", "C", "d", " \* " und " \# ". Sowohl der anfangs-als auch der Down-Rand der DTMF-Ziffern können überwacht werden.

Eine Anwendung kann die Ziffern Überwachung für einen angegebenen-Befehl mit [**linemonitordigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)aktivieren bzw. deaktivieren. Wenn die Ziffern Überwachung aktiviert ist, bewirken erkannte Ziffern, dass die Anwendung mit der [**Zeile " \_ monitordigits**](line-monitordigits.md) " benachrichtigt wird. Diese Meldung enthält das Telefon handle, für das die Ziffer erkannt wurde, sowie den Ziffern-und Ziffern Modus. Der Bereich der Ziffern Überwachung wird durch die Lebensdauer des Aufrufes gebunden. Die Ziffern Überwachung bei einem-Rückruf wird beendet, sobald der-Rückruf die Verbindung *trennt oder in* den *Leerlauf* wechselt.

 

 



