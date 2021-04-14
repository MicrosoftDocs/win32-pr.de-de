---
title: Objekte (Windows Media Format 11 SDK)
description: Objekte
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows Media-Format-SDK, Objekte
- Advanced Systems Format (ASF), Objekte
- ASF (Advanced Systems Format), Objekte
- Objekte, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d73672891395d6491009e1c62fac1f9eb81dfe
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391468"
---
# <a name="objects-windows-media-format-11-sdk"></a>Objekte (Windows Media Format 11 SDK)

Das Windows Media-Format SDK verwendet mehrere Objekte zum Lesen, schreiben, bearbeiten und Indizieren von ASF-Dateien sowie zum Erstellen und Bearbeiten von Profilen. Jedes-Objekt unterstützt eine Reihe von Schnittstellen. Einige Schnittstellen werden in mehreren Objekten unterstützt. In diesen Fällen werden alle Unterschiede in der Implementierung im Referenz Abschnitt für die-Schnittstelle erläutert.

Die Objekte im Windows Media Format SDK sind com-kompatibel. Um die Entwicklung zu vereinfachen, verfügt jedes Objekt über eine zugeordnete Erstellungs Funktion oder-Methode. Sie sollten Objekte erstellen, indem Sie die Erstellungs Funktion oder-Methode anstelle von manuell mithilfe der com-Funktion **cokreateingestance** verwenden.

An manchen Schnittstellen ist eine Zahl angefügt, wie z. b. **IWMProfile2** und **IWMWriter3**. In jedem Fall erben die nummerierten Versionen alle Methoden der früheren Versionen und fügen neue Funktionen hinzu.

Auf jeder Objekt Seite dieses Verweises werden die Schnittstellen, die im Haupt-com-Objekt enthalten sind, zuerst aufgelistet, gefolgt von Rückruf Schnittstellen, die von der Anwendung implementiert werden müssen.

In der folgenden Tabelle sind die Objekte aufgelistet, die von diesem SDK unterstützt werden, sowie eine Beschreibung der Funktionalität der einzelnen und der zum Erstellen verwendeten Objekte.



