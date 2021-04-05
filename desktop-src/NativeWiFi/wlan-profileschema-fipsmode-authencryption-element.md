---
description: Gibt an, ob der Federal Information Processing Standards (fps)-Modus aktiviert ist.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Mepsmode-Element (authencryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752304"
---
# <a name="fipsmode-authencryption-element"></a>Mepsmode-Element (authencryption)

Das Element " **fpsmode** (authencryption)" gibt an, ob der Modus "Federal Information Processing Standards (fps)" aktiviert ist. Wenn eine drahtlose Verbindung im PPS-Modus betrieben wird, entspricht die Sicherheitsstufe der Verbindung 140-2 dem Standard-Standard von Standard. Weitere Informationen zu "fps" finden Sie auf der [Startseite](https://www.itl.nist.gov/fipspubs/)von "Fi".

Dieses Element ist optional. Wenn dieses Element nicht in einem Profil angegeben wird, ist der Modus "PPS" nicht aktiviert.

" **Fpsmode** " kann nur auf "true" festgelegt werden, wenn die folgenden Bedingungen erfüllt sind:

-   Das [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) -Element hat den Wert `ESS` (d. h. die Verbindung ist eine infrastrukturverbindung).
-   Das [**Authentifizierungs**](wlan-profileschema-authentication-authencryption-element.md) Element hat den Wert `WPA2` oder `WPA2PSK` .
-   Das [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Element weist den Wert auf `AES` .

Anders als die meisten Elemente im WLAN- \_ Profil Schema befindet sich dieses Element im- `https://www.microsoft.com/networking/WLAN/profile/v2` Namespace.

**Der Wert des Elements "** -Element" wird ignoriert, wenn der Mini Port-Treiber für die drahtlos Schnittstelle den PPS-Modus nicht unterstützt.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt. Wenn " **fpsmode** " in einem Profil vorhanden ist, wird das-Element ignoriert.

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="examples"></a>Beispiele

Ein Beispiel Profil, das das-Element in der-Datei verwendet, finden Sie unter Beispiel für das **PPS** - [Profil](fips-profile-sample.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**authencryption (Sicherheit)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
