---
description: MSWebDVD-Ereignisse
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: MSWebDVD-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a37eda7b8c2ebafc704d96195cc9e92e70fbd9d8bfda4aa7c971cd890e41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042710"
---
# <a name="mswebdvd-events"></a>MSWebDVD-Ereignisse

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

> [!Note]  
> Diese API ist veraltet. Informationen zur Wiedergabe und Navigation von DVD in DirectShow finden Sie unter [DVD-Anwendungen](dvd-applications.md).

 

Das Microsoft® ActiveX®-Steuerelement MSWebDVD benachrichtigt Ihre Anwendung, wenn verschiedene Arten von internen Ereignissen auftreten oder bestimmte Informationen auf dem Datenträger gefunden werden.

Die meisten Ereignisse beziehen sich auf UOP-Steuerelemente (User Operation). DVD-Autoren können den Datenträger so codieren, dass jeder DVD-Befehl (z. B. **PlayForwards,** **Pause,** **ShowMenu** und so weiter) jederzeit deaktiviert werden kann. Die meisten Datenträger ermöglichen es Benutzern beispielsweise nicht, schnell vorwärts zu gehen oder ein Menü zu zeigen, während die WARNUNG abspielt. Nachdem die Warnung beendet wurde, lässt der Datenträger diese Vorgänge zu. Durch die Behandlung der UOP-Ereignisse kann Ihre Anwendung ihre Benutzeroberfläche aktualisieren, um dem Benutzer zu zeigen, welche Befehle derzeit vom Datenträger zugelassen sind. Die gängigste Methode besteht in der Deaktivierung einer Schaltfläche. Wenn Ihre Anwendung beispielsweise ein PlayForwards-Ereignis empfangen hat, bei dem **bEnabled** auf **FALSE** festgelegt ist, können Sie die Wiedergabeschaltfläche deaktivieren. Wenn das Ereignis empfangen wurde und **bEnabled** auf **TRUE** festgelegt ist, können Sie die Schaltfläche erneut aktivieren.

Es gibt drei Ereignisse, die sich nicht auf UOP-Steuerelemente beziehen. Das **DVDNotify-Ereignis** benachrichtigt Ihre Anwendung über viele verschiedene Arten von DVD-bezogenen Ereignissen, die im *EventCode-Parameter identifiziert* werden. Einige Ereignisse enthalten zusätzliche Informationen in den *Parametern Param1* *und Param2.* Das **ReadyStateChange-Ereignis** benachrichtigt Ihre Anwendung über Änderungen in der Eigenschaft MSWebDVD ReadyState, bei der es sich um eine Eigenschaft handelt, die allen steuerelementen ActiveX ist. Das **UpdateOverlay-Ereignis** wird nur dann an Anwendungen gesendet, wenn sie MSWebDVD im fensterlosen Modus hosten. Anwendungen müssen nur dann auf dieses Ereignis reagieren, wenn sie unverankerte Schaltflächen über dem Videorechteck im Vollbildmodus anzeigen.



| Ereignis                                                                  | BESCHREIBUNG                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Wird gesendet, wenn der Datenträger das Ändern des Winkels aktiviert oder deaktiviert.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Wird gesendet, wenn der Datenträger das Ändern des Audiodatenstroms aktiviert oder deaktiviert.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Wird gesendet, **wenn der ChangeCurrentSubpictureStream-Befehl** aktiviert oder deaktiviert wurde. |
| [**DVDNotify**](dvdnotify.md)                                         | Benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Datenträgeranweisungen.           |
| [**PauseOn**](pauseon.md)                                             | Wird gesendet, wenn **der Befehl** Anhalten aktiviert oder deaktiviert wurde.                         |
| [**PlayAtTime**](playattime.md)                                       | Wird gesendet, **wenn der PlayAtTime-Befehl** aktiviert oder deaktiviert wurde.                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Wird gesendet, **wenn der Befehl PlayAtTimeInTitle** aktiviert oder deaktiviert wurde.             |
| [**PlayBackwards**](playbackwards.md)                                 | Wird gesendet, **wenn der PlayBackwards-Befehl** aktiviert oder deaktiviert wurde.                 |
| [**PlayChapter**](playchapter.md)                                     | Wird gesendet, **wenn der PlayChapter-Befehl** aktiviert oder deaktiviert wurde.                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Wird gesendet, **wenn der Befehl PlayChapterInTitle** aktiviert oder deaktiviert wurde.            |
| [**PlayForwards**](playforwards.md)                                   | Wird gesendet, **wenn der PlayForwards-Befehl** aktiviert oder deaktiviert wurde.                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Wird **gesendet, wenn der PlayNextChapter-Befehl** aktiviert oder deaktiviert wurde.               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Wird gesendet, **wenn der PlayPrevChapter-Befehl** aktiviert oder deaktiviert wurde.               |
| [**PlayTitle**](playtitle.md)                                         | Wird gesendet, **wenn der PlayTitle-Befehl** aktiviert oder deaktiviert wurde.                     |
| [**ReadyStateChange**](readystatechange.md)                           | Wird gesendet, wenn sich die **ReadyState-Eigenschaft** des MSWebDVD-Steuerelements geändert hat.            |
| [**ReplayChapter**](replaychapter.md)                                 | Wird gesendet, wenn **der Befehl ReplayChapter** aktiviert oder deaktiviert wurde.                 |
| [**Fortsetzen**](resume.md)                                               | Wird gesendet, wenn **der Befehl** Fortsetzen aktiviert oder deaktiviert wurde.                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Wird gesendet, **wenn der Befehl ReturnFromSubmenu** aktiviert oder deaktiviert wurde.             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Wird gesendet, wenn der Datenträger die Auswahl oder Aktivierung von Menüschaltflächen aktiviert oder deaktiviert.   |
| [**ShowMenu**](showmenu.md)                                           | Wird gesendet, wenn der Datenträger die Anzeige eines Menüs aktiviert oder deaktiviert.                         |
| [**StillOff**](stilloff.md)                                           | Wird gesendet, wenn **der StillOff-Befehl** aktiviert oder deaktiviert wurde.                      |
| [**Beenden**](stop.md)                                                   | Wird gesendet, **wenn der Befehl** Beenden aktiviert oder deaktiviert wurde.                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | Wird gesendet, wenn die Überlagerungsoberfläche verschoben oder ihre Größe geändert wurde oder der Farbschlüssel geändert wurde. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MSWebDVD-Objekt](mswebdvd-object.md)
</dt> </dl>

 

 



