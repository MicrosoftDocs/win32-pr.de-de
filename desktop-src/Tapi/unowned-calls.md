---
description: Um zu verhindern, dass sich Anrufe im Telefoniesystem befinden, löscht TAPI die von einem Dienstanbieter signalisierten Aufrufe, wenn eine Anwendung nicht als anfänglicher Besitzer des Aufrufs identifiziert werden kann.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Nicht im Besitz befindliche Anrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349027"
---
# <a name="unowned-calls"></a>Nicht im Besitz befindliche Anrufe

Um zu verhindern, dass sich Anrufe im Telefoniesystem befinden, löscht TAPI die von einem Dienstanbieter signalisierten Aufrufe, wenn eine Anwendung nicht als anfänglicher Besitzer des Aufrufs identifiziert werden kann. In TAPI, Version 2,0 und höher, ruft TAPI die [**TSPI-Funktion \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) auf, um den Aufruf zu löschen.

Der Dienstanbieter kann im Voraus wissen, ob eine Anwendung verfügbar ist, um den Besitz eines neuen Aufrufes zu übernehmen. TAPI informiert den Dienstanbieter stets über die Medientypen, für die eine Anwendung verfügbar ist, indem er die Funktion [**TSPI \_ linesetdefaultmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) verwendet.

Wenn ein Dienstanbieter z. b. feststellt, dass ein aktiver Aufruf in der Zeile mit linemediamode \_ interactivevoice Mode vorhanden ist, sollte die Standard Medien Erkennung überprüft werden, bevor die [**Zeilen- \_ newcall-**](line-newcall.md) und die [**line \_ CallState**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) -Nachricht erzeugt werden. Wenn die Standard Medien Erkennung anzeigt, dass keine Anwendung nach einem linemediamode \_ interactivevoice-Befehl sucht, sollte der Dienstanbieter die Nachrichten nicht senden, da TAPI ihn sofort löscht.

 

 
