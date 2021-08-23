---
title: Player-Objektmodell für Skriptsprachen
description: Player-Objektmodell für Skriptsprachen
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player,Objektmodell
- Windows Media Player Objektmodell, Informationen
- Objektmodell, Informationen
- Windows Media Player ActiveX-Steuerelement, Objektmodell
- ActiveX-Steuerelement, Objektmodell
- Windows Media Player Mobiles ActiveX-Steuerelement, Objektmodell
- Windows Media Player Mobil, Objektmodell
- Software Development Kit (SDK),Windows Media Player ActiveX Steuerelementobjektmodell
- SDK (Software Development Kit),Windows Media Player ActiveX Steuerelementobjektmodell
- Dokumentation,Windows Media Player ActiveX Steuerelementobjektmodell
- Windows Media Player,Skriptsprachen
- Windows Media Player-Objektmodell, Skriptsprachen
- Objektmodell, Skriptsprachen
- Windows Media Player ActiveX-Steuerelement, Skriptsprachen
- ActiveX-Steuerelement, Skriptsprachen
- Windows Media Player Mobile ActiveX-Steuerelement, Skriptsprachen
- Windows Media Player Mobil, Skriptsprachen
- Skriptsprachen
- Windows Media Player,Player-Objekt
- Windows Media Player-Objektmodell, Player-Objekt
- Objektmodell,Player-Objekt
- Windows Media Player ActiveX-Steuerelement, Player-Objekt
- ActiveX-Steuerelement, Player-Objekt
- Windows Media Player Mobiles ActiveX-Steuerelement, Player-Objekt
- Windows Media Player Mobiles, Player-Objekt
- Player-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe34bfc227dfe250a9c9d7ebb60977a9ab079c4a062067c65e83e62f0e5976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996025"
---
# <a name="player-object-model-for-scripting-languages"></a>Player-Objektmodell für Skriptsprachen

ActiveX verwendet das Konzept von -Objekten, um Programmierfunktionen zu enthalten. Windows Media Player verwendet mehrere -Objekte, um die Funktionalität aufzuteilen, die das Steuerelement bereitstellt. Das Stammobjekt  ist das Player-Objekt, und die anderen Objekte werden über bestimmte Eigenschaften an das **Player-Objekt** angefügt.

Das folgende Diagramm zeigt, wie das Windows Media Player 11 ActiveX-Steuerelementobjektmodell für Skriptsprachen funktioniert.

![Diagramm des Windows Media Player 11-Objektmodells](images/playeromdiag.png)

In C++ und manchmal in .NET-Sprachen werden Objekte durch COM-Schnittstellen dargestellt. Im Windows Media Player-Objektmodell sind com-Schnittstellennamen identisch mit dem Objektnamen, haben aber das Präfix "IWMP". Beispielsweise wird das **Netzwerkobjekt** über die **IWMPNetwork-Schnittstelle** verfügbar gemacht.

Die folgenden Abschnitte enthalten konzeptionelle Übersichten für jedes Objekt:

-   [Informationen zu den Objekten "Chole" und "CcollectionCollection"](about-the-cdrom-and-cdromcollection-objects.md)
-   [Informationen zum ClosedCaption-Objekt](about-the-closedcaption-object.md)
-   [Informationen zum Controls-Objekt](about-the-controls-object.md)
-   [Informationen zum DVD-Objekt](about-the-dvd-object.md)
-   [Informationen zu Error- und ErrorItem-Objekten](about-the-error-and-erroritem-objects.md)
-   [Informationen zu MediaCollection und Medienobjekten](about-the-mediacollection-and-media-objects.md)
-   [Informationen zum MetadataPicture-Objekt](about-the-metadatapicture-object.md)
-   [Informationen zum MetadataText-Objekt](about-the-metadatatext-object.md)
-   [Informationen zum Netzwerkobjekt](about-the-network-object.md)
-   [Informationen zum Player-Objekt](about-the-player-object.md)
-   [Informationen zum PlayerApplication-Objekt](about-the-playerapplication-object.md)
-   [Informationen zu den Objekten "Playlist", "PlaylistCollection" und "PlaylistArray"](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Informationen zum Abfrageobjekt](about-the-query-object.md)
-   [Informationen zum Einstellungen-Objekt](about-the-settings-object.md)
-   [Informationen zum StringCollection-Objekt](about-the-stringcollection-object.md)

Zusätzliche Funktionen sind über bestimmte COM-Schnittstellen verfügbar. Ob Sie auf diese Schnittstellen zugreifen können, hängt möglicherweise von der Sprache ab, die Sie für die Programmierung verwenden, und von anderen Faktoren, z. B. dem Modus, der zum Erstellen der Instanz des Windows Media Player-Steuerelements verwendet wird. Eine vollständige Liste der COM-Schnittstellen, die vom Windows Media Player-Steuerelement verfügbar gemacht werden, finden Sie in der [Objektmodellreferenz für C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Playerobjektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuerelements in einer .NET Framework-Projektmappe**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




