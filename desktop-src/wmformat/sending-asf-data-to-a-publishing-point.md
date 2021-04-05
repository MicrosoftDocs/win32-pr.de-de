---
title: Senden von ASF-Daten an einen Publishing Point
description: Senden von ASF-Daten an einen Publishing Point
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media-Format-SDK, Senden von ASF-Daten
- Windows Media-Format-SDK, Veröffentlichungs Punkte
- Advanced Systems Format (ASF), Senden von Daten
- ASF (Advanced Systems Format), Senden von Daten
- Advanced Systems Format (ASF), Veröffentlichungs Punkte
- ASF (Advanced Systems-Format), Veröffentlichungs Punkte
- Veröffentlichungs Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724126"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Senden von ASF-Daten an einen Publishing Point

Mit dem Windows Media-Format-SDK können Sie die Daten von ASF an einen Publishing Point auf einem Windows Media-Server überführen. Der Server überträgt dann die Daten von diesem Publishing Point. Dieses Szenario ist nützlich, wenn Sie Inhalte auf einem Computer erfassen oder neu codieren und den Inhalt von einem anderen Computer (oder mehreren Computern) verteilen möchten. Dies ist auch nützlich, wenn Sie Inhalte von einem Computer innerhalb einer Firewall auf einen Windows Media-Server außerhalb der Firewall verschieben müssen, da die Pushverteilung das HTTP-Protokoll verwendet.

> [!Note]  
> Ein *Publishing Point* verhält sich im Wesentlichen wie ein Redirector. Der Client gibt den Publishing Point in der URL an (z. b. MMS://MyServer/MyPublishingPoint), und der Server übersetzt diesen in eine Inhalts Anforderung.

 

Fügen Sie das Push Sink-Objekt an das Writer-Objekt an, um Daten per Push an den Publishing Point zu übersetzen Mithilfe der Push-Senke wird die Verbindung mit dem Server geöffnet und die pushsitzung verwaltet. Das Writer-Objekt behandelt alle anderen Aspekte der Dateierstellung.

Führen Sie die folgenden Schritte aus:

1.  Erstellen Sie das Writer-Objekt, indem Sie die [**wmcreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion aufrufen, die einen [**iwmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) -Zeiger zurückgibt.
2.  Erstellen Sie das Push Sink-Objekt, indem Sie die [**wmcreateschreiterpushsink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) -Funktion aufrufen, die einen [**iwmwrite-pushsink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) -Zeiger zurückgibt.
3.  Fügen Sie die Netzwerk Senke an den Writer an, indem Sie [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) für den Writer aufrufen, mit einem Zeiger auf die **iwmschreiterpushsink** -Schnittstelle der Netzwerk Senke.
4.  Stellen Sie eine Verbindung mit dem Server her, indem Sie [**iwmschreiterpushsink:: Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect)aufrufen.
5.  Schreiben Sie den Stream. Dieser Schritt umfasst das Festlegen des Profils für das Writer-Objekt, das Senden von Beispielen an den Writer und möglicherweise andere Aufgaben. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md). Weitere Aufgaben können das Festlegen von Metadatenattributen (wie unter [Arbeiten mit Metadaten](working-with-metadata.md)beschrieben) oder das Festlegen von Live-DRM im Stream (wie unter [Aktivieren der DRM-Unterstützung](enabling-drm-support.md)beschrieben) umfassen. Diese Aufgaben werden genau wie beim Schreiben von ASF-Dateien ausgeführt.
6.  Wenn Sie den Schreibvorgang abgeschlossen haben, nennen Sie [**iwmwriteradvanced:: removesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) auf dem Writer, um das Push Sink-Objekt zu trennen.
7.  Nennen Sie [**iwmschreiterpushsink:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) auf der Push-Senke, um die Sitzung mit dem Server zu beenden.

Diese Schritte werden in der wmvnetwrite-Beispielanwendung veranschaulicht.

> [!Note]  
> Wenn Sie eine nur-Low-Bitrate-Videodatei senden, wird Sie möglicherweise einige Sekunden lang nicht auf dem Publishing Point abgespielt. Dies kann in verschiedenen Fällen vorkommen, z. b. Wenn ein einzelnes Paket viele kleine Video Frames und keine Audiodaten enthält, oder wenn es eine lange Zeitspanne zwischen dem ersten Paket und dem zweiten Paket in einer nur-Video-Datei mit geringem Bitrate gibt. Um dieses Problem zu vermeiden, fügen Sie einen automatischen Audiostream in die Datei ein.

 

## <a name="authentication"></a>Authentifizierung

Die Authentifizierung beim Server wird automatisch vom Push-Senkenobjekt verarbeitet. Die Anwendung muss jedoch möglicherweise Anmelde Informationen bereitstellen. Dies erfolgt über die **iwmkredentialcallback** -Rückruf Schnittstelle wie folgt:

1.  Implementieren Sie die [**iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) -und die [**iwmkredentialcallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) -Schnittstelle in Ihrer Anwendung.
2.  Fragen Sie das Push Sink-Objekt für die [**iwmregistercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) -Schnittstelle ab.
3.  Rufen Sie [**iwmregistercallback:: Rat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) mit einem Zeiger auf die **iwmstatus Callback** -Schnittstelle Ihrer Anwendung auf.
4.  Wenn die pushsenke Anmelde Informationen von der Anwendung erhalten muss, fragt Sie den **iwmstatus Callback** -Zeiger auf die **iwmkredentialcallback** -Schnittstelle ab und ruft [**iwmkredentialcallback:: acquirecredenseins**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials)auf. Weitere Informationen zu dieser Methode finden Sie unter [Authentifizierung](authentication.md).
5.  Wenn Sie den Vorgang abgeschlossen haben, rufen Sie [**iwmregistercallback:: unempfehlung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) auf, um das Abrufen von Ereignis Benachrichtigungen von der pushsenke zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Senden von ASF-Daten über ein Netzwerk**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> <dt>

[**Writer-Push-Sink-Objekt**](writer-push-sink-object.md)
</dt> </dl>

 

 




