---
description: Stellt einen Drahtloskommunikationsendpunkt dar, der Datenrahmen senden und empfangen kann, wenn das zugehörige Schnittstellengerät mit einem IEEE 802.11-Drahtlos-LAN verbunden ist.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: CIM_WiFiEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b188c59be8ca6fc6c1d171c4c030fa222e0fb8d4ac22622979304d975d74a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646323"
---
# <a name="cim_wifiendpoint-class"></a>CIM \_ WiFiEndpoint-Klasse

Stellt einen Drahtloskommunikationsendpunkt dar, der Datenrahmen senden und empfangen kann, wenn das zugehörige Schnittstellengerät mit einem IEEE 802.11-Drahtlos-LAN verbunden ist.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a>Member

Die **CIM \_ WiFiEndpoint-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ WiFiEndpoint-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessPointAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die MAC-Adresse des Zugriffspunkts, der dem Wi-Fi-Endpunkt zugeordnet ist. Andernfalls **NULL.**

</dd> <dt>

**Zugeordnet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der WLAN-Endpunkt derzeit einem Zugriffspunkt oder einer Clientstation zugeordnet ist; andernfalls **FALSE.**

</dd> <dt>

**AuthenticationMethod**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**", "**CIM \_ WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM \_ WiFiEndpoint**.**OtherAuthenticationMethod**")
</dt> </dl>

Der Authentifizierungstyp, der zwischen dem Wi-Fi-Endpunkt und dem Netzwerk verwendet wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

**Open System** (2)


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

**Gemeinsam verwendeter Schlüssel** (3)


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

**WPA PSK** (4)


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

**WPA IEEE 802.1x** (5)


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

**WPA2 PSK** (6)


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

**WPA2 IEEE 802.1x** (7)


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

**CCKM IEEE 802.1x** (8)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (9..)


</dt> <dd></dd> </dl>

</dd> <dt>

**BSSType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")
</dt> </dl>

Der BSS-Typ (Basic Service Set) des Netzwerks, das der Instanz entspricht. Ein BSS ist eine Reihe von Stationen, die von einer einzigen Koordinationsfunktion gesteuert werden.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Unabhängig** (2)


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

**Infrastruktur** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (4..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Encryptionmethod**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**", "**CIM \_ WiFiEndpoint**.**OtherEncryptionMethod**")
</dt> </dl>

Der Verschlüsselungstyp, der beim Senden und Empfangen von Daten über den Wi-Fi Endpunkt verwendet wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

**WEP** (2)


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

**TKIP** (3)


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

**CCMP** (4)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (6..)


</dt> <dd></dd> </dl>

</dd> <dt>

**IEEE8021xAuthenticationProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF", "RFC2716. IETF", "draft-ietf-ppext-eap-ttls. IETF", "draft-kamath-ppext-peapv0. IETF", "draft-feldernsson-tlsext-eap-tls-eap", "RFC4851. IETF", "RFC3748. IETF", "RFC4764. IETF", "RFC4186. IETF", "RFC4187. IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")
</dt> </dl>

Der EAP-Typ (Extensible Authentication Protocol) für den Wi-Fi Endpunkt, wenn **AuthenticationMethod** "7" (WPA IEEE 802.1x) oder "8" (CCKM IEEE 802.1x) enthält.

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

**EAP-TLS** (0)


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

**EAP-TTLS/MSCHAPv2** (1)


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

**PEAPv0/EAP-MSCHAPv2** (2)


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

**PEAPv1/EAP-GTC** (3)


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

**EAP-FAST/MSCHAPv2** (4)


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

**EAP-FAST/GTC** (5)


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

**EAP-MD5** (6)


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

**EAP-PSK** (7)


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

**EAP-SIM** (8)


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

**EAP-AKA** (9)


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

**EAP-FAST/TLS** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (11..)


</dt> <dd></dd> </dl>

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")
</dt> </dl>

Der Dienstsatzbezeichner (SSID) des Drahtlos-LAN, das dem Wi-Fi-Endpunkt zugeordnet ist. Andernfalls **NULL.**

</dd> <dt>

**OtherAuthenticationMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")
</dt> </dl>

Der Authentifizierungstyp, der zwischen dem Wi-Fi-Endpunkt und dem Netzwerk verwendet wird, wenn **AuthenticationMethod** "1" (Other) enthält.

</dd> <dt>

**OtherEncryptionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**")
</dt> </dl>

Beschreibt den Verschlüsselungstyp für den Wi-Fi Endpunkt, wenn **EncryptionMethod** "1" (Sonstige) enthält.

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")
</dt> </dl>

Die Kategorie oder Klassifizierung dieser Instanz. Die möglichen Werte sind auf die Wi-Fi und reservierten Werte aus dmtf und [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib)beschränkt.

Wenn **ProtocolIFType** auf "1" (Other) festgelegt ist, sollten die Typinformationen in der **OtherTypeDescription-Eigenschaft** bereitgestellt werden.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

**IEEE 802.11** (71)


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

**Reservierte IANA** (225..4095)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserved** (4301..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768.)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ LANEndpoint**](cim-lanendpoint.md)
</dt> </dl>

 

