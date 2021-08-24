---
description: Ein allgemeiner Gerätekontext wird zum Zeichnen im Clientbereich des Fensters verwendet.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Allgemeine Anzeigegerätekontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d9de2d9908be735d959a85ca6bdfe99abf7f33489c74175ab2882551393cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105689"
---
# <a name="common-display-device-contexts"></a>Allgemeine Anzeigegerätekontexte

Ein *allgemeiner Gerätekontext* wird zum Zeichnen im Clientbereich des Fensters verwendet. Das System stellt standardmäßig einen allgemeinen Gerätekontext für jedes Fenster bereit, dessen Fensterklasse nicht explizit einen Anzeigegerätekontextstil angibt. Allgemeine Gerätekontexte werden in der Regel mit Fenstern verwendet, die ohne umfangreiche Änderungen an den Gerätekontextattributen gezeichnet werden können. Allgemeine Gerätekontexte sind praktisch, da sie keine zusätzlichen Arbeitsspeicher- oder Systemressourcen erfordern. Sie können jedoch unpraktisch sein, wenn die Anwendung viele Attribute einrichten muss, bevor sie verwendet werden.

Das System ruft alle allgemeinen Gerätekontexte aus dem Anzeigegerätekontextcache ab. Eine Anwendung kann unmittelbar nach dem Erstellen des Fensters einen allgemeinen Gerätekontext abrufen. Da der allgemeine Gerätekontext aus dem Cache stammt, muss die Anwendung den Gerätekontext nach dem Zeichnen immer so schnell wie möglich freigeben. Nachdem der allgemeine Gerätekontext freigegeben wurde, ist er nicht mehr gültig, und die Anwendung darf nicht versuchen, damit zu zeichnen. Zum erneuten Zeichnen muss die Anwendung einen neuen allgemeinen Gerätekontext abrufen und bei jedem Zeichnen im Fenster weiterhin einen gemeinsamen Gerätekontext abrufen und freigeben. Wenn die Anwendung das Gerätekontexthandle mithilfe der [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) abruft, muss sie die [**ReleaseDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-releasedc) verwenden, um das Handle freizugeben. Analog dazu muss die Anwendung für jede [**BeginPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) eine entsprechende [**EndPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-endpaint) verwenden.

Wenn die Anwendung den Gerätekontext abruft, passt das System den Ursprung so an, dass er an der oberen linken Ecke des Clientbereichs ausgerichtet ist. Außerdem wird der Ausschneidebereich so festgelegt, dass die Ausgabe an den Gerätekontext auf den Clientbereich abgeschnitten wird. Jede Ausgabe, die andernfalls außerhalb des Clientbereichs angezeigt wird, wird abgeschnitten. Wenn die Anwendung den allgemeinen Gerätekontext mit [**beginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)abruft, schließt das System auch den Updatebereich in den Clippingbereich ein, um die Ausgabe weiter einzuschränken.

Wenn eine Anwendung einen allgemeinen Gerätekontext freigibt, stellt das System die Standardwerte für die Attribute des Gerätekontexts wieder her. Eine Anwendung, die Attributwerte ändert, muss dies jedes Mal tun, wenn sie einen gemeinsamen Gerätekontext abruft. Durch das Freigeben des Gerätekontexts werden alle Zeichnungsobjekte freigegeben, die die Anwendung möglicherweise darin ausgewählt hat. Daher muss die Anwendung diese Objekte nicht freigeben, bevor sie den Gerätekontext freigibt. In allen Fällen darf eine Anwendung nie davon ausgehen, dass der allgemeine Gerätekontext nach der Veröffentlichung nicht standardmäßige Auswahlmöglichkeiten beibehält.

 

 



