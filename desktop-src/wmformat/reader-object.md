---
title: Reader-Objekt
description: Reader-Objekt
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Media-Format-SDK, Reader-Objekte
- Advanced Systems Format (ASF), Reader-Objekte
- ASF (Advanced Systems Format), Reader-Objekte
- Objekte, Reader-Objekte
- Reader-Objekte, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7958689fa7744286c92c294219fb2c963e55c860
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390099"
---
# <a name="reader-object"></a>Reader-Objekt

Das Reader-Objekt liest Daten Beispiele aus Mediendateien. Das Reader-Objekt unterstützt derzeit Dateien mit der Dateistruktur "Advanced Systems Format (ASF)" und MP3-Dateien. Die vom Reader-Objekt übermittelten Daten sind nicht komprimiert und können standardmäßig bereitgestellt werden, obwohl Stichproben bei Bedarf übermittelt werden können. Beispiele werden asynchron aus dem Reader-Objekt übermittelt. Sie müssen eine Rückruffunktion einrichten, um Sie zu empfangen. Verwenden Sie für die synchrone Wiedergabe von ASF-Dateien das synchrone Reader-Objekt. Weder der Reader noch der synchrone Reader rendert Daten. Sie müssen ihre eigenen renderingroutinen bereitstellen, um die aus einer Datei abgerufenen Medien anzuzeigen.

Wenn eine Datei codierte Medien enthält, die mit einem vom Reader-Objekt unterstützten Codec decodiert werden können, können Sie das Format der nicht komprimierten Ausgabe steuern. Um das Format der dekomprimierten Ausgabe für einen Stream zu ändern, müssen Sie das Standardeigenschaften Objekt für Ausgabemedien für diesen Stream abrufen, Änderungen daran vornehmen und es dem Stream im Reader erneut zuweisen. Die Eigenschaften der Ausgabemedien Eigenschaften sind dem Reader-Objekt untergeordnet und sollten nur mit der [**iwmreader:: getOutputProperties**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) -Methode erstellt werden.

Das Reader-Objekt wird von der [**wmkreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)-Funktion erstellt, mit der ein Zeiger auf eine **iwmreader** -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Reader-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Reader-Objekt unterstützt.



| Schnittstelle                                                    | BESCHREIBUNG                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | Bietet Zugriff auf die vom Reader verwendete Systemuhr.                                                                                                                         |
| [**Iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Verwaltet den Lizenzerwerb, [*DRM*](wmformat-glossary.md) -Eigenschaften und die Client Individualisierung.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Bietet Zugriff auf Lizenzen, die für die Angabe von Rechten die Ausgabe Schutz Ebenen (OPL) verwenden.                                                                                          |
| [**Iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Legt Header Informationen, einschließlich Metadaten, [*Markierungen*](wmformat-glossary.md)und Skript Daten, fest und ruft diese ab.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Ruft Informationen zu den Codecs ab, die zum Codieren des Inhalts in der Datei verwendet wurden. Erbt alle Methoden von **iwmheaderinfo**.                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Unterstützt umfangreiche Attribut Größen, doppelte Attributnamen und Unterstützung mehrerer Sprachen. Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**.              |
| [**Iwmpacketsize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Ruft die Größe des größten Pakets in der Datei ab, das in den Reader geladen wurde.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Ruft die Größe des kleinsten Pakets in der Datei ab, die im Reader geladen wurde.                                                                                                     |
| [**Iwmprofile**](iwmprofile.md)                             | Ermöglicht den Zugriff auf die Profilinformationen der Datei, die im Reader geladen wurde.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Ruft die Globally Unique Identifier (GUID) ab, die dem Profil zugeordnet ist, sofern vorhanden. Erbt alle Methoden von **iwmprofile**.                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Unterstützt die Bandbreiten Freigabe und Datenstrom Priorisierungs Informationen im Profil. Erbt alle Methoden von **iwmprofile** und **IWMProfile2**.                             |
| [**Iwmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Bietet grundlegende Funktionen zum Lesen von Dateien, einschließlich der Vorgänge zum Öffnen, schließen, starten, anhalten, fortsetzen, beenden und zum Festlegen und Festlegen der Ausgabe Eigenschaften.                  |
| [**Iwmreaderaccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Kommuniziert mit der DirectX-Videobeschleunigung.                                                                                                                                   |
| [**Iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Bietet erweiterte Funktionen des Readers, z. b. eine vom Benutzer bereitgestellte Uhr, Puffer Zuordnung, Rückgabe Statistiken und streamauswahlbenachrichtigungen.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Stellt einen zusätzlichen Bereich von erweiterten Methoden für ein vorhandenes Reader-Objekt bereit. Erbt alle Methoden von **iwmreaderadvanced**.                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Bietet erweiterte Such-und streamingsteuerung. Erbt alle Methoden von **iwmreaderadvanced** und **IWMReaderAdvanced2**.                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Bietet erweiterte Reader-Optionen einschließlich Unterstützung mehrerer Sprachen. Erbt alle Methoden von **iwmreaderadvanced**, **IWMReaderAdvanced2** und **IWMReaderAdvanced3**. |
| [**Iwmreadernetworkconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Steuert die Netzwerk Konfigurationseinstellungen.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Bietet Zugriff auf Erweiterte Netzwerk Konfigurationseinstellungen. Erbt alle Methoden von **iwmreadernetworkconfig**.                                                          |
| [**Iwmreaderstreamclock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Legt Timer für Datenstrom Uhren fest und bricht Sie ab und ruft den aktuellen Wert einer angegebenen streamuhr ab.                                                                          |
| [**Iwmreadertimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Stellt Informationen zu SMPTE-Zeit Codebereichen in der Datei bereit, die im Reader geladen wurde.                                                                                             |
| [**Iwmreadertypenegotiziierung**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Testet, ob Änderungen an den Ausgabe Eigenschaften eines Streams ordnungsgemäß funktionieren.                                                                                                |



 

Die folgenden Rückruf Schnittstellen können in der Anwendung implementiert werden, um den Fortschritt eines Reader-Objekts zu verfolgen.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmkredentialcallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Ruft die Anmelde Informationen von Benutzern ab und überprüft, ob Sie über die Berechtigung zum Zugreifen auf eine Remote Website verfügen.                                               |
| [**Iwmreaderzuweisung**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Stellt erweiterte Alternativen zu den Methoden " **zuweicateforoutput** " und " **zuweicateforstream** " der **iwmreadercallbackadvanced** -Schnittstelle bereit. |
| [**Iwmreadercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Stellt Rückruf Methoden für die **Start** -und **Open** -Methoden von **iwmreader** bereit.                                                            |
| [**Iwmreadercallbackadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Stellt Rückruf Methoden für die Methoden der [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle bereit.                                    |
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen.                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> </dl>

 

 




