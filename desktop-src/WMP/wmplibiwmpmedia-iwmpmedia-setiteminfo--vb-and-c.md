---
title: Iwmpmedia-Methode "* titeminfo"
description: Die setiteminfo-Methode legt den Wert des angegebenen Attributs für das Medien Element fest.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo", Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, Methode "stiteminfo"
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
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356499"
---
# <a name="iwmpmediasetiteminfo-method"></a>Iwmpmedia:: abtiteminfo-Methode

Die **setiteminfo** -Methode legt den Wert des angegebenen Attributs für das Medien Element fest.

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

*bstritemname* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Attribut Name ist.

</dd> <dt>

*bstrauval* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der neue Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **AttributeCount** -Eigenschaft ruft die Anzahl der für ein bestimmtes Medien Element verfügbaren Attribute ab. Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um die Namen der integrierten Attribute zu bestimmen, die mit dieser Methode verwendet werden können.

Verwenden Sie vor der Verwendung dieser Methode die **isread onlyitem** -Methode, um zu ermitteln, ob ein bestimmtes Attribut festgelegt werden kann.

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Hinweis

Wenn Sie das Windows Media Player-Steuerelement in Ihre Anwendung einbetten, werden Dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player ausführt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der Wert des Genre-Attributs für das aktuelle Medien Element mithilfe von " **sminfo** " geändert. Ein Textfeld ermöglicht dem Benutzer die Eingabe einer Zeichenfolge, die dann verwendet wird, um die Attributinformationen als Reaktion auf das Click-Ereignis einer Schaltfläche zu ändern. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. AttributeCount (VB und c#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. GetAttributeName (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. isleseronlyitem (VB und c#)**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





