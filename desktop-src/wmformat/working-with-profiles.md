---
title: Arbeiten mit Profilen
description: Arbeiten mit Profilen
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows Media-Format-SDK, profile
- Windows Media-Format-SDK, IWMCodecInfo3-Schnittstelle
- Profile, Informationen zu
- Profile, SDK für Windows Media-Format
- Profile, IWMCodecInfo3
- IWMCodecInfo3, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664bbafd6c628588aa3b45b0a62a216db7bd7749
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389872"
---
# <a name="working-with-profiles"></a>Arbeiten mit Profilen

In diesem Abschnitt wird beschrieben, wie Profile entworfen, erstellt und geändert werden. In jedem Profil werden die Streams beschrieben, aus denen eine Datei und ihre Beziehungen zusammenhängen. Ein Profil Objekt enthält Datenstrom-Konfigurationsinformationen für jeden Stream, Informationen zur gegenseitigen Ausschluss von Datenströmen, die nicht gleichzeitig übermittelt werden können, Informationen zur Bandbreiten Freigabe sowie Informationen zur streampriorisierung.

Der Hauptzweck von Profilen besteht darin, streamingkonfigurationsinformationen für das Writer-Objekt bereitzustellen. Der Writer verwendet die Informationen in einem Profil, um den Prozess der Komprimierung von Eingaben mit den Codecs zu koordinieren. Beim Konfigurieren eines komprimierten Mediendaten Stroms geben Sie den Codec an, der zum Komprimieren der Daten und der vom Codec verwendeten Einstellungen verwendet wird. Sie können auch Profile für nicht komprimierte Datenströme erstellen. Mehrere nicht komprimierte Streamtypen werden unterstützt. Obwohl Sie keinen Codec benötigen, haben diese Typen ihre eigenen Anforderungen an die streamkonfiguration. Weitere Informationen finden Sie unter [Konfigurieren von Streams](configuring-streams.md) und [Verwenden von unkomprimierten Audiodatenströmen](using-uncompressed-audio-and-video-streams.md).

Datenstrom-Konfigurationsinformationen für einen Datenstrom mithilfe eines der Windows Media-Codecs müssen mithilfe der Methoden der [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) -Schnittstelle aus dem Codec abgerufen werden. Die Vorgehensweise für die Verwendung von Datenstrom Formaten ist für Video Codecs anders als für Audiocodecs. in beiden Fällen müssen Sie jedoch zunächst das Format vom Codec erhalten. Sie sollten nie versuchen, einen Stream manuell mithilfe eines der Windows Media-Codecs zu konfigurieren, da kleine Fehler im Profil tiefgreifende Auswirkungen auf die ASF-Datei haben können.

Die grundlegenden Schritte beim Erstellen und/oder Ändern von Profilen lauten:

1.  Erstellen Sie ein leeres Profil, oder laden Sie ein vorhandenes Profil, das bearbeitet werden soll.
2.  Konfigurieren Sie jeden der Streams, falls erforderlich, basierend auf den unterstützten Profildaten, die vom Codec abgerufen werden, der zum Codieren des Streams verwendet wird.
3.  Konfigurieren Sie bei Bedarf den gegenseitigen Ausschluss.
4.  Konfigurieren Sie die Bandbreiten Freigabe bei Bedarf.
5.  Legen Sie bei Bedarf die Priorität der Streams in der Datei fest.

In den folgenden Abschnitten wird das Erstellen und Bearbeiten von Profilen erläutert.



| `Section`                                                        | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Entwerfen von Profilen](designing-profiles.md)                   | Beschreibt, wie ein Profil entworfen wird.                                                                 |
| [Erstellen von Profilen](creating-profiles.md)                     | Hier wird beschrieben, wie ein leeres Profil erstellt wird.                                                          |
| [Konfigurieren von Streams](configuring-streams.md)                 | Beschreibt das Konfigurieren von Streams und das einschließen in ein Profil.                                  |
| [Verwenden von gegenseitigem Ausschluss](using-mutual-exclusion.md)           | Beschreibt das Erstellen von gegenseitigen Ausschluss Objekten und das einschließen in ein Profil.                    |
| [Verwenden der Bandbreiten Freigabe](using-bandwidth-sharing.md)         | Beschreibt, wie die Bandbreiten Freigabe in einem Profil verwendet wird.                                               |
| [Verwenden der streampriorisierung](using-stream-prioritization.md) | Beschreibt, wie die streampriorisierung in einem Profil verwendet wird.                                           |
| [Speichern von Profilen](saving-profiles.md)                         | Hier wird beschrieben, wie Sie Ihre benutzerdefinierten Profile in einer Datei speichern.                                              |
| [Verwenden von System Profilen](using-system-profiles.md)             | Beschreibt das Arbeiten mit Systemprofilen, um Zeit und Aufwand beim Erstellen von Profilen zu sparen.           |
| [Verwalten der Paketgröße](managing-packet-size.md)               | Erläutert, wie die Größe von Paketen in den Datenströmen von Dateien gesteuert wird, die mit Ihrem Profil erstellt wurden. |



 

**Hinweis** Benutzer früherer Versionen des Windows Media SDK-SDK sind möglicherweise daran gewöhnt, Systemprofile ohne Änderungen zum Erstellen Ihrer Dateien zu verwenden. Das Windows Media Format 9-Serien-SDK oder höher enthält keine neuen Systemprofile, die die Windows Media 9-Serie oder spätere Codecs verwenden. Dies liegt an der zunehmenden Anzahl von Profilen, die benötigt werden, um die verschiedenen Features abzudecken, die jetzt von den Codecs angeboten werden. Sie können die Systemprofile der Version 8 weiterhin als Ausgangspunkt für Ihre Profile verwenden. Weitere Informationen finden [Sie unter Verwenden von System Profilen](using-system-profiles.md). Informationen zum neuen Mechanismus für die Zielplattform für Profile für bestimmte Übermittlungs Geräte finden Sie unter [Arbeiten mit Geräte Konformitäts Vorlagen](working-with-device-conformance-templates.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




