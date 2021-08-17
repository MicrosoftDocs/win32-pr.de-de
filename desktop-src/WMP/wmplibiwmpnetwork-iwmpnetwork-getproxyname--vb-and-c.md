---
title: IWMPNetwork getProxyName-Methode
description: Die getProxyName-Methode gibt den Namen des verwendeten Proxyservers zurück.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- getProxyName-Windows Media Player
- getProxyName-Methode Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , getProxyName-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c8c15df5e741c02bf3c47ecac8b3f57d4adddfeeb41cb6a71cf418b600006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745938"
---
# <a name="iwmpnetworkgetproxyname-method"></a>IWMPNetwork::getProxyName-Methode

Die **getProxyName-Methode** gibt den Namen des verwendeten Proxyservers zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrProtocol* \[ In\]
</dt> <dd>

Eine **System.String,** die der Protokollname ist. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,die** den Namen des verwendeten Proxyservers angibt. Der Wert ist nur sinnvoll, **wenn IWMPNetwork.getProxySettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).

## <a name="remarks"></a>Hinweise

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getProxyName** verwendet, um Windows Media Player Proxyservernamen für die HTTP- und MMS-Protokolle anzuzeigen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
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

[**IWMPNetwork.getProxySettings (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxyName (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





