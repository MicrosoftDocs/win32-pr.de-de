---
description: Die folgenden Funktionen bieten Unterstützung für mehrere Monitore.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funktionen für mehrere Anzeigemonitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e35ab6fef353f793257721077074271915a3628859471a2f5d89694f6d47440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779140"
---
# <a name="multiple-display-monitors-functions"></a>Funktionen für mehrere Anzeigemonitore

Die folgenden Funktionen bieten Unterstützung für mehrere Monitore.



| Funktion                                           | Beschreibung                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Listet Anzeigemonitore auf, die einen Bereich überschneiden, der durch die Schnittmenge eines angegebenen Ausschneiderechtecks und den sichtbaren Bereich eines Gerätekontexts gebildet wird. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Ruft Informationen zu einem Anzeigemonitor ab.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Eine anwendungsdefinierte Rückruffunktion, die von der [**EnumDisplayMonitors-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) aufgerufen wird.                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Ruft ein Handle für den Anzeigemonitor ab, der einen angegebenen Punkt enthält.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Ruft ein Handle für den Anzeigemonitor ab, der den größten Schnittpunkt mit einem angegebenen Rechteck hat.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Ruft ein Handle für den Anzeigemonitor ab, der den größten Schnittpunkt mit dem umgrenzten Rechteck eines angegebenen Fensters hat.                       |



 

 

 



