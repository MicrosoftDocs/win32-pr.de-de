---
title: Senden von ASF-Daten an einen Veröffentlichungspunkt
description: Senden von ASF-Daten an einen Veröffentlichungspunkt
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Medienformat-SDK, Senden von ASF-Daten
- Windows Medienformat-SDK, Veröffentlichungspunkte
- Advanced Systems Format (ASF), Senden von Daten
- ASF (Advanced Systems Format), Senden von Daten
- Advanced Systems Format (ASF), Veröffentlichungspunkte
- ASF (Advanced Systems Format), Veröffentlichungspunkte
- Veröffentlichungspunkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f70c1a49ea7ff6272d0eef9f1a51ff79ec216ed9af445c3078d59dd19841dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197539"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Senden von ASF-Daten an einen Veröffentlichungspunkt

Sie können das Windows Media Format SDK verwenden, um ASF-Daten mithilfe von Push an einen Veröffentlichungspunkt auf einem Windows Medienserver zu übertragen. Der Server überträgt dann die Daten von diesem Veröffentlichungspunkt. Dieses Szenario ist nützlich, wenn Sie Inhalte auf einem Computer erfassen oder erneut codieren und den Inhalt von einem anderen Computer (oder mehreren Computern) verteilen möchten. Dies ist auch nützlich, wenn Sie Inhalte von einem Computer innerhalb einer Firewall auf einen Windows Media-Server außerhalb der Firewall verschieben müssen, da die Pushverteilung das HTTP-Protokoll verwendet.

> [!Note]  
> Ein *Veröffentlichungspunkt* verhält sich im Wesentlichen wie ein Redirector. Der Client gibt den Veröffentlichungspunkt in der URL an (z. B. mms://MyServer/MyPublishingPoint), und der Server übersetzt dies in eine Inhaltsanforderung.

 

Fügen Sie das Pushsenkenobjekt an das Writerobjekt an, um Daten an den Veröffentlichungspunkt zu pushen. Die Pushsenke wird verwendet, um die Verbindung mit dem Server zu öffnen und die Pushsitzung zu verwalten. Das Writer-Objekt verarbeitet alle anderen Aspekte beim Erstellen der Datei.

Führen Sie die folgenden Schritte aus:

1.  Erstellen Sie das Writer-Objekt, indem Sie die [**WMCreateWriter-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) aufrufen, die einen [**IWMWriter-Zeiger**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) zurückgibt.
2.  Erstellen Sie das Pushsenkenobjekt, indem Sie die [**WMCreateWriterPushSink-Funktion**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) aufrufen, die einen [**IWMWriterPushSink-Zeiger**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) zurückgibt.
3.  Fügen Sie die Netzwerksenke an den Writer an, indem Sie [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) auf dem Writer mit einem Zeiger auf die **IWMWriterPushSink-Schnittstelle** der Netzwerksenke aufrufen.
4.  Verbinden durch Aufrufen von [**IWMWriterPushSink::Verbinden**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect)auf den Server.
5.  Schreiben Sie den Stream. Dieser Schritt umfasst das Festlegen des Profils für das Writer-Objekt, das Senden von Beispielen an den Writer und möglicherweise andere Aufgaben. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md) Weitere Aufgaben können das Festlegen von Metadatenattributen (wie [unter](working-with-metadata.md)Arbeiten mit Metadaten beschrieben) oder das Festlegen von Live-DRM im Stream (wie unter Aktivieren [der DRM-Unterstützung beschrieben) umfassen.](enabling-drm-support.md) Diese Aufgaben werden genau so ausgeführt, wie sie für das Schreiben von ASF-Dateien gelten.
6.  Nachdem Sie mit dem Schreiben fertig sind, rufen Sie [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) auf dem Writer auf, um das Pushsenkenobjekt zu trennen.
7.  Rufen [**Sie IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) in der Pushsenke auf, um die Sitzung mit dem Server zu beenden.

Diese Schritte werden in der WMVNetWrite-Beispielanwendung veranschaulicht.

> [!Note]  
> Wenn Sie eine Nur-Videodatei mit sehr niedriger Bitrate senden, wird die Wiedergabe am Veröffentlichungspunkt möglicherweise einige Sekunden lang nicht gestartet. Dies kann in verschiedenen Fällen vorkommen, z. B. wenn ein einzelnes Paket viele kleine Videoframes und keine Audiodaten enthält oder wenn eine lange Zeitlücke zwischen dem ersten Paket und dem zweiten Paket in einer videobasierten Datei mit niedriger Bitrate besteht. Um dieses Problem zu vermeiden, fügen Sie einen automatischen Audiostream in die Datei ein.

 

## <a name="authentication"></a>Authentifizierung

Die Authentifizierung beim Server wird automatisch vom Pushsenkenobjekt verarbeitet. Die Anwendung muss jedoch möglicherweise Anmeldeinformationen angeben. Dies erfolgt über **die IWMCredentialCallback-Rückrufschnittstelle** wie folgt:

1.  Implementieren Sie [**die SCHNITTSTELLEN IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) und [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) in Ihrer Anwendung.
2.  Fragen Sie das Pushsenkenobjekt für die [**IWMRegisterCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) ab.
3.  Rufen [**Sie IWMRegisterCallback::Advise mit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) einem Zeiger auf die **IWMStatusCallback-Schnittstelle Ihrer Anwendung** auf.
4.  Wenn die Pushsenke Anmeldeinformationen von der Anwendung abrufen muss, fragt sie den **IWMStatusCallback-Zeiger** für die **IWMCredentialCallback-Schnittstelle** ab und ruft [**IWMCredentialCallback::AcquireCredentials auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials) Informationen zu dieser Methode finden Sie unter [Authentifizierung.](authentication.md)
5.  Wenn Sie fertig sind, rufen Sie [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) auf, um das Abrufen von Ereignisbenachrichtigungen von der Pushsenke zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Senden von ASF-Daten über ein Netzwerk**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> <dt>

[**Writer-Pushsenkeobjekt**](writer-push-sink-object.md)
</dt> </dl>

 

 




