---
description: Geräte Darstellung
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Geräte Darstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484739"
---
# <a name="device-representation"></a>Geräte Darstellung

Geräte verfügen über zwei Haupt Verhaltensweisen, die von der WPD-Architektur (Windows Portable Devices) adressiert werden:

-   Zugreifen auf und Speichern von Inhalten Beispielsweise müssen Anwendungen in der Lage sein, einem tragbaren Musikplayer Musikdateien hinzuzufügen.
-   Programmieren des Geräts. Dies schließt einfache Vorgänge ein, z. b. das Ändern von Einstellungen und das Vorbereiten des Geräts für die Datenerfassung oder komplexere Vorgänge wie das Hochladen von Firmware. Beispiele hierfür sind das Ausgeben eines Befehls "Bildaufnahme" an eine digitale, immer noch Kamera.

In WPD werden diese Verhaltensweisen durch das darstellen des Geräts als Hierarchie von Objekten beschrieben. Die folgende Abbildung zeigt eine WPD-Objektdarstellung für ein Gerät mit mehreren Funktionen, bei dem es sich in diesem Fall um ein Mobiltelefon handelt.

![Abbildung der Hierarchie von Objekten für ein Mobiltelefon](images/wpd-overview-figure3.gif)

Diese Hierarchie veranschaulicht die folgenden Funktionen und Inhalte.

Alitäts

-   Speicher Objekt. Dieses Gerät verfügt über Datenspeicher.
-   Kontakt Dienst. Dieser Dienst ist ein funktionales Objekt, das zum Synchronisieren und Speichern von Kontakten auf dem Telefon verwendet werden kann.
-   SMS-Dienst. Dieser Dienst ist ein funktionales Objekt, das zum Senden, empfangen und Speichern von SMS-Nachrichten verwendet werden kann.

Inhalte:

-   Medienobjekte. Dieses Gerät speichert Bild-, Musik-und Videodateien in Ordnern des Speicher Objekts. Obwohl die in der Abbildung gezeigten Dateien unter einem Ordner gespeichert werden, kann ein Gerät Inhalte in Ordner unterteilen, die nach dem gespeicherten Medientyp angeordnet sind. beispielsweise Bildordner, Musik Ordner und Videoordner.
-   Contact-Objekte. Dieses Gerät speichert Kontaktinformationen (z. b. Name, Telefonnummer und Adresse) als untergeordnete Elemente des Contacts-Dienstanbieter.
-   Nachrichten Objekte. Dieses Gerät speichert SMS-Nachrichten als untergeordnete Elemente des SMS-Dienstanbieter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungs Übersicht**](application-overview.md)
</dt> </dl>

 

 



