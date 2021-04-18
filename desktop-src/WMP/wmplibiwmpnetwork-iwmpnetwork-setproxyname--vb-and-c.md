---
title: Iwmpnetwork setproxyname-Methode
description: Die setproxyname-Methode gibt den Namen des zu verwendenden Proxy Servers an. | Iwmpnetwork setproxyname-Methode
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- setproxyname-Methode, Windows Media Player
- setproxyname-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxyname-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355054"
---
# <a name="iwmpnetworksetproxyname-method"></a>Iwmpnetwork:: setproxyname-Methode

Die **setproxyname** -Methode gibt den Namen des zu verwendenden Proxy Servers an.

## <a name="syntax"></a>Syntax


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauprotocol* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Protokoll Name ist. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*bstrinproxyname* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der den Namen des zu verwendenden Proxy Servers ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode hat keine Auswirkung, es sei denn, der Wert, der von **iwmpnetwork. getproxysettings** abgerufen wird, ist 2 (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **setproxyname** verwendet, um den Namen des Windows Media Player-Proxy Servers für das MMS-Protokoll anzugeben. Der neue Name wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

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

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. getproxyname (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. getproxysettings (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





