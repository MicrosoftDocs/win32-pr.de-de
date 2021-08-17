---
title: IWMPNetwork setProxyExceptionList-Methode
description: Die setProxyExceptionList-Methode gibt die Proxyausnahmeliste an. | IWMPNetwork setProxyExceptionList-Methode
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- setProxyExceptionList-Windows Media Player
- setProxyExceptionList-Methode Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , setProxyExceptionList-Methode
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
ms.openlocfilehash: eddfd3ce8495c02fc6ae352f918349ff7174afb99e69d9e1ba8aa19c45d1a49d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745762"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a>IWMPNetwork::setProxyExceptionList-Methode

Die **setProxyExceptionList-Methode** gibt die Proxyausnahmeliste an.

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

*bstrProtocol* \[ In\]
</dt> <dd>

Eine **System.String,** die der Protokollname ist. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> <dt>

*pbstrExceptionList* \[ In\]
</dt> <dd>

Eine **System.String,** die eine durch Semikolons getrennte Liste von Hosts ist, für die der Proxyserver umgangen wird. Führende und nachstellende Leerzeichen sollten nicht vorhanden sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxyserver umgehen, wenn der Hostteil der Ziel-URL einem Eintrag in der Liste entspricht.

Das \* Zeichen kann als Platzhalterzeichen zum Auflisten von Einträgen verwendet werden. Beispielsweise würde .com mit allen Hosts in der Com-Domäne übereinstimmen, während 67. mit allen Hosts \* \* im Subnetz der 67-Klasse A übereinstimmen würde.

Diese Methode hat keine Auswirkungen, es sei denn, der von **IWMPNetwork.getProxySettings** abgerufene Wert ist 2 (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **setProxyExceptionList** verwendet, um eine Liste von Hosts anzugeben, für die der Proxyserver umgangen wird, wenn das MMS-Protokoll verwendet wird. Die neue Liste wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxyExceptionList (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





