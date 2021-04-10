---
description: Lautstärkeregler
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: Lautstärkeregler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fd25d4157030071a47ac8eec26dc0e4d50e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861288"
---
# <a name="volume-controls"></a>Lautstärkeregler

Clients, die Datenströme im freigegebenen Modus verwalten, verwenden in der Regel die Schnittstellen [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) und [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) in der [WASAPI](wasapi.md) , um die Datenstrom Volume-Ebenen zu steuern Mithilfe der Methoden in der **isimpleaudiovolume** -Schnittstelle kann der Client die volumeebenen der [audiositzungen](audio-sessions.md) , zu denen die Streams im freigegebenen Modus gehören, erhalten und festlegen. Wenn das Sitzungs Volume von sndvol oder einer anderen Anwendung geändert wird, kann der Client über die Schnittstelle **iaudiosessionevents** eine Benachrichtigung über die Änderung empfangen.

Clients, die Datenströme im exklusiven Modus verwalten, verwenden in der Regel die Schnittstellen [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) und [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) in der [endpointvolume-API](endpointvolume-api.md) zum Steuern und Überwachen der Datenstrom Volume-Ebenen. Mithilfe der Methoden in der **iaudioendpointvolume** -Schnittstelle kann der Client die Volumeebene eines [audioendpunktgeräts](audio-endpoint-devices.md)erhalten und festlegen. Wenn die Volumeebene des Endpunkt Geräts von sndvol oder einer anderen Anwendung geändert wird, kann der Client über die Schnittstelle **iaudioendpointvolumecallback** eine Benachrichtigung über die Änderung empfangen.

Wie in [audiositzungen](audio-sessions.md)erläutert, ist sndvol das Programm zur Systemvolumen Steuerung. Es werden volumesteuerelemente für die audiorendering-Endpunkt Geräte im System angezeigt. (Zurzeit werden die volumesteuerelemente für Geräte mit audioerfassungs-Endpunkt nicht angezeigt.) Um die volumesteuerelemente für ein bestimmtes Gerät anzuzeigen, klicken Sie in der Menüleiste auf **Gerät** , und wählen Sie in der Liste der verfügbaren Geräte einen Gerätenamen aus.

Das sndvol-Fenster trennt die volumesteuerelemente für ein Gerät in zwei Gruppen. Das Gruppenfeld auf der linken Seite des Fensters wird als **Gerät** bezeichnet. Das Feld **Gerät** enthält ein einzelnes volumensteuerelement, das von der [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle gesteuert wird. Änderungen, die der Benutzer an diesem volumensteuerelement vornimmt, können über die [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle überwacht werden.

Das Gruppenfeld auf der rechten Seite des sndvol-Fensters heißt **Anwendungen**. Das Feld **Anwendungen** enthält die volumesteuerelemente für die Anwendungen, die das Gerät zurzeit freigeben. Bei Anwendungen, die das Gerät im freigegebenen Modus verwenden, stellen die volumesteuerelemente die von der Schnittstelle [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) kontrollierten volumeebenen dar. Änderungen, die der Benutzer an diesen volumesteuerelementen vornimmt, können über die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle überwacht werden.

Obwohl eine Anwendung im freigegebenen Modus die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle verwenden kann, um Änderungen zu überwachen, die der Benutzer an der volumesteuerung der Anwendung im Feld **Anwendungen** im Fenster sndvol vornimmt, kann die Anwendung Änderungen an den volumesteuerelementen anderer, nicht verwandter Anwendungen nicht überwachen. Ebenso kann eine Anwendung die volumeebenen ihrer audiositzungen über die [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) -Schnittstelle ändern, aber Sie kann die volumeebenen von Sitzungen, die zu anderen, nicht verknüpften Anwendungen gehören, nicht ändern.

Allerdings können zwei oder mehr verwandte Anwendungen (oder Instanzen der gleichen Anwendung) dasselbe volumensteuerelement im **Anwendungs** Feld des sndvol-Fensters gemeinsam nutzen, indem Sie Ihre Audiodatenströme entweder der gleichen prozessübergreifenden Sitzung zuweisen oder ihre entsprechenden Sitzungen mit demselben Gruppierungs Parameter verknüpfen. Weitere Informationen finden Sie unter [audiositzungen](audio-sessions.md) und [Gruppierungs Parameter](grouping-parameters.md).

WASAPI bietet zwei zusätzliche Schnittstellen, [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) und [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume), um die volumeebenen von Datenströmen im freigegebenen Modus zu steuern. Diese Schnittstellen werden hauptsächlich von spezialisierten Clients verwendet, die die Kontrolle über die volumeebenen entweder einzelner Kanäle in einer Sitzung oder einzelner Datenströme in einer Sitzung benötigen.

Mit der-API für die Geräte- [API](devicetopology-api.md) können Clients auf die volumesteuerelemente in den Topologien von audioadaptern zugreifen. Clients, die Datenströme im exklusiven Modus verwalten, verwenden jedoch in der Regel die endpointvolume-API anstelle der devicetopology-API, um die streamvolumeebenen zu steuern. Die endpointvolume-API vereinfacht die Steuerung des Umfangs eines Endpunkt Geräts auf zwei Arten. Erstens: Wenn ein Endpunkt Gerät ein Hardware Volume-Steuerelement implementiert, erfordert die Geräte-API, dass der Client die Geräte Topologie bei der Suche nach dem Hardware Steuerelement durchläuft. Im Gegensatz dazu findet die endpointvolume-API automatisch das Hardware Volume-Steuerelement für den Client. Zweitens: Wenn das Endpunktgerät kein Hardware Volume-Steuerelement implementiert, muss ein Software-Client ein Volume-Steuerelement implementieren. Im Gegensatz dazu ersetzt die endpointvolume-API automatisch ein Software Volume-Steuerelement für die fehlende Hardware Steuerung.

In den folgenden Abschnitten werden die volumesteuerelemente für audiositzungen und für audioendpunktgeräte beschrieben:

-   [Sitzungs Volume-Steuerelemente](session-volume-controls.md)
-   [Steuerelemente für Endpunkt-](endpoint-volume-controls.md)
-   [Endpointvolume-API](endpointvolume-api.md)
-   [Steuerelemente für Audiosteuer Elemente](audio-tapered-volume-controls.md)
-   [Spitzen Zähler](peak-meters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



