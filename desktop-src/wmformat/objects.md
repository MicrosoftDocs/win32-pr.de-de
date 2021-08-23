---
title: Objekte (Windows Media Format 11 SDK)
description: Objekte
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows Medienformat-SDK,Objekte
- Advanced Systems Format (ASF),objects
- ASF (Advanced Systems Format),objects
- Objekte,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccd206a548093602f609a11ed11a8d98b910bc35eefb6ba55b985427ac1d212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707450"
---
# <a name="objects-windows-media-format-11-sdk"></a>Objekte (Windows Media Format 11 SDK)

Das Windows Media Format SDK verwendet mehrere Objekte zum Lesen, Schreiben, Bearbeiten und Indizieren von ASF-Dateien sowie zum Erstellen und Bearbeiten von Profilen. Jedes -Objekt unterstützt eine Reihe von Schnittstellen. Einige Schnittstellen werden in mehreren Objekten unterstützt. In diesen Fällen werden alle Unterschiede in der Implementierung im Referenzabschnitt für die Schnittstelle erläutert.

Die Objekte im Windows Media Format SDK sind COM-kompatibel. Um die Entwicklung zu vereinfachen, verfügt jedes Objekt über eine zugeordnete Erstellungsfunktion oder -methode. Sie sollten Objekte mithilfe der Erstellungsfunktion oder -methode erstellen, anstatt die COM-Funktion **CoCreateInstance manuell zu verwenden.**

An einige Schnittstellen wird eine Zahl angefügt, z. B. **IWMProfile2** und **IWMWriter3.** In jedem Fall erben die nummerierten Versionen alle Methoden der früheren Versionen und fügen neue Funktionen hinzu.

Auf jeder Objektseite dieses Verweises werden die schnittstellen, die im COM-Hauptobjekt enthalten sind, zuerst aufgeführt, gefolgt von Rückrufschnittstellen, die von der Anwendung implementiert werden müssen.

In der folgenden Tabelle sind die von diesem SDK unterstützten Objekte mit einer Beschreibung der Jeweiligen Funktionalität und der funktion aufgeführt, die zum Erstellen verwendet wird.



| Object                                                          | BESCHREIBUNG                                                                                                                                              | Erstellungsfunktion                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Sicherungswiederherstellung](backup-restorer-object.md)                   | Sichern von Lizenzen( in der Regel auf Wechselmedien) und Anschließend werden diese Lizenzen auf einem anderen Computer wiederhergestellt.                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Geräteregistrierung](device-registration-object.md)           | Verwaltet die Geräteregistrierungsdatenbank, die Einträge für Medienwiedergabegeräte enthält, die über eine Netzwerkverbindung verfügbar sind.             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [DRM-Transcryptor](drm-transcryptor-object.md)                 | Konvertiert DRM-geschützte Mediendaten in einen Datenstrom, der an Geräte gesendet werden kann, die das Windows Media DRM 10 for Network Devices-Protokoll verwenden. | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indexer](indexer-object.md)                                   | Erstellt einen Index für ASF-Dateien, um die Suche in Dateien mit Videostreams zu ermöglichen.                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Lizenzsperr-Agent](license-revocation-agent-object.md) | Verwaltet die Lizenzsperrung.                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Metadata Editor](metadata-editor-object.md)                   | Bearbeitet Metadaten in einem ASF-Dateiheader.                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Profil-Manager](profile-manager-object.md)                   | Stellt Schnittstellen zum Erstellen, Laden und Speichern von Profilen bereit. Zum Schreiben einer ASF-Datei ist ein Profil erforderlich.                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Leser](reader-object.md)                                     | Liest ASF-Dateien. Dieses Objekt verwendet ein asynchrones Aufrufmodell für seine Vorgänge.                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Synchroner Reader](synchronous-reader-object.md)             | Liest ASF-Dateien mit synchronen Aufrufen.                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Schriftsteller](writer-object.md)                                     | Schreibt ASF-Dateien.                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Writer-Dateisenke](writer-file-sink-object.md)                 | Steuert ASF-Dateien, die vom Writer-Objekt geschrieben wurden.                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Writer-Netzwerksenke](writer-network-sink-object.md)           | Steuert das Live-Netzwerkstreaming von ASF-Dateien, die vom Writer-Objekt geschrieben wurden.                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Writer-Pushsenke](writer-push-sink-object.md)                 | Steuert die Übermittlung von Streaminginhalten an Veröffentlichungsserver.                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

