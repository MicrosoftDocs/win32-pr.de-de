---
title: Informationen zur Bibliothek
description: Informationen zur Bibliothek
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player,Bibliothek
- Windows Media Player Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player ActiveX,Bibliothek für objektmodell
- ActiveX,Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobil,Bibliothek für Objektmodell
- Windows Media Player Bibliothek, Informationen
- Bibliothek, Informationen
- Metadata,Windows Media Player Library
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63fdaa19fc8be11de1886074a21b0cc1fb6d4be7dde73faa05c67e1f496ac17c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470350"
---
# <a name="about-the-library"></a>Informationen zur Bibliothek

Die Bibliothek ist eine Datenbank mit Informationen oder *Metadaten* zu den digitalen Medieninhalten, die für die Windows Media Player. Einige der Informationen werden im Bereich Bibliothek **im** Player angezeigt. mehr davon ist über Code verfügbar.

(In Windows Media Player Serie 9 und früher heißt dieses Feature **Media Library**.)

Die Bibliothek bietet Benutzern eine einfache Möglichkeit, digitale Medieninhalte zu organisieren und darauf zu zugreifen. Benutzer können z. B. Musik, die nach Album, Interpret, Genre oder einfach als Liste aller Musik organisiert ist, anzeigen. Sie können das Windows Media Player SDK-Objektmodell verwenden, um auf die Bibliothek zu zugreifen, um Inhalte wieder anzuzeigen, Wiedergabelisten abzurufen, Inhalte hinzuzufügen, Inhalte zu entfernen und die zugeordneten Metadaten zu ändern. Windows Media Player schützt den Datenschutz der Benutzer, indem Sie die Möglichkeit einschränken, unter bestimmten Bedingungen über Code auf die Bibliothek zu zugreifen. Weitere Informationen zu Zugriffsrechten finden Sie unter [Bibliothekszugriff.](library-access.md)

Die Bibliothek speichert Metadaten zu zwei grundlegenden Arten von digitalen Medieninhalten. Der erste Typ, digitale Medienelemente, sind einzelne Inhaltsdateien, z. B. eine Musikspur oder ein Foto. Der zweite Typ, Wiedergabelisten, sind Dateien, die eine Gruppe von digitalen Medienelementen darstellen, die in der Regel in einer angegebenen Reihenfolge abgespielt werden sollen. Die Metadaten, die digitalen Medieninhalten zugeordnet sind, werden als Name-Wert-Paare gespeichert. Beispielsweise werden die Metadaten, die die Person beschreiben, die einen Titel ausgeführt hat, als "Interpret" bezeichnet, und der zugeordnete Wert ist in der Regel eine Textzeichenfolge, die den Namen des Performers enthält. Jeder eindeutige Metadatenname wird als Attribut *bezeichnet.* Eine Liste der unterstützten Attribute finden Sie in der [Attributreferenz.](attribute-reference.md) Informationen zur Verwendung von Attributen im Code finden Sie unter [Media Item Attributes](media-item-attributes.md).

Die folgenden Abschnitte enthalten weitere Informationen zum Arbeiten mit der Bibliothek:

-   [Programmgesteuerter Zugriff auf die Bibliothek](accessing-the-library-programmatically.md)
-   [Informationen zu Bibliotheksdiensten](about-library-services.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




