---
title: Imsrdpclientadvancedsettings loadbalanceinfo-Eigenschaft
description: Gibt das Lasten Ausgleichs Cookie an, das in der Verbindungs Sequenz des Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Protokolls in das X. 224-Verbindungs Anforderungspaket eingefügt wird.
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste
- Loadbalanceinfo-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, loadbalanceinfo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391737"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>Imsrdpclientadvancedsettings:: loadbalanceinfo-Eigenschaft

Gibt das Lasten Ausgleichs Cookie an, das in der Verbindungs Sequenz des Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Protokolls in das X. 224-Verbindungs Anforderungspaket eingefügt wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>Eigenschaftswert

Zeiger auf das neue Cookie. Weitere Informationen finden Sie im Abschnitt "Hinweise".

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Die Informationen zum Lastenausgleich werden von Lasten Ausgleichs Routern verwendet, um den besten Server für den Client auszuwählen, wenn RD-Sitzungshost Serverfarmen verwendet werden. Der RD-Sitzungshost Server selbst verwendet diese Informationen nicht und verwirft ihn.

Das Cookie verwendet die folgende Syntax, wobei die Groß-/Kleinschreibung beachtet wird:

**Cookie: MSTS =**_ipaddressandportnumber_*_\\ r \\ n_*

Dabei ist " *ipaddressandportnumber* " die IP-Adresse und die Portnummer in der Netzwerk-Byte-Reihenfolge.

Beispielsweise ist das Cookie, das für den Zugriff auf die IP-Adresse von 172.31.249.216 verwendet wird, Portnummer 3389 wie folgt:

**Cookie: MSTS = 3640205228.15629.0000 \\ r \\ n**

Die letzten vier Nullen sind optional und reserviert. Der abschließende Dezimaltrennzeichen ist erforderlich, ebenso wie der nachfolgende Wagen Rücklauf und Zeilenvorschub. Die Länge der Zeichenfolge in Zeichen muss ein gleich Vielfaches von 2 sein. Fügen Sie daher ggf. ein Leerzeichen hinzu.

Wenn kein Cookie angegeben ist, lautet der Standardwert **Cookie: mstshash =**_username_*_\\ r \\ n_*.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