In der folgenden Tabelle sind Objekte aufgeführt, die von anderen -Objekten abhängig sind. Diese Objekte werden durch Methoden vorhandener Objekte erstellt.



| Object                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                           | Erstellungsmethode                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bandbreitenfreigabe](bandwidth-sharing-object.md)             | Verwaltet Informationen zur Bandbreitenfreigabe in einem Profil. Für ein Profil kann mehr als ein Bandbreitenfreigabeobjekt vorhanden sein. Es gibt verschiedene Methoden zum Erstellen eines Bandbreitenfreigabeobjekts, je nachdem, ob Sie ein neues Bandbreitenfreigabeobjekt erstellen oder auf ein vorhandenes zugreifen möchten.                                           | [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) Oder<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Enthält ein Medienbeispiel und alle zugeordneten Dateneinheitserweiterungen. Wird zum Schreiben und Lesen von Beispielen verwendet.                                                                                                                                                                                                                           | [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) Oder<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> oder<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> oder<br/> Wird automatisch vom Readerobjekt oder synchronen Readerobjekt für die Beispielbereitstellung erstellt.<br/> |
| [Eingabemedieneigenschaften](input-media-properties-object.md)   | Verwaltet die Eigenschaften einer Eingabe. Für jede Eingabe kann ein Eingabeeigenschaftenobjekt vorhanden sein.                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Gegenseitiger Ausschluss](mutual-exclusion-object.md)               | Verwaltet gegenseitige Ausschlussinformationen in einem Profil. Häufige Verwendungsmöglichkeiten für gegenseitigen Ausschluss sind Inhalte mit mehreren Bitraten und -n in mehreren Sprachen. Es gibt verschiedene Methoden zum Erstellen eines gegenseitigen Ausschlussobjekts, je nachdem, ob Sie ein neues objekt für gegenseitigen Ausschluss erstellen oder auf ein vorhandenes zugreifen möchten.         | [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) Oder<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Ausgabemedieneigenschaften](output-media-properties-object.md) | Verwaltet die Eigenschaften einer Ausgabe. Für jede Ausgabe kann ein Ausgabemedieneigenschaftenobjekt vorhanden sein. Diese Objekte können vom Reader oder vom synchronen Reader erstellt werden.                                                                                                                                                            | [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) Oder<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Profil](profile-object.md)                                 | Enthält die Daten in einem Profil, während es bearbeitet wird. Profilobjekte werden jedes Mal erstellt, wenn das Profil bearbeitet werden muss. Es gibt verschiedene Methoden zum Erstellen eines Profilobjekts, je nachdem, ob Sie ein neues Profil erstellen oder auf ein vorhandenes zugreifen möchten.                                                  | [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) Oder<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> oder<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> oder<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Streamkonfiguration](stream-configuration-object.md)       | Verwaltet die Eigenschaften eines Streams innerhalb eines Profils. Streamkonfigurationsobjekte werden von Streamobjekten jedes Mal erstellt, wenn Sie auf die Informationen zu einem Stream zugreifen müssen. Es gibt verschiedene Methoden zum Erstellen eines Streamkonfigurationsobjekts, je nachdem, ob Sie einen neuen Datenstrom erstellen oder auf einen vorhandenen Stream zugreifen möchten. | [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) Oder<br/> [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> oder<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Streampriorisierung](stream-prioritization-object.md)     | Verwaltet die Streamprioritätsliste für ein Profil. Die Streams werden in der Reihenfolge der zunehmenden Priorität gelöscht, wenn die verfügbare Bandbreite eingeschränkt ist. Es kann nur ein Streampriorisierungsobjekt in einem Profil vorhanden sein.                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 





