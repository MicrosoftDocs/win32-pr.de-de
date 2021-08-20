---
title: IMsRdpClientAdvancedSettings7 NetworkConnectionType-Eigenschaft
description: Ruft den Typ der Netzwerkverbindung ab, die zwischen Client und Server verwendet wird, oder legt diese fest. Die an den Server übergebenen Informationen zum Netzwerkverbindungstyp helfen dem Server, mehrere Parameter basierend auf dem Netzwerkverbindungstyp zu optimieren.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- NetworkConnectionType-Eigenschaft Remotedesktopdienste
- NetworkConnectionType-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , NetworkConnectionType-Eigenschaft
- NetworkConnectionType-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , NetworkConnectionType-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e331fde1a8f7013c376b99184a90e7b3bb9f599197259b044c4d1cbd38841584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352157"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>IMsRdpClientAdvancedSettings7::NetworkConnectionType-Eigenschaft

Ruft den Typ der Netzwerkverbindung ab, die zwischen Client und Server verwendet wird, oder legt diese fest. Die an den Server übergebenen Informationen zum Netzwerkverbindungstyp helfen dem Server, mehrere Parameter basierend auf dem Netzwerkverbindungstyp zu optimieren.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Netzwerkverbindungstyp.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION \_ TYPE \_ MODEM** (1 (0x1))


</dt> <dd>

Modem (56 KBit/s)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION \_ TYPE \_ BROADBAND \_ LOW** (2 (0x2))


</dt> <dd>

Breitband mit niedriger Geschwindigkeit (256 KBit/s bis 2 MBit/s)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION \_ TYPE \_ SATELLITE** (3 (0x3))


</dt> <dd>

Satellite (2 MBit/s bis 16 MBit/s, mit hoher Latenz)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION \_ TYPE \_ BROADBAND \_ HIGH** (4 (0x4))


</dt> <dd>

Hochgeschwindigkeits-Breitband (2 MBit/s bis 10 MBit/s)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION \_ TYPE \_ WAN** (5 (0x5))


</dt> <dd>

Wan (Wide Area Network) (10 MBit/s oder höher, mit hoher Latenz)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION \_ TYPE \_ LAN** (6 (0x6))


</dt> <dd>

Lokales Netzwerk (LAN) (10 MBit/s oder höher)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 ist als 26036036-4010-4578-8091-0db9a1edf9c3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





