---
title: IMsRdpClientAdvancedSettings LoadBalanceInfo (Eigenschaft)
description: Gibt das Lastenausgleichscookie an, das im X.224-Verbindungsanforderungspaket in der Verbindungssequenz des Remotedesktop-Sitzungshost-Servers (RD-Sitzungshost) platziert wird.
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- LoadBalanceInfo-Remotedesktopdienste
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
- LoadBalanceInfo-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , LoadBalanceInfo-Eigenschaft
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
ms.openlocfilehash: efe7ca9b9ed68f3327779177e706ee5a943c9e6580e2b789e2b96e74ee9f0b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353039"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>IMsRdpClientAdvancedSettings::LoadBalanceInfo (Eigenschaft)

Gibt das Lastenausgleichscookie an, das im X.224-Verbindungsanforderungspaket in der Verbindungssequenz des Remotedesktop-Sitzungshost-Servers (RD-Sitzungshost) platziert wird.

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

Gibt **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Die Lastenausgleichsinformationen werden von Lastenausgleichsroutern verwendet, um den besten Server für den Client zu wählen, wenn Farmen von RD-Sitzungshost werden. Der RD-Sitzungshost server selbst verwendet diese Informationen nicht und verwirft sie.

Das Cookie verwendet die folgende Syntax, bei der die Zwischenschreibung beachtet wird:

**Cookie: msts=**_IpAddressAndPortNumber_*_\\ r \\ n_*

Dabei *ist IpAddressAndPortNumber* die IP-Adresse und Portnummer in Netzwerk-Byte-Reihenfolge.

Beispielsweise lautet das Cookie für den Zugriff auf die IP-Adresse 172.31.249.216, Portnummer 3389, wie folgt:

**Cookie: msts=3640205228.15629.0000 \\ r \\ n**

Die letzten vier Nullen sind optional und reserviert. Das letzte Dezimaltrennzeichen ist erforderlich, ebenso wie der nachstellende Wagenrücklauf und der Zeilenumlauf. Die Länge der Zeichenfolge in Zeichen muss ein gleichmäßiges Vielfaches von 2 sein. Fügen Sie daher bei Bedarf ein Leerzeichen hinzu.

Wenn kein Cookie angegeben wird, ist der Standardwert **Cookie: mstshash=**_UserName_*_\\ r \\ n_*.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                  |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

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

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





