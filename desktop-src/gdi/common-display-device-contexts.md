---
description: Ein gemeinsamer Gerätekontext wird zum Zeichnen im Client Bereich des Fensters verwendet.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Gängige Anzeige von Geräte Kontexten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890b0235784ec1ed11c8ce3a553244629a008d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959311"
---
# <a name="common-display-device-contexts"></a>Gängige Anzeige von Geräte Kontexten

Ein *gemeinsamer Gerätekontext* wird zum Zeichnen im Client Bereich des Fensters verwendet. Das System stellt standardmäßig einen gemeinsamen Gerätekontext für jedes Fenster bereit, dessen Fenster Klasse nicht explizit einen Kontext Stil des Anzeige Geräts angibt. Häufig verwendete Geräte Kontexte werden in der Regel mit Fenstern verwendet, die ohne umfassende Änderungen an den Gerätekontext Attributen gezeichnet werden können. Häufige Geräte Kontexte sind praktisch, da Sie keine zusätzlichen Arbeitsspeicher-oder Systemressourcen benötigen. Sie können jedoch unpraktisch sein, wenn die Anwendung viele Attribute einrichten muss, bevor Sie Sie verwenden.

Das System ruft alle gängigen Geräte Kontexte aus dem Kontext Cache des Anzeige Geräts ab. Eine Anwendung kann einen gemeinsamen Gerätekontext sofort nach der Erstellung des Fensters abrufen. Da der gemeinsame Gerätekontext vom Cache ist, muss die Anwendung den Gerätekontext nach dem Zeichnen immer so bald wie möglich freigeben. Nachdem der gemeinsame Gerätekontext freigegeben wurde, ist er nicht mehr gültig, und die Anwendung darf nicht versuchen, ihn zu zeichnen. Zum erneuten zeichnen muss die Anwendung einen neuen gemeinsamen Gerätekontext abrufen und weiterhin einen gemeinsamen Gerätekontext abrufen und freigeben, wenn er sich im Fenster zeichnet. Wenn die Anwendung das Gerätekontext Handle mithilfe der [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion abruft, muss Sie die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion verwenden, um das Handle freizugeben. Ebenso muss die Anwendung für jede [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -Funktion eine entsprechende [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktion verwenden.

Wenn die Anwendung den Gerätekontext abruft, passt das System den Ursprung so an, dass er sich an der oberen linken Ecke des Client Bereichs anpasst. Außerdem wird der Clippingbereich festgelegt, sodass die Ausgabe in den Gerätekontext auf den Client Bereich zugeschnitten wird. Alle Ausgaben, die andernfalls außerhalb des Client Bereichs angezeigt werden, werden abgeschnitten. Wenn die Anwendung den gemeinsamen Gerätekontext mithilfe von [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)abruft, schließt das System auch den Aktualisierungs Bereich in den Clippingbereich ein, um die Ausgabe weiter einzuschränken.

Wenn eine Anwendung einen gemeinsamen Gerätekontext freigibt, stellt das System die Standardwerte für die Attribute des Geräte Kontexts wieder her. Eine Anwendung, die Attributwerte ändert, muss dies jedes Mal durchführen, wenn ein gemeinsamer Gerätekontext abgerufen wird. Durch das Freigeben des Geräte Kontexts werden alle Zeichnungsobjekte freigegeben, die von der Anwendung möglicherweise ausgewählt wurden, sodass die Anwendung diese Objekte vor dem Freigeben des Geräte Kontexts nicht freigeben muss. In allen Fällen muss eine Anwendung niemals davon ausgehen, dass der gemeinsame Gerätekontext nach der Freigabe nicht die Standardauswahl beibehält.

 

 



