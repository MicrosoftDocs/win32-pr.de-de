---
title: IWMPNetwork getProxyExceptionList-Methode
description: Die getProxyExceptionList-Methode gibt die Proxyausnahmeliste zurück.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- getProxyExceptionList-Windows Media Player
- getProxyExceptionList-Methode Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , getProxyExceptionList-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96434d4ea2341a8d33fcb9673898f4adca5eae7ace27eb7a7cafb9d482d74a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053538"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a>IWMPNetwork::getProxyExceptionList-Methode

Die **getProxyExceptionList-Methode** gibt die Proxyausnahmeliste zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrProtocol* \[ In\]
</dt> <dd>

Eine **System.String,** die der Protokollname ist. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die eine durch Semikolons getrennte Liste von Hosts ist, für die der Proxyserver umgangen wird. Der Wert ist nur sinnvoll, **wenn IWMPNetwork.getProxySettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).

## <a name="remarks"></a>Hinweise

Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxyserver umgehen, wenn der Hostteil der Ziel-URL einem Eintrag in der Liste entspricht.

Das \* Zeichen kann als Platzhalterzeichen zum Auflisten von Einträgen verwendet werden. Beispielsweise würde .com mit allen Hosts in der Com-Domäne übereinstimmen, während 67. mit allen Hosts \* \* im Subnetz der 67-Klasse A übereinstimmen würde.

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getProxyExceptionList** verwendet, um anzuzeigen, ob Windows Media Player festgelegt ist, um den Proxyserver für lokale Adressen zu umgehen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxyExceptionList (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





