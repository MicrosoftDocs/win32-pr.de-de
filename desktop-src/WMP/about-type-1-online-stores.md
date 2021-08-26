---
title: Informationen zu Onlineshops vom Typ 1
description: Informationen zu Onlineshops vom Typ 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Onlineshops, geben Sie 1 Onlineshops ein.
- Onlineshops, Geben Sie 1 Onlineshops ein.
- Geben Sie 1 Onlineshops ein, informationen
- Windows Media Player, geben Sie 1 Onlineshops ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bc84311bb61c71fdcaf57b584b5c595a62be5c80d406f71ef36c8d1ad8e655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903060"
---
# <a name="about-type-1-online-stores"></a>Informationen zu Onlineshops vom Typ 1

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Microsoft Windows Media Player 11 unterstützt zwei Arten von Onlineshops: Typ 1 und Typ 2. Speicher vom Typ 1 sind stärker in Windows Media Player integriert als Speicher vom Typ 2. Ein Onlineshop vom Typ 1 stellt einen herunterladbaren Musikkatalog bereit, sodass Windows Media Player den Inhalt des Speichers für den Benutzer verfügbar machen können, als ob der Inhalt in der lokalen Medienbibliothek des Benutzers enthalten wäre.

Ein Onlineshop vom Typ 1 muss ein Plug-In bereitstellen, das die [IWMPContentPartner-Schnittstelle](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) implementiert. Während der Benutzer auf der Windows Media Player Benutzeroberfläche navigiert, ruft der Player das Plug-In auf, sodass der Onlineshop die Benutzerfreundlichkeit verbessern kann, indem Webseiten zur Verfügung gestellt werden, die im Player angezeigt werden.

Zu den Features von Onlineshops vom Typ 1, die sie von Denkspeichern vom Typ 2 unterscheiden, gehören folgende:

-   **Benutzerfreundlichkeit.** Benutzer können mithilfe der gleichen, vertrauten Windows Media Player Benutzeroberfläche, die sie derzeit zum Verwalten ihrer persönlichen Bibliothek verwenden, nach Musik aus dem Onlineshopkatalog suchen. Benutzer können in der Funktion Durchsuchen zu einem bestimmten Zeitpunkt nur einen einzelnen Onlineshopkatalog anzeigen.
-   **Bequemlichkeit.** Benutzer können Musikbeispiele erstellen oder kaufen, ohne von der Funktion Durchsuchen zu einem anderen Teil der Windows Media Player Benutzeroberfläche zu wechseln.
-   **Umfassende Features.** Da der Onlineshopkatalog ähnlich wie die Bibliothek des Benutzers gespeichert wird, können viele der Windows Media Player Bibliotheksfunktionen auf den Katalog angewendet werden. Beispielsweise können Benutzer das Wortrad des Features Durchsuchen verwenden, um den Onlineshopkatalog zu filtern.

Für einen Onlineshopanbieter bieten die Folgenden Vorteile, wenn sie einen Store vom Typ 1 anstelle eines Stores vom Typ 2 bereitstellen:

-   Ein stark sichtbarer benutzerdefinierter Knoten in der Windows Media Player Bibliotheksstruktur.
-   Ein Für Musikkäufe konzipiertes System.
-   Verbesserte Verbindungen mit Player-Prozessen.
-   Ein besserer, benutzerfreundlicherer Download-Manager.
-   Die Möglichkeit, zwischen verschiedenen Features im Player zu navigieren (einschließlich des Öffnens bestimmter Bibliotheksstrukturknoten).
-   Benachrichtigungen zum Lizenzablauf für Abonnementinhalte.
-   Benachrichtigungen für die Arbeit mit verbundenen portablen Musikplayern.

Die folgenden Abschnitte enthalten Übersichtsinformationen zu Onlineshops vom Typ 1.



| `Section`                                                                                              | BESCHREIBUNG                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Musik Katalog](music-catalog.md)                                                                   | Beschreibt den musikkatalog, der vom Onlineshop bereitgestellt wird. Beschreibt den von Microsoft bereitgestellten Katalogcompiler.                                                                     |
| [Inhaltscontainer](content-containers.md)                                                         | Beschreibt die Inhaltscontainerschnittstelle[(IWMPContentContainer),](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)die verwendet wird, um eine Sammlung von Medienelementen darzustellen, die erworben oder heruntergeladen werden sollen. |
| [Bibliotheksintegration](library-integration.md)                                                       | Beschreibt, wie der Musikkatalog des Onlineshops in die Bibliotheksansicht des Players integriert wird.                                                                                        |
| [Ermittlungsseiten](discovery-pages.md)                                                               | Beschreibt die Interaktion zwischen Windows Media Player und Webseiten, die vom Onlineshop bereitgestellt werden.                                                                                   |
| [Kontextmenüs](context-menus.md)                                                                   | Beschreibt, wie der Onlineshop Kontextmenüs bereitstellen kann, während der Benutzer auf der Benutzeroberfläche des Players navigiert.                                                                         |
| [Audio Streams](audio-streams.md)                                                                   | Beschreibt, wie der Onlineshop Windows Media Player mit der URL zum Streamen von Audioinhalten bereitstellt.                                                                              |
| [ServiceInfo-Dokument für ein Online-Store vom Typ 1](serviceinfo-document-for-a-type-1-online-store.md) | Beschreibt das ServiceInfo-XML-Dokument, das von einem Onlineshop vom Typ 1 bereitgestellt wird.                                                                                                           |
| [Geben Sie 1 Online Store Plug-In ein.](type-1-online-store-plug-in.md)                                       | Beschreibt das Plug-In, das ein Onlineshop vom Typ 1 bereitstellen muss.                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geben Sie 1 Onlineshops ein.**](type-1-online-stores.md)
</dt> </dl>

 

 




