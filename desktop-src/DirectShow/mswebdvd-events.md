---
description: Mswebdvd-Ereignisse
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Mswebdvd-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f363f15c35cbfe61a3ab1ff3703a31307785481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346586"
---
# <a name="mswebdvd-events"></a>Mswebdvd-Ereignisse

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

> [!Note]  
> Diese API ist veraltet. Weitere Informationen zur DVD-Wiedergabe und-Navigation in DirectShow finden Sie unter [DVD-Anwendungen](dvd-applications.md).

 

Das mswebdvd Microsoft® ActiveX®-Steuerelement benachrichtigt Ihre Anwendung, wenn verschiedene Typen interner Ereignisse auftreten oder wenn bestimmte Informationen auf der Festplatte auftreten.

Die meisten Ereignisse beziehen sich auf User Operation (UOP)-Steuerelemente. DVD-Autoren können die Festplatte codieren, sodass ein beliebiger DVD-Befehl (z. b. **playforward**, **Pause**, **showmenu** usw.) jederzeit deaktiviert werden kann. Die meisten Benutzer können z. b. Benutzern nicht erlauben, ein Menü zu beschleunigen oder anzuzeigen, während die FBI-Warnung wiedergegeben wird. Nach dem Überschreiten der Warnung werden diese Vorgänge von der Festplatte zugelassen. Durch die Behandlung der UOP-Ereignisse kann Ihre Anwendung die Benutzeroberfläche aktualisieren, um den Benutzer anzuzeigen, welche Befehle derzeit von der Festplatte zugelassen werden. Die gängigste Methode hierfür ist, eine Schaltfläche zu deaktivieren. Wenn Ihre Anwendung z. b. ein playforward-Ereignis empfangen hat, bei dem **benabled** auf **false** festgelegt ist, können Sie die Wiedergabe Schaltfläche deaktivieren. Wenn dieses Ereignis empfangen wurde, bei dem **benabled** auf **true** festgelegt ist, können Sie die Schaltfläche erneut aktivieren.

Es gibt drei Ereignisse, die nicht mit UOP-Steuerelementen in Beziehung stehen. Das **dvdnotify** -Ereignis benachrichtigt Ihre Anwendung über viele verschiedene Arten von DVD-bezogenen Ereignissen, die im *EventCode* -Parameter identifiziert werden. Einige Ereignisse verfügen über zusätzliche Informationen in den Parametern *param1* und *Param2* . Das Ereignis "read **ystatechange** " benachrichtigt Ihre Anwendung über Änderungen in der Eigenschaft "mswebdvd Read ystate", bei der es sich um eine Eigenschaft handelt, die allen ActiveX-Steuerelementen gemeinsam ist. Das **updateoverlay** -Ereignis wird nur an Anwendungen gesendet, wenn mswebdvd im fensterlosen Modus gehostet wird. Anwendungen müssen nur auf dieses Ereignis reagieren, wenn Sie Gleit Komma Schaltflächen über dem Video Rechteck im Vollbildmodus anzeigen.



| Ereignis                                                                  | BESCHREIBUNG                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Changecurrentangle**](changecurrentangle.md)                       | Wird gesendet, wenn die Festplatte das Ändern des Winkels aktiviert oder deaktiviert.                            |
| [**Changecurrentaudiostream**](changecurrentaudiostream.md)           | Wird gesendet, wenn die Festplatte das Ändern des Audiostreams aktiviert oder deaktiviert.                     |
| [**Changecurrentsubpicturestream**](changecurrentsubpicturestream.md) | Wird gesendet, wenn der **changecurrentsubpicturestream** -Befehl aktiviert oder deaktiviert wurde. |
| [**Dvdnotify**](dvdnotify.md)                                         | Benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Disk-Anweisungen.           |
| [**Pausegon**](pauseon.md)                                             | Wird gesendet, wenn der **Pause** -Befehl aktiviert oder deaktiviert wurde.                         |
| [**Playattime**](playattime.md)                                       | Wird gesendet, wenn der **playattime** -Befehl aktiviert oder deaktiviert wurde.                    |
| [**Playattimeingetitle**](playattimeintitle.md)                         | Wird gesendet, wenn der Befehl " **playattimeintitle** " aktiviert oder deaktiviert wurde.             |
| [**Playrückwärts**](playbackwards.md)                                 | Wird gesendet, wenn der Befehl " **playrückwärts** " aktiviert oder deaktiviert wurde.                 |
| [**Playchapter**](playchapter.md)                                     | Wird gesendet, wenn der Befehl " **playchapter** " aktiviert oder deaktiviert wurde.                   |
| [**Playchapterintitle**](playchapterintitle.md)                       | Wird gesendet, wenn der Befehl " **playchapterintitle** " aktiviert oder deaktiviert wurde.            |
| [**Playforward**](playforwards.md)                                   | Wird gesendet, wenn der Befehl " **playforward** " aktiviert oder deaktiviert wurde.                  |
| [**Playnextchapter**](playnextchapter.md)                             | Wird gesendet, wenn der Befehl **playnextchapter** aktiviert oder deaktiviert wurde.               |
| [**Playprevchapter**](playprevchapter.md)                             | Wird gesendet, wenn der Befehl **playprevchapter** aktiviert oder deaktiviert wurde.               |
| [**Playtitle**](playtitle.md)                                         | Wird gesendet, wenn der **playtitle** -Befehl aktiviert oder deaktiviert wurde.                     |
| [**"Leserystatechange"**](readystatechange.md)                           | Wird gesendet, wenn die Eigenschaft "read- **State** " des mswebdvd-Steuer Elements geändert wurde.            |
| [**Replaychapter**](replaychapter.md)                                 | Wird gesendet, wenn der **replaychapter** -Befehl aktiviert oder deaktiviert wurde.                 |
| [**Fortsetzen**](resume.md)                                               | Wird gesendet, wenn der **Resume** -Befehl aktiviert oder deaktiviert wurde.                        |
| [**Returnfromsubmenu**](returnfromsubmenu.md)                         | Wird gesendet, wenn der **returnfromsubmenu** -Befehl aktiviert oder deaktiviert wurde.             |
| [**Selectoractivatbutton**](selectoractivatbutton.md)                 | Wird gesendet, wenn die Festplatte die Auswahl oder Aktivierung von Menü Schaltflächen aktiviert oder deaktiviert.   |
| [**Showmenu**](showmenu.md)                                           | Wird gesendet, wenn der Disc die Anzeige eines Menüs aktiviert oder deaktiviert.                         |
| [**Stilloff**](stilloff.md)                                           | Wird gesendet, wenn der Befehl " **stilloff** " aktiviert oder deaktiviert wurde.                      |
| [**Stop**](stop.md)                                                   | Wird gesendet, wenn der Befehl " **Beenden** " aktiviert oder deaktiviert wurde.                          |
| [**Updateoverlay**](updateoverlay.md)                                 | Wird gesendet, wenn die Overlay-Oberfläche verschoben oder die Größe geändert wurde oder der Farbschlüssel geändert wurde. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mswebdvd-Objekt](mswebdvd-object.md)
</dt> </dl>

 

 



