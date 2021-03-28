---
description: Mit einem privaten Gerätekontext kann eine Anwendung das Abrufen und Initialisieren eines Anzeigegeräte Kontexts vermeiden, wenn die Anwendung in einem Fenster gezeichnet werden muss.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Private Anzeigegeräte Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451dbd3c0a232610026740d0ea0fa817ea2034b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528286"
---
# <a name="private-display-device-contexts"></a>Private Anzeigegeräte Kontexte

*Mit einem privaten Gerätekontext* kann eine Anwendung das Abrufen und Initialisieren eines Anzeigegeräte Kontexts vermeiden, wenn die Anwendung in einem Fenster gezeichnet werden muss. Private Geräte Kontexte sind für Windows nützlich, bei denen viele Änderungen an den Werten der Attribute des Geräte Kontexts erforderlich sind, um Sie für das Zeichnen vorzubereiten. Private Geräte Kontexte verkürzen die Zeit, die zum Vorbereiten des Geräte Kontexts erforderlich ist, und damit die Zeit, die zum Durchführen der Zeichnung im Fenster benötigt wird.

Eine Anwendung weist das System an, einen privaten Gerätekontext für ein Fenster zu erstellen, indem der CS- \_ owndc-Stil in der Window-Klasse angegeben wird. Jedes Mal, wenn ein neues Fenster erstellt wird, das zur-Klasse gehört, erstellt das System einen eindeutigen privaten Gerätekontext. Anfänglich hat der private Gerätekontext dieselben Standardwerte für Attribute als gemeinsamer Gerätekontext, aber die Anwendung kann diese jederzeit ändern. Das System behält Änderungen am Gerätekontext während der Lebensdauer des Fensters oder bis zur Änderung der Anwendung bei.

Eine Anwendung kann ein Handle für den privaten Gerätekontext abrufen, indem die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion nach der Erstellung des Fensters verwendet wird. Die Anwendung muss das Handle nur einmal abrufen. Danach kann das Handle beliebig oft beibehalten und verwendet werden. Da ein privater Gerätekontext nicht zum Anzeigegeräte Kontext Cache gehört, muss eine Anwendung den Gerätekontext nie mithilfe der [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion freigeben.

Das System passt den Gerätekontext automatisch an, um Änderungen am Fenster widerzuspiegeln, z. b. verschieben oder anpassen. Dadurch wird sichergestellt, dass überlappende Fenster immer ordnungsgemäß abgeschnitten werden. Das heißt, für die Anwendung ist keine Aktion erforderlich, um das Clipping sicherzustellen. Das System ändert den Gerätekontext jedoch nicht, um den Aktualisierungs Bereich einzubeziehen. Daher muss die Anwendung bei der Verarbeitung einer WM-Zeichnungs Nachricht den Update Bereich einschließen, indem Sie entweder [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) aufrufen oder den Update Bereich abrufen und mit dem aktuellen Clippingbereich interzieren. [**\_**](wm-paint.md) Wenn die Anwendung nicht **BeginPaint** aufruft, muss Sie den Aktualisierungs Bereich mithilfe der [**validaterierten**](/windows/desktop/api/Winuser/nf-winuser-validaterect) oder [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) -Funktion explizit validieren. Wenn die Anwendung den Update Bereich nicht überprüft, empfängt das Fenster eine unendliche Reihe von **WM \_ Paint** -Meldungen.

Da [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) die Einfügemarke verbirgt, wenn ein Fenster es anzeigt, sollte eine Anwendung, die **BeginPaint** aufruft, auch die [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktion aufrufen, um die Einfügemarke wiederherzustellen. **Endpaint** wirkt sich nicht auf einen privaten Gerätekontext aus.

Obwohl ein privater Gerätekontext praktisch verwendet werden kann, ist er in Bezug auf Systemressourcen Speicher intensiv, wobei 800 oder mehr Bytes gespeichert werden müssen. Der Kontext privater Geräte wird empfohlen, wenn die Speicherkosten überwiegen.

Das System schließt den privaten Gerätekontext ein, wenn die " [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) "-Meldung an die Anwendung gesendet wird. Die aktuelle Auswahl des privaten Geräte Kontexts, einschließlich des Kartenmodus, ist wirksam, wenn die Anwendung oder das System diese Nachrichten verarbeitet. Um unerwünschte Auswirkungen zu vermeiden, verwendet das System logische Koordinaten, wenn der Hintergrund gelöscht wird. Beispielsweise wird die [**getclipbox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) -Funktion verwendet, um die logischen Koordinaten des Bereichs abzurufen, der gelöscht werden soll, und diese Koordinaten an die [**fillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect) -Funktion weitergeleitet. Anwendungen, die diese Nachrichten verarbeiten, können ähnliche Techniken verwenden.

Eine Anwendung kann die [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion verwenden, um zu erzwingen, dass das System einen gemeinsamen Gerätekontext für das Fenster mit privatem Gerätekontext zurückgibt. Dies ist nützlich, um schnell Berührungen für ein Fenster auszuführen, ohne die aktuellen Werte der Attribute des privaten Geräte Kontexts zu ändern.

 

 
