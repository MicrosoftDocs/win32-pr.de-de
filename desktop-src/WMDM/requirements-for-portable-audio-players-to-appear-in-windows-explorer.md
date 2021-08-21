---
title: Anforderungen für das Anzeigen portabler Audioplayer im Windows Explorer
description: Anforderungen für das Anzeigen portabler Audioplayer im Windows Explorer
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Medien Geräte-Manager, portable Audioplayer
- Geräte-Manager, portable Audioplayer
- Programmierhandbuch, portable Audioplayer
- Dienstanbieter,portable Audioplayer
- Erstellen von Dienstanbietern, portable Audioplayer
- Portable Audioplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d91e844f564ead03ddb78cf57c13c81a56bc8934bbfbde51c105b5c7e1e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055578"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Anforderungen für das Anzeigen portabler Audioplayer im Windows Explorer

Die Shellnamespaceerweiterung für portable Audioplayer bietet benutzern Windows eine konsistente Möglichkeit zum Verwalten von Audiogeräten, die von Windows Media Geräte-Manager. Wenn Sie Ihre Dienstanbieter- und Treiberkomponenten gemäß den folgenden Richtlinien erstellen, wird Ihr Gerät im Shellnamespace angezeigt. Benutzer können in Windows Explorer konsistent mit dem Inhalt Ihres Geräts interagieren, um grundlegende Vorgänge wie Kopieren, Löschen und Umbenennen durchzuführen.

Die folgenden Shellanforderungen für Dienstanbieter- und Treiberkomponenten sollen die allgemeinen Richtlinien Windows Media Geräte-Manager ergänzen.

Gerätefunktionen

Windows Media Geräte-Manager-Dienstanbieter sollten in ihren unterstützten Funktionen explizit sein. Wenn ein Aufruf nicht unterstützt wird, muss ein Fehlercode zurückgegeben werden. Die entsprechenden Felder müssen für das Vorhandensein oder Fehlen von Funktionen bei rückgabe der folgenden Funktionen festgelegt werden:

-   [**IMDSPStorageGlobals::GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Dienstanbieter müssen die folgenden Funktionen unterstützen, um mit der Shell kompatibel zu sein:

-   Kopieren auf das Gerät (mit Unterstützung für Rückrufe zum Abbrechen und Status)
-   Datei vom Gerät löschen (mit Unterstützung für Rückrufe zum Abbrechen und Status)
-   Umbenennen der Datei auf dem Gerät
-   Speicherplatzberichterstellung (Gesamtspeicherplatz, freier Speicherplatz, nicht verwendbarer Speicherplatz)
-   Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))
-   Format (vorzugsweise mit Unterstützung für Abbrechen und Statusrückrufe)

Wenn Metadaten unterstützt werden, müssen die folgenden Felder für einzelne Dateien unterstützt werden. Wenn keine Daten verfügbar sind, sollte das Feld als leere Zeichenfolge initialisiert werden:



| Feld        | Konstante (definiert in WMDM.idl) | Metadatentag    |
|--------------|--------------------------------|-----------------|
| Titel des Titels   | g \_ wszWMDMTitle                | WMDM/Titel      |
| Track Number | g \_ wszWMDMTrack                | WMDM/Track      |
| Künstler       | g \_ wszWMDMAuthor               | WMDM/Author     |
| Album        | g \_ wszWMDMItätTitle           | WMDM/AlbumTitle |
| Jahr         | g \_ wszWMDMYear                 | WMDM/Jahr       |
| Genre        | g \_ wszWMDMGenre                | WMDM/Genre      |



 

Parallelität

Kernelmodustreiber für Windows Media Geräte-Manager müssen bei der Verarbeitung des gleichzeitigen Zugriffs stabil sein. Beispielsweise kann ein Benutzer gleichzeitig über die Shell und den Media Player oder einfach über mehrere Fenster in der Shell auf das Gerät zugreifen. Im Rahmen der Behandlung von Parallelität sollten Treiber nicht davon ausgehen, dass das Gerät verwendet wird, nur weil der Dienstanbieter geladen ist. Stattdessen sollten sie einen Sperrmechanismus implementieren, um den Zugriff auf das Gerät bei Bedarf für einzelne Vorgänge zu serialisieren.

Benutzeroberfläche

Dienstanbieter für Windows Media Geräte-Manager sollten keine Benutzeroberfläche anzeigen. Alle Fehler sollten von Methodenaufrufen nach Möglichkeit als Windows Media Geräte-Manager zurückgegeben werden.

Aktivieren in der Shell

Wenn Ihr Paket alle Shellanforderungen erfüllt, können Sie das Anzeigen Ihres Geräts in der Shell aktivieren, indem Sie den *ShowInShell-Wert* unter den Geräteparametern auf 1 festlegen. Weitere Informationen finden Sie unter [Geräteparameter.](device-parameters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




