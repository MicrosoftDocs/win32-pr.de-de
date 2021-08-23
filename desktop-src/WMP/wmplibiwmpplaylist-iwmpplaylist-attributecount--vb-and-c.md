---
title: IWMPPlaylist attributeCount-Eigenschaft
description: Die attributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die einer Wiedergabeliste zugeordnet sind.
ms.assetid: 0713ec4e-7e06-4ad2-8f7c-17ed5a92d5ee
keywords:
- attributeCount-Eigenschaft Windows Media Player
- attributeCount-Eigenschaft Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , attributeCount-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b51c621f5a484c23a2f7d0677fe20d1b62bfb4d2ec94228e003adc2ebc841cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760770"
---
# <a name="iwmpplaylistattributecount-property"></a>IWMPPlaylist::attributeCount-Eigenschaft

Die **attributeCount-Eigenschaft** ruft die Anzahl der Attribute ab, die einer Wiedergabeliste zugeordnet sind.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 attributeCount {get; set;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Int32-Datei,** die der Anzahl von Attributen entspricht, die der Wiedergabeliste zugeordnet sind.

## <a name="remarks"></a>Hinweise

Da Wiedergabelisten aus vielen verschiedenen Quellen stammen können, können sie über mehrere unterschiedliche Attribute verfügen. Diese Eigenschaft ruft die Gesamtzahl der Attribute ab, die einer bestimmten Wiedergabeliste zugeordnet sind, sodass andere Member der **IWMPPlaylist-Schnittstelle** darauf zugreifen können.

Bevor Sie diese Eigenschaft verwenden können, benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Weitere Informationen zu Attributen, die von Windows Media Player unterstützt werden, finden Sie unter [Attributverweis.](attribute-reference.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie verschiedene Eigenschaften und Methoden der **IWMPPlaylist-** und **IWMPMedia-Schnittstellen** verwendet werden, indem ein Treeview-Steuerelement mit Knoten für die aktuelle Wiedergabeliste, Wiedergabelistenattribute, Medienelemente in der Wiedergabeliste und Medienelementattribute gefüllt wird. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
WMPLib.IWMPPlaylist playlist = player.currentPlaylist;
WMPLib.IWMPMedia media;
string name;

// Demonstrates setItemInfo()
playlist.setItemInfo("custom playlist attribute", "changed");
playlist.get_Item(0).setItemInfo("new custom attribute", "5");

// Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
System.Windows.Forms.TreeNode playlistRootNode = new System.Windows.Forms.TreeNode("Playlist Attributes");

for (int i = 0; i < playlist.attributeCount; ++i)
{
    // Add a tree node for each playlist attribute.
    string attribute = playlist.get_attributeName(i);
    playlistRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(attribute));

    // Add a subnode for the item info for that attribute.
    string info = playlist.getItemInfo(attribute);
    playlistRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(info));
}

// Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode);

// Add nodes for each media item and subnodes for each attribute of that item.
System.Windows.Forms.TreeNode mediaRootNode = new System.Windows.Forms.TreeNode("Media Items in the Playlist");
for(int i = 0; i < playlist.count; i++)
{
    // Get the media item
    media = playlist.get_Item(i);

    // Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(media.name));

    // Add a child node for each attribute of the media item
    for(int j = 0; j < media.attributeCount; j++)
    {
        name = media.getAttributeName(j);
        mediaRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(name + ": " + media.getItemInfo(name)));
    }
}

// Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode);
```


```VB

Dim playlist As WMPLib.IWMPPlaylist = player.currentPlaylist
Dim Media As WMPLib.IWMPMedia
Dim name As String

&#39; Demonstrates setItemInfo()
playlist.setItemInfo(&quot;custom playlist attribute&quot;, &quot;changed&quot;)
playlist.Item(0).setItemInfo(&quot;new custom attribute&quot;, &quot;5&quot;)

&#39; Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
Dim playlistRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Playlist Attributes&quot;)

For i As Integer = 0 To (playlist.attributeCount - 1) Step 1

    &#39; Add a tree node for each playlist attribute.
    Dim attribute As String = playlist.attributeName(i)
    playlistRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(attribute))

    &#39; Add a subnode for the item info for that attribute.
    Dim info As String = playlist.getItemInfo(attribute)
    playlistRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(info))

Next i

&#39; Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode)

&#39; Add nodes for each media item and subnodes for each attribute of that item.
Dim mediaRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Media Items in the Playlist&quot;)

For i As Integer = 0 To (playlist.count - 1) Step 1

    &#39; Get the media item
    Media = playlist.Item(i)

    &#39; Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(Media.name))

    &#39; Add a child node for each attribute of the media item
    For j As Integer = 0 To (Media.attributeCount - 1) Step 1

        name = Media.getAttributeName(j)
        mediaRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(name + &quot;: &quot; + Media.getItemInfo(name)))

    Next j

Next i

&#39; Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode)
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





