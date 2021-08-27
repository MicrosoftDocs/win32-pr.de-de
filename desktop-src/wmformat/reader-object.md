---
title: Reader-Objekt
description: Reader-Objekt
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Medienformat-SDK, Readerobjekte
- Advanced Systems Format (ASF), Readerobjekte
- ASF (Advanced Systems Format), Readerobjekte
- Objekte, Readerobjekte
- Readerobjekte, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1c01b824bbe278991f1512e963a6dde1727c00e73b3c17f5ab4c5556534b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089709"
---
# <a name="reader-object"></a>Reader-Objekt

Das Readerobjekt liest Datenbeispiele aus Mediendateien. Das Readerobjekt unterstützt derzeit Dateien mit der ASF-Dateistruktur (Advanced Systems Format) sowie MP3-Dateien. Die vom Readerobjekt übermittelten Daten sind standardmäßig nicht komprimiert und können standardmäßig gerendert werden. Beispiele können jedoch übermittelt werden, ohne bei Bedarf dekomprimiert zu werden. Beispiele werden asynchron vom Readerobjekt übermittelt. Sie müssen eine Rückruffunktion einrichten, um sie zu empfangen. Verwenden Sie für die synchrone Wiedergabe von ASF-Dateien das synchrone Readerobjekt. Weder der Reader noch der synchrone Reader rendert Daten. Sie müssen eigene Renderingroutinen bereitstellen, um die aus einer Datei abgerufenen Medien anzuzeigen.

Wenn eine Datei codierte Medien enthält, die mit einem vom Readerobjekt unterstützten Codec decodiert werden können, können Sie das Format der nicht komprimierten Ausgabe steuern. Um das Format der dekomprimierten Ausgabe für einen Stream zu ändern, müssen Sie das Standardobjekt der Ausgabemedieneigenschaften für diesen Stream abrufen, Änderungen daran vornehmen und es dem Stream im Reader neu zuweisen. Ausgabemedieneigenschaftenobjekte sind dem Readerobjekt untergeordnet und sollten nur mithilfe der [**IWMReader::GetOutputProps-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) erstellt werden.

Das Readerobjekt wird von der [**Funktion WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)erstellt, die einen Zeiger auf eine **IWMReader-Schnittstelle** festlegt. Die anderen Schnittstellen des Readerobjekts können durch Aufrufen der **QueryInterface-Methode** abgerufen werden.

Die folgenden Schnittstellen werden vom Readerobjekt unterstützt.



| Schnittstelle                                                    | BESCHREIBUNG                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | Ermöglicht den Zugriff auf die vom Reader verwendete Systemuhr.                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Verwaltet den Lizenzerwerb, [*DRM-Eigenschaften*](wmformat-glossary.md) und die Individualisierung von Clients.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Bietet Zugriff auf Lizenzen, die Ausgabeschutzebenen (Output Protection Levels, OPL) verwenden, um Rechte anzugeben.                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Legt Headerinformationen fest und ruft diese ab, einschließlich Metadaten, [*Marker*](wmformat-glossary.md)und Skriptdaten.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Ruft Informationen zu den Codecs ab, die zum Codieren des Inhalts in der Datei verwendet wurden. Erbt alle Methoden von **IWMHeaderInfo.**                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Unterstützt große Attributgrößen, doppelte Attributnamen und Unterstützung mehrerer Sprachen. Erbt alle Methoden von **IWMHeaderInfo** und **IWMHeaderInfo2.**              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Ruft die Größe des größten Pakets in der Im Reader geladenen Datei ab.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Ruft die Größe des kleinsten Pakets in der Im Reader geladenen Datei ab.                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | Ermöglicht den Zugriff auf die Profilinformationen der im Reader geladenen Datei.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Ruft den GUID (Globally Unique Identifier) ab, sofern vorhanden, der dem Profil zugeordnet ist. Erbt alle Methoden von **IWMProfile.**                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Unterstützt bandbreitenfreigabe- und Streampriorisierungsinformationen im Profil. Erbt alle Methoden von **IWMProfile** und **IWMProfile2.**                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Stellt grundlegende Funktionen zum Lesen von Dateien bereit, einschließlich Vorgänge wie Öffnen, Schließen, Starten, Anhalten, Fortsetzen, Beenden und Abrufen und Festlegen der Ausgabeeigenschaften.                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Kommuniziert mit der DirectX-Videobeschleunigung.                                                                                                                                   |
| [**IWMReaderErweitert**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Stellt erweiterte Features des Readers bereit, z. B. eine vom Benutzer bereitgestellte Uhr, Pufferzuordnung, Rückgabestatistiken und Datenstromauswahlbenachrichtigungen.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Stellt einen zusätzlichen Bereich erweiterter Methoden für ein vorhandenes Readerobjekt bereit. Erbt alle Methoden von **IWMReaderErweitert.**                                           |
| [**IWMReaderErweitert3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Bietet erweiterte Such- und Streamingsteuerelement. Erbt alle Methoden von **IWMReaderAdvanced** und **IWMReaderAdvanced2.**                                               |
| [**IWMReaderErweitert4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Stellt erweiterte Readeroptionen bereit, einschließlich Unterstützung mehrerer Sprachen. Erbt alle Methoden von **IWMReaderAdvanced**, **IWMReaderAdvanced2** und **IWMReaderAdvanced3**. |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Steuert die Netzwerkkonfigurationseinstellungen.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Bietet Zugriff auf erweiterte Netzwerkkonfigurationseinstellungen. Erbt alle Methoden von **IWMReaderNetworkConfig.**                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Legt Timer für Streamuhren fest und bricht sie ab und ruft den aktuellen Wert einer angegebenen Streamuhr ab.                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Stellt Informationen zu SMPTE-Zeitcodebereichen in der im Reader geladenen Datei bereit.                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Testet, ob Änderungen an den Ausgabeeigenschaften eines Streams ordnungsgemäß funktionieren.                                                                                                |



 

Die folgenden Rückrufschnittstellen können in der Anwendung implementiert werden, um den Fortschritt eines Readerobjekts nachzuverfolgen.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Übernimmt die Anmeldeinformationen von Benutzern und überprüft, ob sie über die Berechtigung für den Zugriff auf einen Remotestandort verfügen.                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Stellt erweiterte Alternativen zu den **AllocateForOutput-** und **AllocateForStream-Methoden** der **IWMReaderCallbackAdvanced-Schnittstelle bereit.** |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Stellt Rückrufmethoden für die **Start-** und **Open-Methoden** von **IWMReader** bereit.                                                            |
| [**IWMReaderCallbackErweitert**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Stellt Rückrufmethoden für die Methoden der [**IWMReaderAdvanced-Schnittstelle bereit.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Erforderlich, wenn Statusinformationen an die Hostanwendung übermittelt werden müssen.                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> </dl>

 

 




