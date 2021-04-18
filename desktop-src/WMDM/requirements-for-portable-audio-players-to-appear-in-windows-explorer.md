---
title: Anforderungen für tragbare Audioplayer, die im Windows-Explorer angezeigt werden
description: Anforderungen für tragbare Audioplayer, die im Windows-Explorer angezeigt werden
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Device Manager, Portable Audioplayer
- Device Manager, Portable Audioplayer
- Programmier Handbuch, Portable Audioplayer
- Dienstanbieter, Portable Audioplayer
- Erstellen von Dienstanbietern, portablen Audioplayern
- Portable Audioplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340837"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Anforderungen für tragbare Audioplayer, die im Windows-Explorer angezeigt werden

Die Portable Audioplayer-Shell-Namespace Erweiterung bietet Windows-Benutzern eine konsistente Möglichkeit, Audiogeräte zu verwalten, die von Windows Media Device Manager verwaltet werden. Wenn Sie den Dienstanbieter und die Treiber Komponenten gemäß den folgenden Richtlinien erstellen, wird Ihr Gerät im Shell-Namespace angezeigt. Benutzer können in Windows-Explorer auf konsistente Weise mit den Inhalten Ihres Geräts interagieren, um grundlegende Vorgänge wie das Kopieren, löschen und Umbenennen auszuführen.

Die folgenden shellanforderungen für Dienstanbieter und Treiber Komponenten dienen dazu, die allgemeinen Richtlinien für Windows Media-Device Manager zu ergänzen.

Gerätefunktionen

Windows Media Device Manager-Dienstanbieter sollten in Ihren unterstützten Funktionen explizit sein. Wenn ein-Befehl nicht unterstützt wird, muss ein Fehlercode zurückgegeben werden. Die entsprechenden Felder müssen für das vorhanden sein oder Fehlen von Funktionen für die Rückgabe der folgenden Funktionen festgelegt werden:

-   [**Imdspstorageglobals:: getfunktionen**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**Imdspstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**Imdspdevice:: getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Dienstanbieter müssen die folgenden Funktionen unterstützen, um mit der Shell kompatibel zu sein:

-   Kopieren auf das Gerät (mit Unterstützung für Abbruch-und Fortschritts Rückrufe)
-   Datei von Gerät löschen (mit Unterstützung für Abbruch-und Fortschritts Rückrufe)
-   Datei auf Gerät umbenennen
-   Speicherplatz Berichterstattung (Gesamter Speicherplatz, freier Speicherplatz, nicht verwendbar)
-   Plug & Play (siehe [Aktivieren von PNP für Geräte](enabling-pnp-for-devices.md))
-   Format (vorzugsweise mit Unterstützung für Abbruch-und Fortschritts Rückrufe)

Wenn Metadaten unterstützt werden, müssen die folgenden Felder für einzelne Dateien unterstützt werden. Wenn keine Daten verfügbar sind, sollte das Feld als leere Zeichenfolge initialisiert werden:



| Feld        | Konstante (in WMDM. idl definiert) | Metadatentag    |
|--------------|--------------------------------|-----------------|
| Titeltitel   | g \_ wszwmdmtitle                | WMDM/Titel      |
| Nachverfolgen der Nummer | g \_ wszwmdmtrack                | WMDM/Track      |
| Interpret       | g \_ wszwmdmauthor               | WMDM/Autor     |
| Aufzunehmen        | g \_ wszwmdmalbumtitle           | WMDM/albumtitle |
| Year         | g \_ wszwmdmyear                 | WMDM/Jahr       |
| Genre        | g \_ wszwmdmgenre                | WMDM/Genre      |



 

Parallelität

Kernelmodustreiber für Windows Media Device Manager müssen bei der Behandlung des gleichzeitigen Zugriffs robust sein. Beispielsweise kann ein Benutzer gleichzeitig sowohl über die Shell als auch über den Media Player oder einfach über mehrere Fenster in der Shell auf das Gerät zugreifen. Im Rahmen der Handhabung von Parallelität sollten Treiber nicht davon ausgehen, dass der Dienstanbieter geladen ist, dass das Gerät verwendet wird. Stattdessen sollten Sie einen Sperrmechanismus implementieren, um den Zugriff auf das Gerät nach Bedarf für einzelne Vorgänge zu serialisieren.

Benutzeroberfläche

Dienstanbieter für Windows Media Device Manager sollten keine Benutzeroberfläche anzeigen. Alle Fehler sollten von Methoden aufrufen als bestimmte Windows Media-Device Manager Fehlercodes zurückgegeben werden, wann immer dies möglich ist.

Aktivieren in der Shell

Wenn Ihr Paket alle shellanforderungen erfüllt, können Sie das Gerät in der Shell anzeigen lassen, indem Sie den *showinshell* -Wert unter den Geräteparametern auf 1 festlegen. Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




