---
title: Wiedergabelistenattribute
description: Wiedergabelistenattribute
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player,Wiedergabelisten
- Windows Media Player Objektmodell,Wiedergabelisten
- Objektmodell,Wiedergabelisten
- Windows Media Player Mobil, Wiedergabelisten
- Windows Media Player ActiveX,Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement,Wiedergabelisten
- ActiveX,Wiedergabelisten
- Wiedergabelisten, Attribute
- Metafile-Wiedergabelisten, Attribute
- Windows Wiedergabelisten von Medienmetadateien, Attribute
- Attribute, Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00416f641fac89c707405c03dc70af0497b34d4cf646aa44fad5124f97f09a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995710"
---
# <a name="playlist-attributes"></a>Wiedergabelistenattribute

Wiedergabelisten verfügen über Metadateninformationen, die als Attribute bezeichnet werden, ebenso wie Medienelemente Attribute haben. Sie können die Namen und Werte von Wiedergabelistenattributen abrufen und auf Ihrer Benutzeroberfläche anzeigen, oder Ihr Code kann Aktionen basierend auf dem Wert eines Attributs ausführen.

Wiedergabelisten werden in Dateien definiert, die in einem XML-Format organisiert sind, und bestimmte Elemente in der Datei definieren Wiedergabelistenattribute. Einige Attributelemente sind bekannt. Der Autor der Metadatei kann auch beliebige Attribute definieren. Weitere Informationen zu Attributelementen in Wiedergabelistendateien finden Sie unter [Abrufen von Metadaten.](retrieving-metadata.md)

Die Bibliothek kann zusätzliche Wiedergabelistenattribute wie **SourceURL** oder **UserLastPlayedTime bereitstellen.** Weitere Informationen zu den Attributen der Bibliothekswiedergabeliste finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

Die *Wiedergabeliste*. **Die attributeCount-Eigenschaft** ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind. Die *Wiedergabeliste*. **Die attributeName-Eigenschaft** ruft den Namen eines Attributs basierend auf seinem Index und die *Wiedergabeliste ab.* **Die getItemInfo-Methode** ruft den Wert eines Attributs basierend auf seinem Namen ab.

Sie können den Wert eines Attributs der aktuellen Wiedergabeliste mit der *Wiedergabeliste ändern.* **setItemInfo-Methode.**

Eine besondere Verwendung der **setItemInfo-Methode** besteht in der Sortierung der Elemente in der Wiedergabeliste mithilfe des **SortAttribute-Attributs.** Im folgenden C#-Beispiel wird eine Wiedergabeliste nach den Werten des **UserLastPlayedTime-Attributs** sortiert. Die Variable *Playlist* ist ein Verweis auf ein **Playlist-Objekt.**


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



In diesem Thema wurde **das Player-Objekt** wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Der folgende C#-Beispielcode veranschaulicht das Abrufen von Wiedergabelistenattributen. Die erste Funktion, ShowPlaylists, füllt ein ListBox-Steuerelement mit den Namen der verfügbaren Wiedergabelisten auf. Der zweite Teil ist der Listenfeldereignishandler. Wenn der Benutzer auf einen Wiedergabelistennamen klickt, ruft dieser Code die Attribute für diese Wiedergabeliste ab und zeigt diese Attribute in einem zweiten Listenfeld an.


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



Das SelectedIndexChanged-Ereignis für das ListBox-Steuerelement wird jedes Mal aufgerufen, wenn der Benutzer einen Wiedergabelistennamen auswählt. Der folgende Ereignishandler füllt ein zweites Listenfeld mit den Attributnamen und Werten aus, die der Auswahl des Benutzers entspricht.


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Medienelementattribute**](media-item-attributes.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> </dl>

 

 




