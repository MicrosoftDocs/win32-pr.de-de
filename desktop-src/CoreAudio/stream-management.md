---
description: Datenstrom Verwaltung
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Datenstrom Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127049"
---
# <a name="stream-management"></a>Datenstrom Verwaltung

Nachdem Sie die [audioendpunktgeräte](audio-endpoint-devices.md) im System aufgelistet und ein geeignetes Rendering-oder Erfassungsgerät identifiziert haben, besteht die nächste Aufgabe für eine audioclientanwendung darin, eine Verbindung mit dem Endpunkt Gerät zu öffnen und den Fluss der Audiodaten über diese Verbindung zu verwalten. [WASAPI](wasapi.md) ermöglicht Clients das Erstellen und Verwalten von Audiodatenströmen.

WASAPI implementiert mehrere Schnittstellen, um streamverwaltungsdienste für audioclients bereitzustellen. Die primäre Schnittstelle ist [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient). Ein Client ruft die **iaudioclient** -Schnittstelle für ein audioendpunktgerät ab, indem er die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode (mit dem Parameter *IID* ist auf **refi** IID \_ iaudioclient festgelegt) für das Endpunkt Objekt aufgerufen.

Der Client ruft die Methoden in der [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle auf, um Folgendes durchzuführen:

-   Ermitteln Sie, welche Audioformate das Endpunkt Gerät unterstützt.
-   Gibt die Größe des Endpunkt Puffers an.
-   Das Streamformat und die Latenzzeit erhalten.
-   Starten, Abbrechen und Zurücksetzen des Streams, der über das Endpunkt Gerät fließt.
-   Greifen Sie auf zusätzliche Audiodienste zu.

Zum Erstellen eines Streams Ruft ein Client die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf. Durch diese Methode gibt der Client das Datenformat für den Stream, die Größe des Endpunkt Puffers und ob der Stream im freigegebenen oder exklusiven Modus betrieben wird.

Die verbleibenden Methoden in der [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle fallen in zwei Gruppen:

-   Methoden, die nur aufgerufen werden können, nachdem der Stream von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)geöffnet wurde.
-   Methoden, die zu einem beliebigen Zeitpunkt vor oder nach dem [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Aufruf aufgerufen werden können.

Die folgenden Methoden können nur nach dem Aufruf von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)aufgerufen werden:

-   [**Iaudioclient:: getBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**Iaudioclient:: getcurrentpadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**Iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**Iaudioclient:: getstreamlatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**Iaudioclient:: Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**Iaudioclient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**Iaudioclient:: Beendigung**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

Die folgenden Methoden können vor oder nach dem [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Aufruf aufgerufen werden:

-   [**Iaudioclient:: getdeviceperiod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**Iaudioclient:: getmixformat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**Iaudioclient:: isformatsupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Um auf die zusätzlichen audioclientdienste zuzugreifen, ruft der Client die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode auf. Mit dieser Methode kann der Client Verweise auf die folgenden Schnittstellen abrufen:

-   [**Iaudiorenderclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Schreibt Renderingdaten in einen Endpunkt Puffer für audiorendering.

-   [**Iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Liest erfasste Daten aus einem Endpunkt Puffer der Audioerfassung.

-   [**Iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Kommuniziert mit dem audiositzungsmanager, um die dem Stream zugeordnete Audiositzung zu konfigurieren und zu verwalten.

-   [**Isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Steuert die Volumeebene der Audiositzung, die dem Stream zugeordnet ist.

-   [**Ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Steuert die volumeebenen der einzelnen Kanäle in der Audiositzung, die dem Stream zugeordnet ist.

-   [**Iaudioclock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Überwacht die streamdatenrate und die Streamposition.

Außerdem sollten WASAPI-Clients, für die Benachrichtigungen über Sitzungs bezogene Ereignisse erforderlich sind, die folgende Schnittstelle implementieren:

-   [**Iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Um Ereignis Benachrichtigungen zu empfangen, übergibt der Client einen Zeiger an seine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle an die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode als callparameter.

Zum Schluss verwendet ein Client möglicherweise eine API auf höherer Ebene, um einen Audiostream zu erstellen, erfordert aber auch Zugriff auf die Sitzungs Steuerelemente und volumesteuerelemente für die Sitzung, die den Stream enthält. Eine API höherer Ebene bietet diesen Zugriff in der Regel nicht. Der Client kann die Steuerelemente für eine bestimmte Sitzung über die [**iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) -Schnittstelle abrufen. Diese Schnittstelle ermöglicht es dem Client, die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle und die [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) -Schnittstelle für eine Sitzung abzurufen, ohne dass der Client die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle zum Erstellen eines Streams und zum Zuweisen des Streams zur Sitzung benötigt. Ein Client ruft die **iaudiosessionmanager** -Schnittstelle für ein audioendpunktobjekt ab, indem er die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode (mit dem Parameter *IID* ist auf **refID** IID \_ iaudiosessionmanager festgelegt) für das Endpunkt Objekt aufgerufen wird.

Die Schnittstellen [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)und [**iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) werden in der Header Datei audiopolicy. h definiert. Alle anderen WASAPI-Schnittstellen sind in der Header Datei "AudioClient. h" definiert.

In den folgenden Abschnitten wird beschrieben, wie Sie die WASAPI verwenden, um Audiostreams zu verwalten:

-   [Informationen zu WASAPI](wasapi.md)
-   [Rendern eines Streams](rendering-a-stream.md)
-   [Erfassen eines Streams](capturing-a-stream.md)
-   [Loopback Aufzeichnung](loopback-recording.md)
-   [Datenströme im exklusiven Modus](exclusive-mode-streams.md)
-   [Wiederherstellen nach einem Invalid-Device Fehler](recovering-from-an-invalid-device-error.md)
-   [Verwenden eines kommunikationsgeräts](using-the-communication-device.md)
-   [Streamrouting](stream-routing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



