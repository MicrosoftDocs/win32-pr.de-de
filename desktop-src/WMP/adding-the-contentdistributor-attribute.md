---
title: Hinzufügen des contentdistributor-Attributs
description: Hinzufügen des contentdistributor-Attributs
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Online Stores, Hinzufügen des contentdistributor-Attributs
- Online Stores, Hinzufügen des contentdistributor-Attributs
- Typ 1 Online Stores, Hinzufügen des contentdistributor-Attributs
- Typ 2 Online Stores, Hinzufügen des contentdistributor-Attributs
- Windows Media Player Online Stores, contentdistributor-Attribut
- Online Stores, contentdistributor-Attribut
- Typ 1 Online Stores, contentdistributor-Attribut
- Typ 2 Online Stores, contentdistributor-Attribut
- Hinzufügen von contentdistributor-Attributen
- Contentdistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310091"
---
# <a name="adding-the-contentdistributor-attribute"></a>Hinzufügen des contentdistributor-Attributs

Wenn der Benutzer versucht, Online Store-Inhalte wiederzugeben oder den Inhalt auf eine CD oder ein Gerät zu kopieren, ruft Windows Media Player bestimmte Methoden in Ihrem com-Objekt auf. Zu diesem Zweck benötigt der Player eine Möglichkeit, ihre Inhalte von anderen Online Store-Anbietern zu unterscheiden. Indem Sie den Namen Ihres Online Store-Schlüssels als Wert für den **contentdistributor** (einen Alias für das Windows Media Format SDK-Attribut mit dem Namen **WM/contentdistributor**) zu Ihrem Windows Media-basierten Inhalt hinzufügen, stellen Sie sicher, dass der Player den dem Dienst zugeordneten Inhalt identifizieren kann.

Durch das Hinzufügen eines Werts für **contentdistributor** wird auch sichergestellt, dass Windows Media Player einen Knoten in der Bibliothek für von Ihnen bereitgestellte Inhalte erstellt. Siehe [Bibliotheks Integration](library-integration.md).

Sie können diesen Wert auf zwei Arten angeben:

-   Verwenden Sie das Windows Media Player-Objektmodell. Wenn Sie dies tun, fügt Windows Media Player den von Ihnen angegebenen Wert der Bibliotheks Datenbank hinzu. Schließlich schreibt der Spieler auch den Attribut Wert in die digitale Mediendatei.
-   Verwenden Sie das SDK für den Windows Media-Format, um das **WM/contentdistributor-** Attribut Programm gesteuert hinzuzufügen. Wenn Sie dies tun, liest Windows Media Player den Attribut Wert und fügt ihn der-Datenbank hinzu, wenn die digitale Mediendatei der Bibliothek hinzugefügt wird.

Wenn Sie das COM-Objekt des Online Stores erstellen, muss der Datei Attribut Wert, den Sie für **contentdistributor** festlegen, und der Wert, der der Konstanten kszcontentdistributorid in yourproject. h zugewiesen ist, exakt übereinstimmen. Denken Sie daran, dass Sie diesen Konstanten Wert für das COM-Objekt angegeben haben, als Sie das Projekt mit dem Projekt-Assistenten erstellt haben. Sie können diesen Wert manuell ändern. Achten Sie einfach darauf, eine Zeichenfolge zu verwenden, die ihren Dienst eindeutig identifiziert.

## <a name="using-the-windows-media-player-object-model"></a>Verwenden des Windows Media Player-Objektmodells

Um einen Wert für **contentdistributor** mithilfe des Windows Media Player-Objektmodells anzugeben, verwenden Sie die [Media. setiteminfo](media-setiteminfo.md) -Methode. Der folgende Beispielcode gibt den Wert "Proseware" für **contentdistributor** für das aktuell wiedergegebene Medien Element an:


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a>Verwenden des SDK für den Windows Media-Format

Das Windows Media Player SDK umfasst eine C++-Beispieldatei mit dem Namen setcontentdistributor. cpp, die veranschaulicht, wie das Windows Media Format 9-Reihe-SDK zum Hinzufügen des **WM/contentdistributor-** Attributs verwendet wird. Sie finden diese Beispieldatei im Ordner "Metadata", in dem Sie das SDK installiert haben. Um diesen Code zu verwenden, müssen Sie die folgenden Schritte ausführen:

1.  Installieren Sie das Windows Media Format 9-Reihe-SDK, und konfigurieren Sie die Runtime, wie in der Dokumentation beschrieben.
2.  Erstellen Sie ein neues leeres C++-Projekt in Visual Studio, und fügen Sie dem Projekt die Beispieldatei mit dem Namen setcontentdistributor. cpp hinzu.
3.  Fügen Sie der Liste der Dateipfade den Pfad der SDK-lib-Ordner des Windows Media-Formats der Serie 9 hinzu. Wählen Sie im Menü **Extras** den Befehl **Optionen**.
4.  Klicken Sie im Dialogfeld **Optionen** auf **Projekte**, und klicken Sie dann auf **VC + +-Verzeichnisse**.
5.  Klicken Sie im Dropdown-Listenfeld **Verzeichnisse anzeigen für** auf **Bibliotheksdateien**.
6.  Verwenden Sie die Schaltflächen, um die Pfade zu den Listenfeldern hinzuzufügen.
7.  Öffnen Sie das Dialogfeld Eigenschaften Seiten für das Projekt. Wählen Sie **Konfigurations Eigenschaften** und dann **Linker** aus, und geben Sie dann **Input** ein. Geben Sie im Textfeld **Zusätzliche Abhängigkeiten** "Wmvcore. lib" ein.

Der Beispielcode erstellt ein Befehlszeilenprogramm. Die Argumente, die Sie beim Ausführen des Programms angeben, geben den Pfad zu der zu ändernden digitalen Mediendatei und eine Zeichenfolge für den Wert des **contentdistributor** -Attributs an. Der Code verwendet **iwmheaderinfo:: setAttribute** , um der von Ihnen angegebenen Datei das-Attribut hinzuzufügen. Sie können dieses Beispiel unverändert verwenden oder als Ausgangspunkt für Ihr eigenes Programm verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




