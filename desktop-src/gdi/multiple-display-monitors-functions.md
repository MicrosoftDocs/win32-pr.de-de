---
description: Die folgenden Funktionen bieten Unterstützung für mehrere Monitore.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funktionen mit mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978536"
---
# <a name="multiple-display-monitors-functions"></a>Funktionen mit mehreren Anzeige Monitoren

Die folgenden Funktionen bieten Unterstützung für mehrere Monitore.



| Funktion                                           | BESCHREIBUNG                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Listet Anzeige Monitore auf, die einen Bereich überschneiden, der durch die Schnittmenge eines angegebenen clippingrechtecks und den sichtbaren Bereich eines Geräte Kontexts gebildet wird. |
| [**Getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Ruft Informationen zu einem Anzeige Monitor ab.                                                                                                               |
| [**Monitorenumschlag**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Eine von der Funktion [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) aufgerufene Anwendungs definierte Rückruffunktion.                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Ruft ein Handle für den Anzeige Monitor ab, der einen angegebenen Punkt enthält.                                                                                   |
| [**Monitorfromrect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Ruft ein Handle für den Anzeige Monitor mit dem größten Bereich der Schnittmenge mit einem angegebenen Rechteck ab.                                              |
| [**Monitorfromwindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Ruft ein Handle für den Anzeige Monitor mit dem größten Bereich der Schnittmenge mit dem umgebenden Rechteck eines angegebenen Fensters ab.                       |



 

 

 



