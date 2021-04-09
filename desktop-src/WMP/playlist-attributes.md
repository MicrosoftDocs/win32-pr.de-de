---
title: Wiedergabelisten Attribute
description: Wiedergabelisten Attribute
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, Attribute
- Metadatei-Wiedergabelisten, Attribute
- Windows Media Metadatei-Wiedergabelisten, Attribute
- Attribute, Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947586"
---
# <a name="playlist-attributes"></a>Wiedergabelisten Attribute

Wiedergabelisten verfügen über Metadateninformationen, die so genannten Attribute sind, wie Medienelemente Attribute aufweisen. Sie können die Namen und Werte von Wiedergabelisten Attributen abrufen und in der Benutzeroberfläche anzeigen, oder der Code kann basierend auf dem Wert eines Attributs Aktionen ausführen.

Wiedergabelisten werden in Dateien definiert, die in einem XML-Format organisiert sind, und bestimmte Elemente in der Datei definieren Wiedergabelisten Attribute. Einige Attribut Elemente sind gut bekannt. der Autor der Metadatei kann auch beliebige Attribute definieren. Weitere Informationen zu Attribut Elementen in Wiedergabelisten Dateien finden Sie unter [Abrufen von Metadaten](retrieving-metadata.md).

Die Bibliothek kann zusätzliche Wiedergabelisten Attribute wie **SourceUrl** oder **userlastplayedtime** bereitstellen. Weitere Informationen zu den Wiedergabelisten Attributen der Bibliothek finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

Die *Wiedergabeliste*. **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind. Die *Wiedergabeliste*. **attributeName** -Eigenschaft ruft den Namen eines Attributs basierend auf seinem Index und der *Wiedergabeliste* ab. die **getiteminfo** -Methode ruft den Wert eines Attributs anhand des Namens ab.

Sie können den Wert eines Attributs der aktuellen Wiedergabeliste mit der *Wiedergabeliste* ändern. die Methode " **stiteminfo** ".

Eine besondere Verwendung **der Methode "** Methode" ist das Sortieren der Elemente in der Wiedergabeliste mithilfe des **SortAttribute** -Attributs. Im folgenden c#-Beispiel wird eine Wiedergabeliste nach den Werten des **userlastplayedtime** -Attributs sortiert. Die Variablen *Wiedergabeliste* ist ein Verweis auf ein **Wiedergabe** Listen Objekt.


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



In diesem Thema wurde das **Player** -Objekt wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Der folgende c#-Beispielcode veranschaulicht das Abrufen von Wiedergabelisten Attributen. Die erste Funktion, showplaylists, füllt ein ListBox-Steuerelement mit den Namen der verfügbaren Wiedergabelisten. Der zweite Teil ist der Listenfeld-Ereignishandler. Wenn der Benutzer auf einen Wiedergabelisten Namen klickt, ruft dieser Code die Attribute für die Wiedergabeliste ab und zeigt diese Attribute in einem zweiten Listenfeld an.


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



Das SelectedIndexChanged-Ereignis für das ListBox-Steuerelement wird jedes Mal aufgerufen, wenn der Benutzer einen Wiedergabelisten Namen auswählt. Der folgende Ereignishandler füllt ein zweites Listenfeld mit den Attributnamen und den Werten aus, die der Auswahl des Benutzers entsprechen.


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

[**Medien Element Attribute**](media-item-attributes.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> </dl>

 

 




