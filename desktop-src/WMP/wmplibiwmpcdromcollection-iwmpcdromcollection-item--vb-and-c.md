---
title: Iwmpcdromcollection-Element Methode
description: Die Item-Methode gibt eine iwmpcdrom-Schnittstelle am angegebenen Index zurück.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371167"
---
# <a name="iwmpcdromcollectionitem-method"></a>Iwmpcdromcollection:: Item-Methode

Die **Item** -Methode gibt eine **iwmpcdrom** -Schnittstelle am angegebenen Index zurück.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpcdrom** -Schnittstelle.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das- **Element** verwendet, um den laufwerkspezifizierer und den Wiedergabelisten Namen von allen auf dem Computer verfügbaren CD in einem Listenfeld anzuzeigen. Wenn das Laufwerk tatsächlich DVD-Inhalte enthält, ist Windows XP oder höher erforderlich. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdrom-Schnittstelle (VB und c#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle (VB und c#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromcollection. Count (VB und c#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromcollection. getbydrivespecifier (VB und c#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Name (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





