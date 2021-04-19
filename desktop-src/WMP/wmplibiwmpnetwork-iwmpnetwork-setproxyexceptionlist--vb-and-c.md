---
title: Iwmpnetwork setproxyexceptionlist-Methode
description: Die setproxyexceptionlist-Methode gibt die Proxy Ausnahmeliste an. | Iwmpnetwork setproxyexceptionlist-Methode
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- setproxyexceptionlist-Methode, Windows Media Player
- setproxyexceptionlist-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxyexceptionlist-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372780"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a>Iwmpnetwork:: setproxyexceptionlist-Methode

Die **setproxyexceptionlist** -Methode gibt die Proxy Ausnahmeliste an.

## <a name="syntax"></a>Syntax


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauprotocol* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Protokoll Name ist. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*pbstrexceptionlist* \[ in\]
</dt> <dd>

Eine **System. String** , bei der es sich um eine durch Semikolons getrennte Liste von Hosts handelt, für die der Proxy Server umgangen wird. Führende und nachfolgende Leerzeichen sollten nicht vorhanden sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxy Server umgehen, wenn der Hostteil der Ziel-URL mit einem Eintrag in der Liste übereinstimmt.

Das \* Zeichen kann als Platzhalter Zeichen zum Auflisten von Einträgen verwendet werden. Beispielsweise \* entspricht ". com" allen Hosts in der com-Domäne, und 67. \* entspricht allen Hosts in der 67-Klasse einem Subnetz.

Diese Methode hat keine Auswirkung, es sei denn, der Wert, der von **iwmpnetwork. getproxysettings** abgerufen wird, ist 2 (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **setproxyexceptionlist** verwendet, um eine Liste von Hosts anzugeben, für die der Proxy Server bei Verwendung des MMS-Protokolls umgangen wird. Die neue Liste wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

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

[**Iwmpnetwork. getproxyexceptionlist (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. getproxysettings (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





