---
title: ServiceInfo-Dokument
description: ServiceInfo-Dokument
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player,ServiceInfo-Dokument
- Onlineshops,ServiceInfo-Dokument
- Typ 1 Onlineshops,ServiceInfo-Dokument
- Typ 2 Onlineshops,ServiceInfo-Dokument
- ServiceInfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88863bb75cd0a7b85bead1c20759b77710c2db483b4d9e48ed1f53741dd0840d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995420"
---
# <a name="serviceinfo-document"></a>ServiceInfo-Dokument

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Onlineshops müssen das ServiceInfo.xml erstellen. Dies ist das Dokument, das der Onlineshop verwendet, um die Windows Media Player-Benutzeroberfläche zu konfigurieren, wenn Windows Media Player 10 oder höher den Onlineshop hosten.

Die folgenden Elemente und ihre Attribute werden für Windows Media Player unterstützt.



| Element                                      | Beschreibung                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Gibt die URL für die Webseite an, Windows Media Player angezeigt wird, wenn der Benutzer weitere Informationen zu einem bestimmten Medienelement anzeigt. Typ 1: optional<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: ignoriert<br/>                                |
| [Buttontext](buttontext-element.md)         | Gibt die Textzeichenfolge an, Windows Media Player schaltfläche für einen Aufgabenbereich angezeigt wird. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | Gibt die QuickInfo an, die angezeigt wird, wenn der Benutzer auf eine Schaltfläche im Aufgabenbereich zeigt. Typ 1: optional<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Gibt die URLs für Webseiten an, Windows Media Player angezeigt werden, wenn sich der Benutzer für einen Kauf entscheidet. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: ignoriert<br/>                                                                      |
| [Farbe](color-element.md)                   | Gibt die Hintergrundfarbe für Die Navigationsschaltflächen von Onlineshops an. Typ 1: optional<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                                                             |
| [Beschreibung](description-element.md)       | Gibt eine Beschreibung des Onlineshops an, die während der ersten Benutzeroberfläche des Benutzers mit einer Installation von Windows Media Player. Erfordert Windows Media Player 11.Typ 1: erforderlich.<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/> |
| [DownloadStatus](downloadstatus-element.md) | Gibt eine URL an, die vom Windows Media Player link angezeigt wird, damit Benutzer den Downloadstatus anzeigen können. Typ 1: ignoriert<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                         |
| [Friendlyname](friendlyname-element.md)     | Gibt die Textzeichenfolge an, Windows Media Player dem Benutzer angezeigt wird, um den Onlineshop zu identifizieren. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Gibt die Basis-URL einer HTMLView-Webseite an. Typ 1: optional<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                                                                                   |
| [Bild](image-element.md)                   | Gibt die Bilder an, Windows Media Player dem Benutzer angezeigt werden, um den Onlineshop zu repräsentieren. Typ 1: erforderlich<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                               |
| [Infocenter](infocenter-element.md)         | Gibt die URL der Webseite an, die Windows Media Player im  Infocenteransichtsfeature jetzt wiedergibt, wenn der Onlineshop aktiv ist. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: ignoriert<br/>                           |
| [Installieren](install-element.md)               | Gibt die Werte an, die Windows Media Player Setup zum Installieren des Standard-Onlineshops verwendet werden. Typ 1: erforderlich<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: ignoriert<br/>                                                                                          |
| [Navigieren](navigate-element.md)             | Gibt eine Basis-URL an, die von Aufrufen von **External.NavigateTaskPaneURL verwendet wird.** Typ 1: optional<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Stellt das Hauptelement für das ServiceInfo.xml dar. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Stellt den ersten Aufgabenbereich des Onlineshops dar. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Stellt den zweiten Aufgabenbereich des Onlineshops dar. Typ 1: ignoriert<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Stellt den dritten Aufgabenbereich des Onlineshops dar. Typ 1: ignoriert<br/> Geben Sie 2 Musik ein: optional.<br/> Typ 2 Commerce: optional<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





