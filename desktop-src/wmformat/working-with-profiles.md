---
title: Arbeiten mit Profilen
description: Arbeiten mit Profilen
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows Medienformat-SDK, Profile
- Windows Medienformat-SDK, IWMCodecInfo3-Schnittstelle
- Profile, Informationen
- profiles,Windows Media Format SDK
- profiles,IWMCodecInfo3
- IWMCodecInfo3,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68982a47b743aaa12397e937ad9bd213fbd7ac0a78b41087d01929c1d42bb622
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055430"
---
# <a name="working-with-profiles"></a>Arbeiten mit Profilen

In diesem Abschnitt wird beschrieben, wie Sie Profile entwerfen, erstellen und ändern. Jedes Profil beschreibt die Datenströme, aus denen sich eine Datei zusammen befindet, und ihre Beziehungen untereinander. Ein Profilobjekt enthält Datenstromkonfigurationsinformationen für jeden Stream, informationen zum gegenseitigen Ausschluss für Datenströme, die nicht gleichzeitig übermittelt werden können, Informationen zur Freigabe der Bandbreite und Informationen zur Streampriorisierung.

Der Hauptzweck von Profilen besteht darin, Dem Writer-Objekt Datenstromkonfigurationsinformationen bereitzustellen. Der Writer verwendet die Informationen in einem Profil, um den Prozess der Komprimierung von Eingaben mit den Codecs zu koordinieren. Wenn Sie einen komprimierten Medienstream konfigurieren, geben Sie den Codec an, der zum Komprimieren der Daten verwendet wird, und die Einstellungen, die der Codec verwendet. Sie können auch Profile für unkomprimierte Streams erstellen. Mehrere nicht komprimierte Streamtypen werden unterstützt. Obwohl sie keinen Codec benötigen, haben diese Typen ihre eigenen Anforderungen an die Streamkonfiguration. Weitere Informationen finden Sie unter [Konfigurieren von Streams](configuring-streams.md) und Verwenden von [unkomprimierten Audio- und Videodaten Streams](using-uncompressed-audio-and-video-streams.md).

Streamkonfigurationsinformationen für einen Stream mit einem der Windows Mediencodecs müssen mithilfe der Methoden der [**IWMCodecInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) aus dem Codec abgerufen werden. Die Vorgehensweise für die Verwendung von Streamformaten unterscheidet sich für Videocodecs von der Vorgehensweise für Audiocodecs. In beiden Fällen müssen Sie jedoch zunächst das Format vom Codec abrufen. Sie sollten niemals versuchen, einen Datenstrom manuell mit einem der Windows Mediencodecs zu konfigurieren, da kleine Fehler im Profil eine tiefgreifende Auswirkung auf die ASF-Datei haben können.

Die grundlegenden Schritte zum Erstellen und/oder Ändern von Profilen sind:

1.  Erstellen Sie ein leeres Profil, oder laden Sie ein vorhandenes Profil, um es zu bearbeiten.
2.  Konfigurieren Sie bei Bedarf die einzelnen Streams basierend auf unterstützten Profildaten, die vom Codec abgerufen werden, der zum Codieren des Streams verwendet wird.
3.  Konfigurieren Sie bei Bedarf gegenseitigen Ausschluss.
4.  Konfigurieren Sie bei Bedarf die Bandbreitenfreigabe.
5.  Legen Sie bei Bedarf die Priorität der Streams in der Datei fest.

In den folgenden Abschnitten wird das Erstellen und Bearbeiten von Profilen erläutert.



| `Section`                                                        | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Entwerfen von Profilen](designing-profiles.md)                   | Beschreibt das Entwerfen eines Profils.                                                                 |
| [Erstellen von Profilen](creating-profiles.md)                     | Beschreibt, wie ein leeres Profil erstellt wird.                                                          |
| [Konfigurieren von Streams](configuring-streams.md)                 | Beschreibt, wie Streams konfiguriert und in ein Profil eingeschlossen werden.                                  |
| [Verwenden des gegenseitigen Ausschlusses](using-mutual-exclusion.md)           | Beschreibt, wie gegenseitige Ausschlussobjekte erstellt und in ein Profil eingeschlossen werden.                    |
| [Verwenden der Bandbreitenfreigabe](using-bandwidth-sharing.md)         | Beschreibt die Verwendung der Bandbreitenfreigabe in einem Profil.                                               |
| [Verwenden der Streampriorisierung](using-stream-prioritization.md) | Beschreibt die Verwendung der Streampriorisierung in einem Profil.                                           |
| [Speichern von Profilen](saving-profiles.md)                         | Beschreibt, wie Ihre benutzerdefinierten Profile in einer Datei gespeichert werden.                                              |
| [Verwenden von Systemprofilen](using-system-profiles.md)             | Beschreibt die Arbeit mit Systemprofilen, um Zeit und Aufwand beim Erstellen von Profilen zu sparen.           |
| [Verwalten der Paketgröße](managing-packet-size.md)               | Erläutert, wie die Größe von Paketen in den Datenströmen von Dateien gesteuert wird, die mit Ihrem Profil erstellt wurden. |



 

**Hinweis** Benutzer früherer Versionen des Windows Media Format SDK sind möglicherweise daran gewohnt, Systemprofile ohne Änderungen zum Erstellen ihrer Dateien zu verwenden. Das Windows Media Format 9 Series SDK oder höher enthält keine neuen Systemprofile, die die Codecs der Windows Media 9-Serie oder höher verwenden. Dies liegt an der zunehmenden Anzahl von Profilen, die benötigt werden, um die verschiedenen Features abzudecken, die jetzt von den Codecs angeboten werden. Sie können weiterhin die Systemprofile der Version 8 als Ausgangspunkt für Ihre Profile verwenden. Weitere Informationen finden Sie unter [Verwenden von Systemprofilen.](using-system-profiles.md) Informationen zum neuen Mechanismus für die Ausrichtung von Profilen auf bestimmte Übermittlungsgeräte finden Sie unter [Arbeiten mit Gerätekonformitätsvorlagen.](working-with-device-conformance-templates.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




