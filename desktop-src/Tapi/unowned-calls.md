---
description: TapI löscht Anrufe, die von einem Dienstanbieter signalisiert wurden, wenn eine Anwendung nicht als ursprünglicher Besitzer des Anrufs identifiziert werden kann, um zu verhindern, dass nicht im Telefoniesystem keine Anrufe tätigen.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Nichtownierte Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea6fffa2ee65f24d73337980e2a8952157aa5d1000e5c657d75af372f26f00d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991650"
---
# <a name="unowned-calls"></a>Nichtownierte Aufrufe

TapI löscht Anrufe, die von einem Dienstanbieter signalisiert wurden, wenn eine Anwendung nicht als ursprünglicher Besitzer des Anrufs identifiziert werden kann, um zu verhindern, dass nicht im Telefoniesystem keine Anrufe tätigen. In TAPI Version 2.0 und höher ruft TAPI die [**TSPI \_ lineDrop-Funktion**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) auf, um den Aufruf zu verdringen.

Der Dienstanbieter kann im Voraus wissen, ob eine Anwendung verfügbar ist, um den Besitz eines neuen Aufrufs zu übernehmen. TAPI informiert den Dienstanbieter immer über die Medientypen, für die eine Anwendung verfügbar ist, indem die [**\_ TSPI-Funktion lineSetDefaultMediaDetection verwendet**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) wird.

Wenn ein Dienstanbieter beispielsweise feststellt, dass in der Zeile ein aktiver Aufruf im LINEMEDIAMODE INTERACTIVEVOICE-Modus ausgeführt wird, sollte er die Standardmedienerkennung überprüfen, bevor die \_ [**LINE \_ NEWCALL-**](line-newcall.md) und [**LINE \_ CALLSTATE-Nachrichten**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) generiert werden. Wenn die Standardmedienerkennung zeigt, dass keine Anwendung nach einem LINEMEDIAMODE INTERACTIVEVOICE-Aufruf sucht, sollte der Dienstanbieter die Nachrichten nicht senden, da TAPI ihn sofort \_ gelöscht.

 

 
