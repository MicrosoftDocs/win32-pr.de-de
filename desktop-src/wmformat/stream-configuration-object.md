---
title: Stream-Konfigurationsobjekt
description: Stream-Konfigurationsobjekt
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Medienformat-SDK, Streamkonfigurationsobjekte
- Advanced Systems Format (ASF), Streamkonfigurationsobjekte
- ASF (Advanced Systems Format), Streamkonfigurationsobjekte
- Objekte,Streamkonfigurationsobjekte
- Streamkonfigurationsobjekte
- Streams, Streamkonfigurationsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e71be6149df3f2da0edba31d9c5803d86a6fd89189e1fc339cf99593336415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929380"
---
# <a name="stream-configuration-object"></a>Stream-Konfigurationsobjekt

Ein Streamkonfigurationsobjekt wird verwendet, um die Eigenschaften eines Medienstreams in einer ASF-Datei anzugeben. Streamkonfigurationsobjekte können für vorhandene Streams in einem Profil oder leer erstellt werden, um neue Daten zu empfangen. Streamkonfigurationsobjekte können nicht unabhängig von einem Profilobjekt vorhanden sein. Um den Inhalt eines Streamkonfigurationsobjekts zu speichern, müssen Sie [**entweder IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) aufrufen, um einen neuen Stream hinzuzufügen, oder [**IWMProfile::ReconfigStream,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) um an einem vorhandenen Stream vorgenommene Änderungen zu speichern.

Verwenden Sie eine der folgenden Methoden, um ein Streamkonfigurationsobjekt zu erstellen.



| Methode                                                                | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Erstellt ein Streamkonfigurationsobjekt ohne Daten.                                                                          |
| [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Erstellt ein Streamkonfigurationsobjekt, das mit Daten aus einem Profil aufgefüllt wird. Verwendet den Streamindex, um den gewünschten Stream zu identifizieren.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Erstellt ein Streamkonfigurationsobjekt, das mit Daten aus einem Profil aufgefüllt wird. Verwendet die Streamnummer, um den gewünschten Stream zu identifizieren. |



 

Alle Methoden in der obigen Tabelle legen einen Zeiger auf eine **IWMStreamConfig-Schnittstelle** fest. Die anderen Schnittstellen des Streamkonfigurationsobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom Streamkonfigurationsobjekt unterstützt.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Legt die [**WM \_ MEDIA \_ TYPE-Struktur für**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) den Stream fest und ruft sie ab.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Legt Eigenschaften fest und ruft diese ab, die nicht für alle Streams erforderlich sind, z. B. VBR-Einstellungen (Variable Bit Rate).                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Legt alle grundlegenden Informationen zu einem Stream fest und ruft sie ab.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Konfiguriert die Typen von Dateneinheitserweiterungen, die dem Stream zugeordnet sind. Erbt alle Methoden von **IWMStreamConfig.** |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Legt die Sprache für den Stream fest und ruft sie ab. Erbt alle Methoden von **IWMStreamConfig** und **IWMStreamConfig2.** |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Verwaltet die Eigenschaften eines Videostreams. Dies ist eine optionale Schnittstelle und nur für Videostreams verfügbar.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> </dl>

 

 




