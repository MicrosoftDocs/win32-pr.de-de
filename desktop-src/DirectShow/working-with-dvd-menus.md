---
description: Arbeiten mit DVD-Menüs
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Arbeiten mit DVD-Menüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351177"
---
# <a name="working-with-dvd-menus"></a>Arbeiten mit DVD-Menüs

Der DVD-Navigator kann ein Menü anzeigen, wenn der Benutzer eine Schaltfläche aktiviert, oder wenn der Navigator die erste Wiedergabe Domäne eingibt. Um ein Menü Programm gesteuert anzuzeigen, müssen Sie die [**IDvdControl2:: showmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) -Methode aufzurufen.

Es gibt mehrere Möglichkeiten, Menü Schaltflächen Programm gesteuert auszuwählen:

-   Um eine Schaltfläche nach Nummer auszuwählen, nennen Sie [**IDvdControl2:: selectbutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). Die Schaltflächen sind von 1 bis 36 nummeriert. Die [**IDvdInfo2:: getcurrentbutton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) -Methode gibt die Anzahl der verfügbaren Schaltflächen zurück.
-   Um eine Schaltfläche in Relation zur Position der aktuell ausgewählten Schaltfläche auszuwählen, nennen Sie [**IDvdControl2:: selectrelativebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). Sie können eine Schaltfläche in der Richtung oben, nach unten, Links oder rechts auswählen.
-   Um eine Schaltfläche anhand ihrer Koordinaten innerhalb des Fensters auszuwählen, nennen Sie [**IDvdControl2:: selectatposition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Diese Methode nimmt (x, y)-Koordinaten in Relation zum Client Bereich des Videofensters. (Für den fensterlosen Modus ist dies das Anwendungsfenster.) Wenn an dieser Stelle keine Schaltfläche vorhanden ist, gibt die Methode VFW \_ E \_ DVD \_ No \_ Button zurück.

Außerdem gibt es mehrere Möglichkeiten, eine Schaltfläche zu aktivieren:

-   Um eine Schaltfläche nach Zahl zu aktivieren, müssen Sie [**IDvdControl2:: selectandactivatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)aufrufen.
-   Um eine Schaltfläche über Ihre Koordinaten zu aktivieren, müssen Sie [**IDvdControl2:: activateatposition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition)aufrufen.
-   Um die Schaltfläche zu aktivieren, die derzeit ausgewählt ist, aufrufen Sie [**IDvdControl2:: activatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Wenn keine Schaltfläche ausgewählt ist, gibt die Methode VFW \_ E \_ DVD \_ No \_ Button zurück.

Beachten Sie, dass durch das Auswählen einer Schaltfläche nur die Rahmen hervorgehoben werden. Damit der zugeordnete Befehl ausgelöst wird, muss die Schaltfläche aktiviert werden. Die programmgesteuerte Aktivierung einer Schaltfläche kann auf verschiedene Weise erfolgen, aber die Schaltfläche muss immer ausgewählt werden, bevor Sie aktiviert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



