---
title: "' Iwmpmediacollection ' (SetDeleted-Methode)"
description: Die SetDeleted-Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente". | ' Iwmpmediacollection ' (SetDeleted-Methode)
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- SetDeleted-Methoden Fenster Media Player
- SetDeleted-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, SetDeleted-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370841"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>Iwmpmediacollection:: SetDeleted-Methode

Die- `setDeleted` Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".

## <a name="syntax"></a>Syntax


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pitem* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpmedia** -Schnittstelle für das Element, das verschoben werden soll.

</dd> <dt>

*varfisdeleted* \[ in\]
</dt> <dd>

Ein **System. Boolean** -Wert, der angibt, ob das Element in den Ordner für gelöschte Elemente verschoben werden soll. Dieser Wert muss immer " **true**" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode entfernt keine Dateien vom Computer des Benutzers, sondern verschiebt Sie lediglich in den Ordner "Gelöschte Elemente".

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird verwendet `setDeleted` , um ein bestimmtes Medien Element in den Ordner "Gelöschte Elemente" zu verschieben. Die **isDeleted** -Methode testet zunächst, ob das Element bereits gelöscht wurde. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





