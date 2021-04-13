---
title: Windows Media Format SDK-Funktionen
description: Functions
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows Media-Format-SDK, Funktionen
- Advanced Systems Format (ASF), Funktionen
- ASF (Advanced Systems Format), Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cab464c3384a65776b993c2423f174debd7a89d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391370"
---
# <a name="windows-media-format-sdk-functions"></a>Windows Media Format SDK-Funktionen

Das Windows Media-Format SDK umfasst Funktionen zum Erstellen von Objekten und Hilfsfunktionen, um einige Prozeduren zu vereinfachen.

Dieses SDK unterstützt die folgenden Funktionen für die anfängliche Erstellung von Objekten. Wenn ein Objekt nicht unten aufgeführt ist, müssen Sie es mithilfe einer Schnittstelle aus einem anderen Objekt erstellen. Weitere Informationen finden Sie unter [Objekte](objects.md).



| Funktion                                                                             | BESCHREIBUNG                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wmcheckurlextension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Untersucht die Dateinamenerweiterung in der URL oder dem Dateinamen, der als Argument an Sie übermittelt wird.                                                               |
| [**Wmcheckurlscheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Prüft ein Netzwerkprotokoll und vergleicht es mit einer internen Liste unterstützter Schemas.                                                                    |
| [**Wmkreatebackuprestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Erstellt ein Backup Restorer-Objekt.                                                                                                                       |
| [**Wmkreatecertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Umschließt die Zertifikate des Benutzers in ein-Objekt.                                                                                                           |
| [**Wmkreatedeviceregistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Erstellt ein Geräte Registrierungs Objekt.                                                                                                                   |
| [**Wmkreatedrmtranszenryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Erstellt ein DRM-transryptorobjekt.                                                                                                                      |
| [**Wmkreateeditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Erstellt ein Metadateneditor-Objekt.                                                                                                                       |
| [**Wmkreateingedexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Erstellt ein Indexer-Objekt.                                                                                                                              |
| [**Wmkreatelicenserevocationagent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Erstellt ein Lizenz Sperr-Agent-Objekt.                                                                                                              |
| [**Wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Erstellt ein Profil-Manager-Objekt.                                                                                                                       |
| [**Wmkreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Erstellt ein Reader-Objekt.                                                                                                                                |
| [**Wmkreatesecurechannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Erstellt ein Objekt, das [**iwmsecurechannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                         |
| [**Wmkreatesecurechannel \_ zertifiziert**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Erstellt ein Objekt, das [**iwmsecurechannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                         |
| [**Wmkreatesecurechannel \_ Certified \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Erstellt ein Objekt, das [**iwmsecurechannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                        |
| [**Wmkreatesecurechannel \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Erstellt ein Objekt, das [**iwmsecurechannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)implementiert.                                                                         |
| [**Wmkreatesynkreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Erstellt ein synchrones Reader-Objekt.                                                                                                                    |
| [**Wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Erstellt ein Writer-Objekt.                                                                                                                                |
| [**Wmkreateschreiterfilesink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Erstellt ein Writer-dateisink-Objekt.                                                                                                                      |
| [**Wmkreateschreiternetworksink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Erstellt ein Writer-netzwerksenksobjekt.                                                                                                                   |
| [**Wmkreateschreiterpushsink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Erstellt ein Writer-Push-Sink-Objekt.                                                                                                                      |
| [**Wmisavailableoffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Überprüft, ob eine ASF-Datei von einer zwischengespeicherten Kopie wiedergegeben werden kann.                                                                                             |
| [**Wmiscontentprotected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Überprüft eine Datei auf vom DRM geschützten Inhalt.                                                                                                                |
| [**Wmvalidatedata**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Mit dieser Option wird überprüft, ob Daten vom Anfang einer Datei mit dem Header Abschnitt eines Dateityps konsistent sind, der vom SDK für den Windows Media-Format unterstützt wird. |



 

Die folgenden Funktionen stellen bequeme Verknüpfungen zum Analysieren von Dateien bereit.



| Funktion                                             | BESCHREIBUNG                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wmcheckurlextension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Versucht anhand der Dateinamenerweiterung zu ermitteln, ob eine Datei durch die Objekte des Windows Media Format SDK lesbar ist.              |
| [**Wmcheckurlscheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Bestimmt, ob ein Netzwerkprotokoll von den Objekten des Windows Media Format SDK unterstützt wird.                                           |
| [**Wmisavailableoffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Bestimmt, ob eine Datei für die Offline Wiedergabe verfügbar ist.                                                                                 |
| [**Wmiscontentprotected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Überprüft eine Datei auf vom DRM geschützten Inhalt.                                                                                                     |
| [**Wmvalidatedata**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Versucht zu bestimmen, ob eine Datei durch die Objekte des Windows Media Format SDK lesbar ist, indem Daten am Anfang der Datei analysiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
