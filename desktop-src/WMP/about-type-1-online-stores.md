---
title: Informationen zu Typ 1 Online Stores
description: Informationen zu Typ 1 Online Stores
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Online Stores, geben Sie 1 Online Stores ein.
- Online Stores, Typ 1 Online Stores
- Geben Sie 1 Online Stores ein, Informationen zu
- Windows Media Player, geben Sie 1 Online Stores ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341506"
---
# <a name="about-type-1-online-stores"></a>Informationen zu Typ 1 Online Stores

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Microsoft Windows Media Player 11 unterstützt zwei Arten von Online Stores: Typ 1 und Typ 2. Die Speicher vom Typ 1 sind tiefer in Windows Media Player als die Speicher vom Typ 2 integriert. Ein Online Store vom Typ 1 stellt einen herunterladbaren Musikkatalog bereit, damit Windows Media Player dem Benutzer den Inhalt des Stores zur Verfügung stellen kann, als ob der Inhalt in der lokalen Medienbibliothek des Benutzers enthalten wäre.

Ein Onlinespeicher vom Typ 1 muss ein Plug-in bereitstellen, das die [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -Schnittstelle implementiert. Wenn der Benutzer in der Windows Media Player-Benutzeroberfläche navigiert, ruft der Player das Plug-in auf, damit der Online Shop die Benutzerfreundlichkeit durch Bereitstellen von Webseiten verbessern kann, die im Player angezeigt werden.

Zu den Features vom Typ 1 Online Stores, die Sie von den Geschäften vom Typ 2 unterscheiden, gehören die folgenden:

-   **Einfache Verwendung.** Benutzer können mit der gleichen, vertrauten Windows Media Player-Benutzeroberfläche, die Sie zurzeit zum Verwalten Ihrer persönlichen Bibliothek verwenden, nach Musik aus dem Online Store-Katalog suchen. Benutzer können zu einem bestimmten Zeitpunkt nur einen einzelnen Online Store-Katalog in der Funktion zum Durchsuchen anzeigen.
-   **Komforts.** Benutzer können eine Stichprobe oder eine Musik erwerben, ohne von der Funktion zum Durchsuchen auf einen anderen Teil der Windows Media Player-Benutzeroberfläche zu wechseln.
-   **Umfassende Features.** Da der Online Store-Katalog ähnlich wie die Bibliothek des Benutzers gespeichert ist, können viele der Features der Windows Media Player-Bibliothek auf den Katalog angewendet werden. Benutzer können z. b. das Word-Rad der Funktion zum Durchsuchen verwenden, um den Online Store-Katalog zu filtern.

Bei einem Online Store-Anbieter haben die Vorteile der Bereitstellung eines Typs vom Typ 1 anstelle eines Typs 2 den folgenden Wert:

-   Ein stark sichtbarer benutzerdefinierter Knoten in der Windows Media Player-Bibliotheksstruktur.
-   Ein System, das für den Erwerb von Musik konzipiert ist.
-   Verbesserte Verbindungen mit Player-Prozessen.
-   Ein besserer, einfacher zu verwendenden Download-Manager.
-   Die Möglichkeit, zwischen verschiedenen Features im Player zu navigieren (einschließlich des Öffnens bestimmter Bibliotheksstruktur Knoten).
-   Benachrichtigungen über den Ablauf der Lizenz für Abonnement Inhalte.
-   Benachrichtigungen zum Arbeiten mit verbundenen portablen Musik Playern.

In den folgenden Abschnitten finden Sie eine Übersicht über den Typ 1 Online Stores.



| `Section`                                                                                              | BESCHREIBUNG                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Musikkatalog](music-catalog.md)                                                                   | Beschreibt den Musikkatalog, der vom Online Shop bereitgestellt wird. Beschreibt den von Microsoft bereitgestellten Katalog Compiler.                                                                     |
| [Inhalts Container](content-containers.md)                                                         | Beschreibt die Content Container Interface ([iwmpcontentcontainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), die zum Darstellen einer Auflistung von zu erwerbenden oder herunter zuladenden Medienobjekten verwendet wird. |
| [Bibliotheks Integration](library-integration.md)                                                       | Beschreibt, wie der Musikkatalog des Online Stores in die Bibliotheks Ansicht des Players integriert ist.                                                                                        |
| [Ermittlungs Seiten](discovery-pages.md)                                                               | Beschreibt die Interaktion zwischen Windows Media Player und Webseiten, die vom Online Store bereitgestellt werden.                                                                                   |
| [Kontextmenüs](context-menus.md)                                                                   | Beschreibt, wie der Online Shop Kontextmenüs bereitstellen kann, während der Benutzer die Benutzeroberfläche des Players navigiert.                                                                         |
| [Audiodatenströme](audio-streams.md)                                                                   | Beschreibt, wie der Online Shop Windows Media Player mit der URL für das Streamen von Audioinhalten bereitstellt.                                                                              |
| [ServiceInfo-Dokument für einen Typ-1-Online Store](serviceinfo-document-for-a-type-1-online-store.md) | Beschreibt das serviceInfo-XML-Dokument, das von einem Online Store vom Typ 1 bereitgestellt wird.                                                                                                           |
| [Typ 1 Online Store-Plug-in](type-1-online-store-plug-in.md)                                       | Beschreibt das Plug-in, das von einem Online Store vom Typ 1 bereitgestellt werden muss.                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Typ 1 Online Stores**](type-1-online-stores.md)
</dt> </dl>

 

 




