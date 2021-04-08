---
title: Stream-Konfigurationsobjekt
description: Stream-Konfigurationsobjekt
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media-Format-SDK, Datenstrom-Konfigurationsobjekte
- Advanced Systems Format (ASF), streamkonfigurationsobjekte
- ASF (Advanced Systems Format), Datenstrom-Konfigurationsobjekte
- Objekte, streamkonfigurationsobjekte
- Stream-Konfigurationsobjekte
- Streams, streamkonfigurationsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101347"
---
# <a name="stream-configuration-object"></a>Stream-Konfigurationsobjekt

Ein Datenstrom-Konfigurationsobjekt wird verwendet, um die Eigenschaften eines Mediendaten Stroms in einer ASF-Datei anzugeben. Stream-Konfigurationsobjekte können für vorhandene Datenströme in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen. Streamkonfigurationsobjekte können nicht unabhängig von einem Profil Objekt vorhanden sein. Zum Speichern des Inhalts eines Datenstrom-Konfigurations Objekts müssen Sie entweder [**iwmprofile:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) zum Hinzufügen eines neuen Streams oder [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) zum Speichern von Änderungen, die an einem vorhandenen Stream vorgenommen wurden, hinzufügen.

Verwenden Sie zum Erstellen eines Datenstrom-Konfigurations Objekts eine der folgenden Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmprofile:: kreatenewstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Erstellt ein Datenstrom-Konfigurationsobjekt ohne Daten.                                                                          |
| [**Iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Erstellt ein Datenstrom-Konfigurationsobjekt, das mit Daten aus einem Profil aufgefüllt ist. Verwendet den streamindex, um den gewünschten Stream zu identifizieren.  |
| [**Iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Erstellt ein Datenstrom-Konfigurationsobjekt, das mit Daten aus einem Profil aufgefüllt ist. Verwendet die Datenstrom Nummer, um den gewünschten Stream zu identifizieren. |



 

Alle Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmstreamconfig** -Schnittstelle fest. Die anderen Schnittstellen des Datenstrom-Konfigurations Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Datenstrom-Konfigurationsobjekt unterstützt.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmmedia-Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Legt die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für den Stream fest und ruft Sie ab.                                    |
| [**Iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Legt Eigenschaften fest, die nicht für alle Streams erforderlich sind, wie z. b. Einstellungen für Variablen Bitraten (VBR), und ruft diese ab.                  |
| [**Iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Legt alle grundlegenden Informationen zu einem Stream fest und ruft diese ab.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Konfiguriert die Typen von Dateneinheiten Erweiterungen, die dem Stream zugeordnet sind. Erbt alle Methoden von **iwmstreamconfig**. |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Legt die Sprache für den Stream fest und ruft Sie ab. Erbt alle Methoden von **iwmstreamconfig** und **IWMStreamConfig2**. |
| [**Iwmvideomedia-Eigenschaften**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Verwaltet die Eigenschaften eines Videostreams. Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> </dl>

 

 




