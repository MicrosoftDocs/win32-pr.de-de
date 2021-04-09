---
title: Rendern von Kontextfunktionen
description: Fünf WGL-Funktionen verwalten renderingkontexte, wie in der folgenden Tabelle beschrieben.
ms.assetid: e03ec03d-2a85-49de-a2be-fe81a5ec5f7f
keywords:
- WGL-Funktionen, renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8d3a8ea0333154d3145711829ab23e262fa485
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949074"
---
# <a name="rendering-context-functions"></a>Rendern von Kontextfunktionen

Fünf WGL-Funktionen verwalten renderingkontexte, wie in der folgenden Tabelle beschrieben.



| WGL-Funktion                                         | BESCHREIBUNG                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)         | Erstellt einen neuen renderingkontext.                                                             |
| [**Wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)             | Legt den aktuellen renderingkontext eines Threads fest.                                                   |
| [**Wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) | Ruft ein Handle für den aktuellen renderingkontext eines Threads ab.                                    |
| [**Wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)           | Ruft ein Handle für den Gerätekontext ab, der dem aktuellen renderingkontext eines Threads zugeordnet ist. |
| [**Wgldeletecontext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)         | Löscht einen renderingkontext.                                                                 |



 

Die [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) -Funktion nimmt ein Gerätekontext Handle als Parameter an und gibt ein Rendering-Kontext Handle zurück. Der erstellte renderingkontext eignet sich zum Zeichnen auf dem Gerät, auf das vom Gerätekontext handle verwiesen wird. Das Pixel Format ist insbesondere mit dem Pixel Format des Geräte Kontexts identisch. Nachdem Sie einen renderingkontext erstellt haben, können Sie den Gerätekontext freigeben oder verwerfen. Weitere Informationen zum Erstellen, abrufen, freigeben und verwerfen eines Geräte Kontexts finden Sie unter [Geräte Kontexte](/windows/desktop/gdi/device-contexts) .

> [!Note]  
> Der an [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) gesendete Gerätekontext muss ein Anzeigegeräte Kontext, ein Speichergeräte Kontext oder ein Farbdrucker-Gerätekontext sein, der vier oder mehr Bits pro Pixel verwendet. Der Gerätekontext darf kein monochrome Drucker Gerätekontext sein.

 

Die [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) -Funktion nimmt ein Rendering-Kontext Handle und ein Gerätekontext Handle als Parameter an. Alle nachfolgenden OpenGL-Aufrufe durch den Thread werden über diesen renderingkontext durchgeführt und auf dem Gerät gezeichnet, auf das von diesem Gerätekontext verwiesen wird. Beim Erstellen des renderingkontexts muss der Gerätekontext nicht identisch sein, da er nicht identisch ist, da **er sich auf** demselben Gerät befinden muss und das gleiche Pixel Format aufweisen muss. Durch den **wglmakecurrent** -Aufrufe wird eine Zuordnung zwischen dem angegebenen renderingkontext und dem Gerätekontext erstellt. Sie können den Gerätekontext, der einem aktuellen renderingkontext zugeordnet ist, erst freigeben oder verwerfen, wenn der renderingkontext nicht aktuell ist.

Wenn ein Thread über einen aktuellen renderingkontext verfügt, kann er OpenGL-Grafik Aufrufe durchführen. Alle Aufrufe müssen einen renderingkontext passieren. Wenn Sie OpenGL-Grafik Aufrufe von einem Thread durchführen, der keinen aktuellen renderingkontext besitzt, geschieht nichts.

Die [**wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) -Funktion nimmt keine Parameter an und gibt ein Handle für den aktuellen renderingkontext des aufrufenden Threads zurück. Wenn der Thread über keinen aktuellen renderingkontext verfügt, ist der Rückgabewert **null**.

Wenn Sie ein Handle für den Gerätekontext abrufen, der dem aktuellen renderingkontext eines Threads zugeordnet ist, indem Sie [**wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)aufrufen, wird die Zuordnung erstellt, wenn ein renderingkontext aktuell gemacht wird.

Sie können die Zuordnung zwischen einem aktuellen renderingkontext und einem Thread unterbrechen, indem Sie [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) mit einem der beiden Handles aufrufen:

-   Ein **null** -Rendering-Kontext Handle
-   Ein Handle, das nicht die ursprünglich aufgerufene ist.

Nachdem [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) aufgerufen wurde und der Parameter für den Rendering-Kontext Handle auf **null** festgelegt wurde, hat der aufrufenden Thread keinen aktuellen renderingkontext. Der renderingkontext wird von seiner Verbindung mit dem Thread freigegeben, und die Zuordnung des renderkontexts zu einem Gerätekontext wird beendet. OpenGL Leert alle Zeichnungs Befehle und gibt möglicherweise einige Ressourcen frei. Bis zum nächsten Aufruf von **wglmakecurrent** wird keine OpenGL-Zeichnung durchgeführt, da der Thread keine OpenGL-Grafik Aufrufe durchführen kann, bis ein aktueller renderingkontext wieder hergestellt wird.

Die zweite Möglichkeit, die Zuordnung zwischen einem renderingkontext und einem Thread zu unterbrechen, besteht darin, **wglmakecurrent** mit einem anderen renderingkontext aufzurufen. Nach einem solchen Aufruf hat der aufrufende Thread einen neuen aktuellen renderingkontext, der vorherige aktuelle renderingkontext wird von der Verbindung mit dem Thread freigegeben, und die Zuordnung des früheren aktuellen renderingkontexts zu einem Gerätekontext wird beendet.

Die [**wgldeletecontext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) -Funktion nimmt einen einzelnen Parameter an, das Handle für den renderingkontext, der gelöscht werden soll. Machen Sie vor dem Aufrufen von **wgldeletecontext** den renderingkontext nicht aktuell, indem Sie [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)aufrufen und den zugehörigen Gerätekontext löschen oder freigeben, indem Sie [DeleteDC](/windows/desktop/api/wingdi/nf-wingdi-deletedc) oder [ReleaseDC](/windows/desktop/api/winuser/nf-winuser-releasedc) nach Bedarf aufrufen.

Es ist ein Fehler, wenn ein Thread einen renderingkontext löscht, der der aktuelle renderingkontext eines anderen Threads ist. Wenn es sich bei einem renderingkontext jedoch um den aktuellen renderingkontext des aufrufenden Threads handelt, leert **wgldeletecontext** alle OpenGL-Zeichenbefehle und macht den renderingkontext vor dem Löschen nicht mehr aktuell. In diesem **Fall muss der** Programmierer den zugehörigen Gerätekontext löschen oder freigeben, damit ein renderingkontext nicht aktuell ist.

 

 