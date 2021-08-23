---
title: Windows Media Format SDK-Funktionen
description: Funktionen
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows Medienformat-SDK, Funktionen
- Advanced Systems Format (ASF), Funktionen
- ASF (Advanced Systems Format), Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560756451ee2f5b49d26b5611b38a40a45cac7643b101fdbe8ae492386901689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708260"
---
# <a name="windows-media-format-sdk-functions"></a>Windows Media Format SDK-Funktionen

Das Windows Media Format SDK enthält Funktionen zum Erstellen von Objekten und Hilfsfunktionen, um einige Prozeduren zu vereinfachen.

Dieses SDK unterstützt die folgenden Funktionen für die anfängliche Erstellung von -Objekten. Wenn ein Objekt unten nicht aufgeführt ist, müssen Sie es mithilfe einer Schnittstelle aus einem anderen Objekt erstellen. Weitere Informationen finden Sie unter [Objekte](objects.md).



| Funktion                                                                             | Beschreibung                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Überprüft die Dateinamenerweiterung in der URL oder dem Dateinamen, die als Argument übergeben wird.                                                               |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Überprüft ein Netzwerkprotokoll und vergleicht es mit einer internen Liste unterstützter Schemas.                                                                    |
| [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Erstellt ein Sicherungswiederherstellungsobjekt.                                                                                                                       |
| [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Umschließt die Zertifikate des Benutzers in ein -Objekt.                                                                                                           |
| [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Erstellt ein Geräteregistrierungsobjekt.                                                                                                                   |
| [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Erstellt ein DRM-Transcryptorobjekt.                                                                                                                      |
| [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Erstellt ein Metadaten-Editor-Objekt.                                                                                                                       |
| [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Erstellt ein Indexerobjekt.                                                                                                                              |
| [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Erstellt ein Lizenzsperr-Agent-Objekt.                                                                                                              |
| [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Erstellt ein Profil-Manager-Objekt.                                                                                                                       |
| [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Erstellt ein Readerobjekt.                                                                                                                                |
| [**WMCreateSecureChannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Erstellt ein Objekt, das [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                         |
| [**WMCreateSecureChannel \_ Certified**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Erstellt ein Objekt, das [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                         |
| [**WMCreateSecureChannel \_ Certified \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Erstellt ein Objekt, das [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                        |
| [**WMCreateSecureChannel \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Erstellt ein Objekt, das [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                         |
| [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Erstellt ein synchrones Readerobjekt.                                                                                                                    |
| [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Erstellt ein Writer-Objekt.                                                                                                                                |
| [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Erstellt ein Writerdatei-Senkenobjekt.                                                                                                                      |
| [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Erstellt ein Writer-Netzwerksenkenobjekt.                                                                                                                   |
| [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Erstellt ein Writer-Pushsenkenobjekt.                                                                                                                      |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Überprüft, ob eine ASF-Datei aus einer zwischengespeicherten Kopie wiedergegeben werden kann.                                                                                             |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Überprüft eine Datei auf DRM-geschützte Inhalte.                                                                                                                |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Überprüft, ob daten vom Anfang einer Datei mit dem Headerabschnitt eines Dateityps konsistent sind, der vom Windows Media Format SDK unterstützt wird. |



 

Die folgenden Funktionen stellen praktische Verknüpfungen zum Analysieren von Dateien bereit.



| Funktion                                             | Beschreibung                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Versucht anhand der Dateinamenerweiterung zu bestimmen, ob eine Datei von den Objekten des Windows Media Format SDK gelesen werden kann.              |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Bestimmt, ob ein Netzwerkprotokoll von den Objekten des Windows Media Format SDK unterstützt wird.                                           |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Bestimmt, ob eine Datei für die Offlinewiedergabe verfügbar ist.                                                                                 |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Überprüft eine Datei auf DRM-geschützte Inhalte.                                                                                                     |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Versucht zu bestimmen, ob eine Datei von den Objekten des Windows Media Format SDK gelesen werden kann, indem Daten am Anfang der Datei analysiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
