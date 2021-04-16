---
title: Player-Objektmodell für Skriptsprachen
description: Player-Objektmodell für Skriptsprachen
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Informationen zu
- Objektmodell, Informationen
- Windows Media Player ActiveX-Steuerelement, Objektmodell
- ActiveX-Steuerelement, Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Objektmodell
- Windows Media Player Mobile, Objektmodell
- Software Development Kit (SDK), Windows Media Player ActiveX-Steuerelement-Objektmodell
- SDK (Software Development Kit), Windows Media Player ActiveX-Steuerelement-Objektmodell
- Dokumentation, Windows Media Player ActiveX-Steuerelement-Objektmodell
- Windows Media Player, Skriptsprachen
- Windows Media Player-Objektmodell, Skriptsprachen
- Objektmodell, Skriptsprachen
- Windows Media Player ActiveX-Steuerelement, Skriptsprachen
- ActiveX-Steuerelement, Skriptsprachen
- Windows Media Player Mobile ActiveX-Steuerelement, Skriptsprachen
- Windows Media Player Mobile, Skriptsprachen
- Skriptsprachen
- Windows Media Player, Player-Objekt
- Windows Media Player-Objektmodell, Player-Objekt
- Objektmodell, Player-Objekt
- Windows Media Player ActiveX-Steuerelement, Player-Objekt
- ActiveX-Steuerelement, Player-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Player-Objekt
- Windows Media Player Mobile, Player-Objekt
- Player-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570737"
---
# <a name="player-object-model-for-scripting-languages"></a>Player-Objektmodell für Skriptsprachen

ActiveX verwendet das Konzept von-Objekten, um Programmierfunktionen zu enthalten. In Windows Media Player werden mehrere-Objekte verwendet, um die Funktionalität des Steuer Elements aufzuteilen. Das Stamm Objekt ist das **Player** -Objekt, und die anderen Objekte werden über bestimmte Eigenschaften an das **Player** -Objekt angefügt.

Das folgende Diagramm zeigt, wie das Objektmodell des ActiveX-Steuer Elements von Windows Media Player 11 für Skriptsprachen funktioniert.

![Diagramm des Windows Media Player 11-Objektmodells](images/playeromdiag.png)

In C++ und manchmal in .NET-Sprachen werden Objekte durch COM-Schnittstellen dargestellt. Im Windows Media Player-Objektmodell Stimmen com-Schnittstellennamen mit dem Objektnamen überein, haben jedoch das Präfix "iwmp". Das **Netzwerk** Objekt wird z. b. über die **iwmpnetwork** -Schnittstelle verfügbar gemacht.

In den folgenden Abschnitten werden konzeptionelle Übersichten für jedes Objekt bereitgestellt:

-   [Informationen zu den CDROM-und cdromcollection-Objekten](about-the-cdrom-and-cdromcollection-objects.md)
-   [Informationen zum closedcaption-Objekt](about-the-closedcaption-object.md)
-   [Informationen zum Steuerelement Objekt](about-the-controls-object.md)
-   [Informationen zum DVD-Objekt](about-the-dvd-object.md)
-   [Informationen zu den Fehlern und ErrorItem-Objekten](about-the-error-and-erroritem-objects.md)
-   [Informationen zu mediacollection und Media Objects](about-the-mediacollection-and-media-objects.md)
-   [Informationen zum MetadataPicture-Objekt](about-the-metadatapicture-object.md)
-   [Informationen zum MetadataText-Objekt](about-the-metadatatext-object.md)
-   [Informationen zum Netzwerk Objekt](about-the-network-object.md)
-   [Informationen zum Player-Objekt](about-the-player-object.md)
-   [Informationen zum playerapplication-Objekt](about-the-playerapplication-object.md)
-   [Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Informationen zum Query-Objekt](about-the-query-object.md)
-   [Informationen zum Einstellungs Objekt](about-the-settings-object.md)
-   [Informationen zum StringCollection-Objekt](about-the-stringcollection-object.md)

Zusätzliche Funktionen sind über bestimmte COM-Schnittstellen verfügbar. Ob Sie auf diese Schnittstellen zugreifen können, hängt möglicherweise von der Sprache, die Sie für die Programmierung verwenden, und anderen Faktoren ab, wie z. b. dem Modus, der zum Erstellen der Instanz des Windows-Media Player Eine umfassende Liste der COM-Schnittstellen, die vom Windows Media Player-Steuerelement verfügbar gemacht werden, finden Sie in der [Objektmodell Referenz für C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einer .NET Framework-Lösung**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




