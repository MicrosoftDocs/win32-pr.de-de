---
title: IMsRdpClientAdvancedSettings7 networkconnectiontype (Eigenschaft)
description: Ruft den Typ der Netzwerkverbindung ab, die zwischen Client und Server verwendet wird, oder legt ihn fest. Die an den Server weiter gegebenen Informationen zum Netzwerk Verbindungstyp helfen dem Server beim Optimieren mehrerer Parameter basierend auf dem Netzwerk Verbindungstyp.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Networkconnectiontype-Eigenschaft Remotedesktopdienste
- Networkconnectiontype-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, networkconnectiontype-Eigenschaft
- Networkconnectiontype-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, networkconnectiontype-Eigenschaft
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
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338745"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>IMsRdpClientAdvancedSettings7:: networkconnectiontype (Eigenschaft)

Ruft den Typ der Netzwerkverbindung ab, die zwischen Client und Server verwendet wird, oder legt ihn fest. Die an den Server weiter gegebenen Informationen zum Netzwerk Verbindungstyp helfen dem Server beim Optimieren mehrerer Parameter basierend auf dem Netzwerk Verbindungstyp.

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

Der Netzwerk Verbindungstyp.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Verbindung \_ \_Typmodem** (1 (0x1))


</dt> <dd>

Modem (56 Kbit/s)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Verbindung \_ Typ \_ Breitband \_ niedrig** (2 (0x2))


</dt> <dd>

Breitband mit niedriger Geschwindigkeit (256 KBit/s bis 2 Mbit/s)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Verbindung \_ \_Typsatellit** (3 (0x3))


</dt> <dd>

Satellit (2 Mbit/s bis 16 Mbit/s mit hoher Latenz)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Verbindung \_ Typ \_ Breitband \_ hoch** (4 (0x4))


</dt> <dd>

Hochgeschwindigkeitsbreitband (2 Mbit/s bis 10 Mbit/s)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Verbindung \_ Typ \_ WAN** (5 (0x5))


</dt> <dd>

WAN (Wide Area Network) (10 Mbit/s oder höher mit hoher Latenz)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Verbindung \_ \_LAN-Typ** (6 (0x6))


</dt> <dd>

LAN (Local Area Network) (10 Mbit/s oder höher)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





