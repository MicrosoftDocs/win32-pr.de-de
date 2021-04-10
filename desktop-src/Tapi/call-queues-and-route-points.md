---
description: Eine Aufruf Warteschlange oder ein Routen Punkt ist eine spezielle Adresse innerhalb des Schalters, bei der Aufrufe vorübergehend Ausstehende Aktionen ausgeführt werden.
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: Callwarteschlangen und Routenpunkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66895101b72ca8e16810d3766edf897efcfedddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215872"
---
# <a name="call-queues-and-route-points"></a>Callwarteschlangen und Routenpunkte

Eine Aufruf Warteschlange oder ein Routen Punkt ist eine spezielle Adresse innerhalb des Schalters, bei der Aufrufe vorübergehend Ausstehende Aktionen ausgeführt werden. Dieses Merkmal wird durch die Bits lineaddrcapflags \_ Queue und lineaddrcapflags \_ Routepoint im Member **dwaddrcapflags** in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)dargestellt. Alle Aufrufe, die für eine solche Adresse angezeigt werden, warten von der Anwendung auf Aktionen, und es können Standard Aktionen stattfinden (z. b. Übertragung an einen Agent oder einen trunk), wenn die Anwendung innerhalb eines definierten Zeitraums keine Aktion durchführt. Die Anwendung muss vom Systemadministrator konfiguriert werden, damit Sie weiß, welche Aktionen in Bezug auf Aufrufe für die einzelnen Warteschlangen-oder Routen Punkt Adressen ausgeführt werden sollten und wie viel Zeit für die Entscheidung für die auszuführende Aktion verfügbar ist.

Anwendungen können die Anzahl der Aufrufe ermitteln, die in einer Warteschlange oder einem Routen Punkt mithilfe von [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)ausstehend sind. Die [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) -Funktion kann verwendet werden, um Informationen wie das Aufrufen der ID, die ID, den eingehenden oder ausgehenden Ursprung usw. abzurufen und von der Anwendung zum Treffen von Entscheidungen bei der Anruf Behandlung zu verwenden. Aufrufe können umgeleitet, Blind übertragen, gelöscht usw. oder nur automatisch aus der Warteschlange an ein Ziel übergeben werden. Ein-Rückruf wird an linecallstate \_ getrennt, wenn er abgebrochen wurde. Aufrufe wechseln in den *Leerlauf* , wenn Sie die Warteschlange verlassen. **linegetcallinfo** kann verwendet werden, um den Umleitungs Bezeichner zu lesen und zu bestimmen, wo Sie übertragen wurden.

Bei manchen Switches können Aufrufe in einer Warteschlange oder in der Warteschlange eine bestimmte Behandlung erhalten, wie z. b. Stille, Rollback, ausgelastete Signale, Musik oder lauschen auf eine aufgezeichnete Ankündigung. Die [**linesetcalltreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) -Funktion ermöglicht der Anwendung die Steuerung der Behandlung. Die Struktur, die durch die Member **dwcalltreatmentlistsize** und **dwcalltreatmentlistoffset** in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) begrenzt ist, ermöglicht Anwendungen, die unterstützten Behandlungen zu bestimmen. Der **dwcalltreatment** -Member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) zeigt die aktuelle Behandlung an, und eine [**Zeile \_ CallInfo**](line-callinfo.md) -Meldung mit linecallinfostate- \_ Behandlung gibt an, wann sich diese Änderung ändert. Das linecallfeature \_ settreement-Bit im **dwcallfeatures** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) zeigt an, wann die Anwendung berechtigt ist, die Verarbeitung zu ändern. Der linecalltreatment- \_ Satz von Konstanten definiert einen begrenzten Satz vordefinierter aufrufsbehandlungen. Dienstanbieter können vieles mehr definieren.

 

 



