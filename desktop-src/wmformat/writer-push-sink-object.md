---
title: Writer-Push-Sink-Objekt
description: Writer-Push-Sink-Objekt
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media-Format-SDK, Writer-Push-Sink-Objekte
- Advanced Systems Format (ASF), Writer Push Sink-Objekte
- ASF (Advanced Systems Format), Writer-Push-Sink-Objekte
- Objekte, Writer-Push-Sink-Objekte
- Writer-Push-Sink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948425"
---
# <a name="writer-push-sink-object"></a>Writer-Push-Sink-Objekt

Das Writer Push Sink-Objekt verteilt digitale Medien an Publishing Points. Beispielsweise kann ein Live Konzert von einem einzelnen Server codiert und dann an verschiedene andere Server übermittelt oder per *Pushvorgang* übertragen werden, die den Inhalt tatsächlich an Benutzer streamen.

Ein Writer-Push-Sink-Objekt wird von der [**wmkreateschreiterpushsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)-Funktion erstellt, mit der ein Zeiger auf eine **iwmschreiterpushsink** -Schnittstelle festgelegt wird. Die anderen vom-Objekt unterstützten Schnittstellen, die in der folgenden Tabelle aufgeführt sind, können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**Iwmregistercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Ermöglicht es der Anwendung, Statusmeldungen aus dem-Objekt zu erhalten.                                                  |
| [**Iwmschreibpushsink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Verwaltet eine pushverteilungssitzung.                                                                             |
| [**Iwmschreibsink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und macht mehrere Rückruf Funktionen verfügbar. |



 

Die folgende Rückruf Schnittstelle kann von der Anwendung implementiert werden, um den Fortschritt eines Writer-senkenerjektobjekts zu verfolgen.



| Schnittstelle                                      | BESCHREIBUNG                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Senden von ASF-Daten an einen Publishing Point**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




