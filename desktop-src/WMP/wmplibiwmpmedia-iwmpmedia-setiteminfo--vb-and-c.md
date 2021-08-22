---
title: IWMPMedia setItemInfo-Methode
description: Die setItemInfo-Methode legt den Wert des angegebenen Attributs für das Medienelement fest.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- setItemInfo-Methode Windows Media Player
- setItemInfo-Methode Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , setItemInfo-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24265e94880899df96aa954f2df30ca6e4f5ae1e5b4fc20c419085e3f9f0ab14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053638"
---
# <a name="iwmpmediasetiteminfo-method"></a>IWMPMedia::setItemInfo-Methode

Die **setItemInfo-Methode** legt den Wert des angegebenen Attributs für das Medienelement fest.

## <a name="syntax"></a>Syntax


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrItemName* \[ In\]
</dt> <dd>

Eine **System.String,die** der Attributname ist.

</dd> <dt>

*bstrVal* \[ In\]
</dt> <dd>

Eine **System.String,die** der neue Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **attributeCount-Eigenschaft** ruft die Anzahl von Attributen ab, die für ein bestimmtes Medienelement verfügbar sind. Indexnummern können dann mit der **getAttributeName-Methode** verwendet werden, um die Namen der integrierten Attribute zu bestimmen, die mit dieser Methode verwendet werden können.

Verwenden Sie vor der Verwendung dieser Methode die **isReadOnlyItem-Methode,** um zu ermitteln, ob ein bestimmtes Attribut festgelegt werden kann.

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Hinweis

Wenn Sie das Windows Media Player-Steuerelement in Ihre Anwendung einbetten, werden dateiattribute, die Sie ändern, erst in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player ausführt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **setItemInfo** verwendet, um den Wert des Genre-Attributs für das aktuelle Medienelement zu ändern. Mit einem Textfeld kann der Benutzer eine Zeichenfolge eingeben, die dann verwendet wird, um die Attributinformationen als Reaktion auf das Click-Ereignis einer Schaltfläche zu ändern. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
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

[**IWMPMedia.attributeCount (VB und C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.isReadOnlyItem (VB und C#)**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





