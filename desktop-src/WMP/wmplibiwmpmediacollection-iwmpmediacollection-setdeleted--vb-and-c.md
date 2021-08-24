---
title: IWMPMediaCollection setDeleted-Methode
description: Die setDeleted-Methode verschiebt das angegebene Medienelement in den Ordner für gelöschte Elemente. | IWMPMediaCollection setDeleted-Methode
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- setDeleted-Methode Windows Media Player
- setDeleted-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , setDeleted-Methode
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
ms.openlocfilehash: 7516d6aab26659fa2bba57bd961671b4dca0f92d367d5d9bb1f048e8fd19eb2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505950"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>IWMPMediaCollection::setDeleted-Methode

Die `setDeleted` -Methode verschiebt das angegebene Medienelement in den Ordner für gelöschte Elemente.

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

*pItem* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPMedia-Schnittstelle** für das zu verschiebende Element.

</dd> <dt>

*varfIsDeleted* \[ In\]
</dt> <dd>

Ein **System.Boolean-Wert,** der angibt, ob das Element in den Ordner gelöschte Elemente verschoben werden soll. Dieser Wert muss immer **true** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode entfernt keine Dateien vom Computer des Benutzers, sie verschiebt sie lediglich in den Ordner gelöschte Elemente.

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird `setDeleted` verwendet, um ein bestimmtes Medienelement in den Ordner für gelöschte Elemente zu verschieben. Die **isDeleted-Methode** testet zunächst, ob das Element bereits gelöscht wurde. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