| Object                                                          | BESCHREIBUNG                                                                                                                                              | Erstellungs Funktion                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Backup Restorer](backup-restorer-object.md)                   | Sichert Lizenzen (in der Regel auf Wechselmedien) und stellt diese Lizenzen dann auf einem anderen Computer wieder her.                                           | [**Wmkreatebackuprestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Geräteregistrierung](device-registration-object.md)           | Verwaltet die Geräte Registrierungsdatenbank, die Einträge für Medienwiedergabe Geräte enthält, die über eine Netzwerkverbindung verfügbar sind.             | [**Wmkreatedeviceregistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [DRM-transryptor](drm-transcryptor-object.md)                 | Konvertiert Mediendaten, die von DRM geschützt sind, in einen Datenstrom, der an Geräte gesendet werden kann, die das Protokoll Windows Media DRM 10 for Network Devices verwenden. | [**Wmkreatedrmtranszenryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indexer](indexer-object.md)                                   | Erstellt einen Index für ASF-Dateien, um das Suchen in Dateien mit Videostreams zu ermöglichen.                                                                            | [**Wmkreateingedexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Lizenz Sperr-Agent](license-revocation-agent-object.md) | Verwaltet den Lizenz Widerruf.                                                                                                                              | [**Wmkreatelicenserevocationagent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Metadata Editor](metadata-editor-object.md)                   | Bearbeitet Metadaten in einem ASF-Dateiheader.                                                                                                                    | [**Wmkreateeditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Profil-Manager](profile-manager-object.md)                   | Stellt Schnittstellen zum Erstellen, laden und Speichern von Profilen bereit. Zum Schreiben einer ASF-Datei ist ein Profil erforderlich.                                                      | [**Wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Leser](reader-object.md)                                     | Liest ASF-Dateien. Dieses Objekt verwendet ein asynchrones Aufruf Modell für seine Vorgänge.                                                                      | [**Wmkreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Synchroner Reader](synchronous-reader-object.md)             | Liest ASF-Dateien mit synchronen Aufrufen.                                                                                                                 | [**Wmkreatesynkreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Maschine](writer-object.md)                                     | Schreibt ASF-Dateien.                                                                                                                                        | [**Wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Writer-Datei Senke](writer-file-sink-object.md)                 | Steuert die vom Writer-Objekt geschriebenen ASF-Dateien.                                                                                                         | [**Wmkreateschreiterfilesink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Writer-Netzwerk Senke](writer-network-sink-object.md)           | Steuert das Live-Netzwerk Streaming von ASF-Dateien, die vom Writer-Objekt geschrieben wurden.                                                                               | [**Wmkreateschreiternetworksink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Writer-pushsenke](writer-push-sink-object.md)                 | Steuert die Übermittlung von Streaminginhalten an Veröffentlichungs Server.                                                                                            | [**Wmkreateschreiterpushsink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

In der folgenden Tabelle sind die Objekte aufgelistet, die von anderen Objekten abhängen. Diese Objekte werden von Methoden vorhandener-Objekte erstellt.



| Object                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                           | Erstellungsmethode                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bandbreiten Freigabe](bandwidth-sharing-object.md)             | Verwaltet Informationen zur Bandbreiten Freigabe in einem Profil. Für ein Profil können mehrere Bandbreiten Freigabe Objekte vorhanden sein. Es gibt verschiedene Methoden zum Erstellen eines Freigabe Objekts für die Bandbreite, je nachdem, ob Sie ein neues Bandbreiten Freigabe Objekt erstellen oder auf ein vorhandenes Objekt zugreifen möchten.                                           | [**IWMProfile3:: kreatenewbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) Noch<br/> [**IWMProfile3:: getbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Enthält ein Medien Beispiel und alle zugehörigen Dateneinheiten Erweiterungen. Wird sowohl zum Schreiben als auch zum Lesen von Beispielen verwendet.                                                                                                                                                                                                                           | [**Iwmwriter:: Zuweisung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) Noch<br/> [**Iwmreaderindecatorex:: Zuordnung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> oder<br/> [**Iwmreaderdepcatorex:: Zuordnung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> oder<br/> Wird automatisch vom Reader-Objekt oder dem synchronen Reader-Objekt für die Beispiel Übermittlung erstellt.<br/> |
| [Eingabemedien Eigenschaften](input-media-properties-object.md)   | Verwaltet die Eigenschaften einer Eingabe. Ein Eingabe Eigenschaften Objekt kann für jede Eingabe vorhanden sein.                                                                                                                                                                                                                                             | [**Iwmwriter:: GetInput-Eigenschaften**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Gegenseitiger Ausschluss](mutual-exclusion-object.md)               | Verwaltet Informationen zum gegenseitigen Ausschluss in einem Profil. Allgemeine Verwendungsmöglichkeiten für den gegenseitigen Ausschluss sind mehrere Bitrate-Inhalte und Sound Spuren in mehreren Sprachen. Es gibt verschiedene Methoden zum Erstellen eines gegenseitigen Ausschluss Objekts, je nachdem, ob Sie ein neues gegenseitiges Ausschluss Objekt erstellen oder auf ein vorhandenes Objekt zugreifen möchten.         | [**Iwmprofile:: kreatenewmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) Noch<br/> [**Iwmprofile:: getmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Ausgabemedien Eigenschaften](output-media-properties-object.md) | Verwaltet die Eigenschaften einer Ausgabe. Ein Ausgabemedien-Eigenschaften Objekt kann für jede Ausgabe vorhanden sein. Diese Objekte können vom Reader oder vom synchronen Reader erstellt werden.                                                                                                                                                            | [**Iwmreader:: GetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) Eigenschaften Noch<br/> [**Iwmsynkreader:: GetOutput-Eigenschaften**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Profil](profile-object.md)                                 | Enthält die Daten in einem Profil, während Sie bearbeitet werden. Profil Objekte werden immer dann erstellt, wenn das Profil manipuliert werden muss. Es gibt verschiedene Methoden zum Erstellen eines Profil Objekts, je nachdem, ob Sie ein neues Profil erstellen oder auf ein vorhandenes Profil zugreifen möchten.                                                  | [**Iwmprofilemanager:: kreateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) Noch<br/> [**Iwmprofilemanager:: loadprofilebydata**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> oder<br/> [**Iwmprofilemanager:: loadprofilebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> oder<br/> [**Iwmprofilemanager:: loadsystemprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Stream-Konfiguration](stream-configuration-object.md)       | Verwaltet die Eigenschaften eines Datenstroms innerhalb eines Profils. Stream-Konfigurationsobjekte werden von Stream-Objekten immer dann erstellt, wenn Sie auf die Informationen zu einem Stream zugreifen müssen. Es gibt verschiedene Methoden zum Erstellen eines Datenstrom-Konfigurations Objekts, je nachdem, ob Sie einen neuen Stream erstellen oder auf einen vorhandenen zugreifen möchten. | [**Iwmprofile:: kreatenewstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) Noch<br/> [**Iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> oder<br/> [**Iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Streampriorisierung](stream-prioritization-object.md)     | Verwaltet die Liste der streamprioritäten für ein Profil. Die Datenströme werden in der Reihenfolge der Erhöhung der Priorität gelöscht, wenn die verfügbare Bandbreite eingeschränkt ist. In einem Profil kann nur ein Datenstrom Priorisierungs Objekt vorhanden sein.                                                                                                                  | [**IWMProfile3:: kreatenewstreampriorisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 





