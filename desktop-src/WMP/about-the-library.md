---
title: Informationen zur Bibliothek
description: Informationen zur Bibliothek
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player Bibliothek, Informationen zu
- Bibliothek, Informationen zu
- Metadaten, Windows-Media Player Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340813"
---
# <a name="about-the-library"></a>Informationen zur Bibliothek

Bei der Bibliothek handelt es sich um eine Datenbank mit Informationen oder *Metadaten* zu den digitalen Medieninhalten, die für Windows-Media Player verfügbar sind. Einige der Informationen werden im Bereich **Bibliothek** im Player angezeigt. Weitere Informationen finden Sie im Code.

(In der Windows Media Player 9-Serie und früher wird diese Funktion als **Medienbibliothek** bezeichnet.)

Die-Bibliothek bietet Benutzern eine einfache Möglichkeit zum organisieren und Zugreifen auf digitale Medieninhalte. Beispielsweise können Benutzer Musik, geordnet nach Album, nach Genre oder einfach als Liste aller Musik anzeigen. Mit dem Windows Media Player SDK-Objektmodell können Sie auf die Bibliothek zugreifen, um Inhalte wiederzugeben, Wiedergabelisten abzurufen, Inhalte hinzuzufügen, Inhalte zu entfernen und die zugehörigen Metadaten zu ändern. Windows Media Player schützt den Datenschutz der Benutzer, indem die Möglichkeit eingeschränkt wird, über Code unter bestimmten Bedingungen auf die Bibliothek zuzugreifen. Weitere Informationen zu Zugriffsrechten finden Sie unter [Bibliotheks Zugriff](library-access.md).

Die Bibliothek speichert Metadaten zu zwei grundlegenden Arten von digitalen Medieninhalten. Der erste Typ, digitale Medienelemente, sind einzelne Inhalts Dateien, z. b. ein Musiktitel oder ein Foto. Der zweite Typ, Wiedergabelisten, sind Dateien, die eine Gruppe digitaler Medienelemente darstellen, die in der Regel in einer angegebenen Reihenfolge wiedergegeben werden sollen. Die Metadaten, die digitalen Medieninhalten zugeordnet sind, werden als Name-Wert-Paare gespeichert. Beispielsweise werden die Metadaten, die die Person beschreiben, die einen Song ausgeführt hat, "Artist" genannt, und der zugeordnete Wert ist in der Regel eine Text Zeichenfolge, die den Namen des Performers enthält. Jeder eindeutige Metadatenname wird als *Attribut* bezeichnet. Eine Auflistung der unterstützten Attribute finden Sie unter [Attribut Verweis](attribute-reference.md). Weitere Informationen zur Verwendung von Attributen im Code finden Sie unter [Medien Element Attribute](media-item-attributes.md).

In den folgenden Abschnitten finden Sie weitere Informationen zum Arbeiten mit der-Bibliothek:

-   [Programm gesteuerter Zugriff auf die Bibliothek](accessing-the-library-programmatically.md)
-   [Informationen zu Bibliothek Diensten](about-library-services.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




