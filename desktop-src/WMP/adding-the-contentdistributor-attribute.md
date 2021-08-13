---
title: Hinzufügen des ContentDistributor-Attributs
description: Hinzufügen des ContentDistributor-Attributs
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Onlineshops, Hinzufügen des ContentDistributor-Attributs
- Onlineshops, Hinzufügen des ContentDistributor-Attributs
- Geben Sie 1 Onlineshops ein, und fügen Sie das ContentDistributor-Attribut hinzu.
- Geben Sie 2 Onlineshops ein, und fügen Sie das ContentDistributor-Attribut hinzu.
- Windows Media Player Onlineshops, ContentDistributor-Attribut
- Onlineshops, ContentDistributor-Attribut
- Geben Sie 1 Onlineshops ein, ContentDistributor-Attribut
- Typ 2 Onlineshops, ContentDistributor-Attribut
- Hinzufügen des ContentDistributor-Attributs
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66871f73c03e73c08b5ae7e72518a48817192def22c8dfce4caf2ce12d36fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391790"
---
# <a name="adding-the-contentdistributor-attribute"></a>Hinzufügen des ContentDistributor-Attributs

Wenn der Benutzer versucht, Inhalte im Onlineshop wiederzuspielen oder den Inhalt auf eine CD oder ein Gerät zu kopieren, ruft Windows Media Player bestimmte Methoden in Ihrem COM-Objekt auf. Hierzu benötigt der Player eine Möglichkeit, Ihre Inhalte von den Inhalten anderer Onlineshopanbieter zu unterscheiden. Indem Sie Den Namen Ihres Onlinespeicherschlüssels als Wert für das **ContentDistributor-Attribut** (ein Alias für das Windows Media Format SDK-Attribut namens **WM/ContentDistributor**) ihrem Windows medienbasierten Inhalt hinzufügen, stellen Sie sicher, dass der Player den Ihrem Dienst zugeordneten Inhalt identifizieren kann.

Das Hinzufügen eines Werts für **ContentDistributor** stellt außerdem sicher, dass Windows Media Player einen Knoten in der Bibliothek für von Ihnen angegebenen Inhalt erstellt. Weitere Informationen finden Sie unter [Bibliotheksintegration.](library-integration.md)

Sie können diesen Wert auf zwei Arten angeben:

-   Verwenden Sie das Windows Media Player-Objektmodell. Wenn Sie dies tun, fügt Windows Media Player der Bibliotheksdatenbank den von Ihnen angegebenen Wert hinzu. Schließlich schreibt der Player auch den Attributwert in die digitale Mediendatei.
-   Verwenden Sie das Windows Media Format SDK, um das **WM/ContentDistributor-Attribut** programmgesteuert hinzuzufügen. Wenn Sie dies tun, liest Windows Media Player den Attributwert und fügt ihn der Datenbank hinzu, wenn die digitale Mediendatei der Bibliothek hinzugefügt wird.

Beim Erstellen des COM-Objekts des Onlineshops müssen der Dateiattributwert, den Sie für **ContentDistributor** festlegen, und der Wert, der der Konstanten kszContentDistributorID in YourProject.h zugewiesen ist, genau übereinstimmen. Denken Sie daran, dass Sie diesen konstanten Wert für das COM-Objekt angegeben haben, als Sie das Projekt mithilfe des Projekt-Assistenten erstellt haben. Sie können diesen Wert manuell ändern. Achten Sie darauf, eine Zeichenfolge zu verwenden, die Ihren Dienst eindeutig identifiziert.

## <a name="using-the-windows-media-player-object-model"></a>Verwenden des Windows Media Player-Objektmodells

Um einen Wert für **ContentDistributor** mithilfe des Windows Media Player-Objektmodells anzugeben, verwenden Sie die [Media.setItemInfo-Methode.](media-setiteminfo.md) Der folgende Beispielcode gibt den Wert "Proseware" für **ContentDistributor** für das aktuell wiedergegebene Medienelement an:


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



## <a name="using-the-windows-media-format-sdk"></a>Verwenden des Windows Media Format SDK

Das Windows Media Player SDK enthält eine C++-Beispieldatei namens SetContentDistributor.cpp, die veranschaulicht, wie das Windows Media Format 9 Series SDK zum Hinzufügen des **WM/ContentDistributor-Attributs** verwendet wird. Sie finden diese Beispieldatei im Ordner Metadaten, in dem Sie das SDK installiert haben. Um diesen Code verwenden zu können, müssen Sie die folgenden Schritte ausführen:

1.  Installieren Sie das Windows Media Format 9 Series SDK, und konfigurieren Sie die Runtime wie in der Dokumentation beschrieben.
2.  Erstellen Sie in Visual Studio ein neues leeres C++-Projekt, und fügen Sie dem Projekt die Beispieldatei SetContentDistributor.cpp hinzu.
3.  Fügen Sie der Liste der Dateipfade den Pfad zu den Ordnern Windows Media Format 9 Series SDK Lib hinzu. Wählen Sie im Menü **Extras** den Befehl **Optionen**.
4.  Klicken Sie im Dialogfeld **Optionen** auf **Projekte** und dann auf **VC++ Verzeichnisse**.
5.  Klicken Sie im Dropdownlistenfeld **Verzeichnisse für anzeigen** auf **Bibliotheksdateien.**
6.  Verwenden Sie die Schaltflächen, um die Pfade zu den Listenfeldern hinzuzufügen.
7.  Öffnen Sie das Dialogfeld Eigenschaftenseiten für Ihr Projekt. Wählen Sie **Konfigurationseigenschaften**, dann **Linker** und dann **Eingabe aus.** Geben Sie "wmvcore.lib" in das Textfeld **Zusätzliche Abhängigkeiten** ein.

Der Beispielcode erstellt ein Befehlszeilenprogramm. Die Argumente, die Sie beim Ausführen des Programms angeben, geben den Pfad zur zu ändernden digitalen Mediendatei und eine Zeichenfolge für den **ContentDistributor-Attributwert** an. Der Code verwendet **IWMHeaderInfo::SetAttribute,** um das Attribut der angegebenen Datei hinzuzufügen. Sie können dieses Beispiel beliebig verwenden oder als Ausgangspunkt für Ihr eigenes Programm verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und Typ 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




