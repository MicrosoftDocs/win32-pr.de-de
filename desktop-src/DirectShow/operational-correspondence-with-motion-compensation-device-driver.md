---
description: Operative Entsprechung für den Gerätetreiber der Bewegungskompensation
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Operative Entsprechung für den Gerätetreiber der Bewegungskompensation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213868"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Operative Entsprechung für den Gerätetreiber der Bewegungskompensation

Dieser Abschnitt enthält eine Beschreibung der Gerätetreiber Seite der Bewegungskompensation der DirectX VA-Schnittstelle. (Referenz: Windows 2000 DDK-graphics drivers-Design Guide-3,0 DirectDraw DDI-3,12 Motion Kompensierung. Eine Dokumentation zu den Strukturen in Fett Schrift finden Sie im Windows-DDK.)

Die folgenden Elemente verweisen auf Einträge, auf die über die TT-Struktur " **\_ jtioncompcallbacks** " zugegriffen wird:

1.  Zu Beginn der relevanten Verarbeitung wird das **ddmucompcreate** -Gerät des Gerätetreibers verwendet, um den Treiber zu benachrichtigen, dass der Software Decoder mit der Verwendung eines Video Acceleration-Objekts beginnt.
2.  Von [**iamvideoaccelerator:: getvideoacceleratorguids**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) empfangene GUIDs stammen aus den **ddmucompgetguids** des Gerätetreibers.
3.  Ein Aufrufen der [**iamvideoaccelerator:: getuncompformatssupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) der downstreameingabepin gibt Daten aus den **ddmucompgetformats** des Gerätetreibers zurück.
4.  Die DXVA- \_ Datenstruktur "ConnectMode" aus der [**iamvideoacceleratornotify:: getcreatevideoacceleratordata**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) des Decoders wird an den **ddmucompcreate** des Gerätetreibers übergeben.
5.  Von [**iamvideoaccelerator:: getcompbufferinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) zurückgegebene Daten stammen aus dem **ddmucompgetbuffinfo**-Gerät des Gerätetreibers.
6.  Puffer, die mithilfe von [**iamvideoaccelerator:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) gesendet werden, werden durch den **ddmukomprender** des Gerätetreibers empfangen.
7.  Durch die Verwendung von [**iamvideoaccelerator:: queryrenderstatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) wird der **ddmucompquerystatus** des Gerätetreibers aufgerufen. Ein Rückgabecode von dderr \_ wasstilldrawing aus ddmucompquerystatus wird vom Host Decoder als Rückgabecode von E \_ Ausstehend von **iamvideoaccelerator:: queryrenderstatus** erkannt.
8.  An [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) gesendete Daten werden vom **ddmucompbeginframe** des Gerätetreibers empfangen. Der Rückgabecode "E \_ Pending" ist von "ddmucompbeginframe" erforderlich, damit "e" \_ vom Host Decoder als Antwort auf " **iamvideoaccelerator:: beginFrame**" angezeigt wird.
9.  An [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) gesendete Daten werden vom **ddmucompendframe** des Gerätetreibers empfangen.
10. Am Ende der relevanten Verarbeitung wird das **ddmucompdestroy** -Gerät des Gerätetreibers verwendet, um den Treiber zu benachrichtigen, dass das aktuelle Video Beschleunigungs Objekt nicht mehr verwendet wird, sodass der Treiber alle notwendigen Bereinigungs Vorgänge ausführen kann.

 

 



