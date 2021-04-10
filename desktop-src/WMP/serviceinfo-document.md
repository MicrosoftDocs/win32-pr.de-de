---
title: Servicinfo-Dokument
description: Servicinfo-Dokument
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539c4e1a58e5dbf88e1fc79909791a7dab767ef1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036611"
---
# <a name="serviceinfo-document"></a>Servicinfo-Dokument

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Online Stores müssen das ServiceInfo.xml Dokument erstellen. Dies ist das Dokument, das der Online Shop zum Konfigurieren der Windows Media Player-Benutzeroberfläche verwendet, wenn Windows Media Player 10 oder höher den Online Store gehostet.

Die folgenden Elemente und deren Attribute werden für Windows-Media Player Online Stores unterstützt.



| Element                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Albuminfo](albuminfo-element.md)           | Gibt die URL für die Webseite an, die von Windows Media Player angezeigt wird, wenn der Benutzer weitere Informationen zu einem bestimmten Medien Element anzeigen möchte. Typ 1: optional<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: ignoriert<br/>                                |
| [Folgendes](buttontext-element.md)         | Gibt die Text Zeichenfolge an, die von Windows für eine Schaltfläche im Aufgabenbereich angezeigt Media Player Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                                             |
| [Buttontip](buttontip-element.md)           | Gibt die QuickInfo an, die angezeigt wird, wenn der Benutzer auf eine Schaltfläche für den Aufgabenbereich zeigt. Typ 1: optional<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                                         |
| [Buycd](buycd-element.md)                   | Gibt die URLs für Webseiten an, die von Windows Media Player angezeigt werden, wenn der Benutzer sich für einen Einkauf entscheidet. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: ignoriert<br/>                                                                      |
| [Farbe](color-element.md)                   | Gibt die Hintergrundfarbe für die Navigations Schaltflächen von Online Stores an. Typ 1: optional<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                                                             |
| [Beschreibung](description-element.md)       | Gibt eine Beschreibung des Online Stores an, der während der ersten Benutzer Darstellung eines Benutzers mit einer Installation von Windows Media Player angezeigt wird. Erfordert Windows Media Player 11. Typ 1: erforderlich<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/> |
| [Download Status](downloadstatus-element.md) | Gibt eine URL an, die der Windows-Media Player als Link anzeigt, damit Benutzer den Download Status anzeigen können. Typ 1: wird ignoriert.<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Gibt die Text Zeichenfolge an, die von Windows Media Player dem Benutzer angezeigt wird, um den Online Store zu identifizieren. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                           |
| [HtmlView](htmlview-element.md)             | Gibt die Basis-URL einer HtmlView-Webseite an. Typ 1: optional<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                                                                                   |
| [Image](image-element.md)                   | Gibt die Bilder an, die von Windows Media Player dem Benutzer angezeigt werden, um den Online Store darzustellen. Typ 1: erforderlich<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                               |
| [InfoCenter für](infocenter-element.md)         | Gibt die URL der **Webseite an, die von Windows** Media Player in der Info Center-Ansichts Funktion von angezeigt wird, wenn der Online Store aktiv ist. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: ignoriert<br/>                           |
| [Installieren](install-element.md)               | Gibt Werte an, die von der Windows Media Player-Installation verwendet werden, um den standardmäßigen Online Store Typ 1: erforderlich<br/> Type 2 Music: optional<br/> Typ 2 Commerce: ignoriert<br/>                                                                                          |
| [Navigieren](navigate-element.md)             | Gibt eine Basis-URL an, die von Aufrufen von " **extern. navigatetaskpaneurl**" verwendet wird. Typ 1: optional<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Stellt das Hauptelement für das ServiceInfo.xml Dokument dar. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Stellt den ersten Aufgabenbereich im Online Store dar. Typ 1: erforderlich<br/> Typ 2 Musik: erforderlich<br/> Typ 2 Commerce: erforderlich<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Stellt den zweiten Aufgabenbereich im Online Store dar. Typ 1: wird ignoriert.<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Stellt den dritten Aufgabenbereich im Online Store dar. Typ 1: wird ignoriert.<br/> Type 2 Music: optional<br/> Typ 2 Commerce: optional<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





