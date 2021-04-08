---
description: Bestimmt das Roamingverhalten eines automatisch verbundenen Netzwerks, wenn ein bevorzugtes Netzwerk in Reichweite ist.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: autoswitch (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863347"
---
# <a name="autoswitch-wlanprofile-element"></a>autoswitch (wlanprofile)-Element

Das autoswitch (wlanprofile)-Element bestimmt das Roamingverhalten eines automatisch verbundenen Netzwerks, wenn ein bevorzugtes Netzwerk in Reichweite ist. . Dieses Element ist optional.

Wenn autoswitch den Wert "true" hat und [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) auf "Auto" festgelegt ist, muss eine Verbindung mit einem besser bevorzugten Netzwerk versucht werden, wenn ein bevorzugtes Netzwerk in den Bereich kommt. Ein bevorzugtes Netzwerk ist ein höheres Netzwerk in der Liste der bevorzugten Drahtlos Netzwerke. Dieser Verbindungsversuch tritt auf, wenn eine Verbindung mit einem anderen Netzwerk besteht.

Wenn [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) auf "Auto" festgelegt ist, kann dieser Wert entweder "true" oder "false" lauten.

Wenn [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) auf "Manual" festgelegt ist, muss dieser Wert auf "false" festgelegt werden. Dieses Element hat keine Auswirkung auf ein manuell verbundenes Netzwerk.

Ein autoswitch-Wert, der auf "true" festgelegt ist, führt zu einer höheren Häufigkeit der regelmäßigen Überprüfung neuer Netzwerke. Dies kann dazu führen, dass regelmäßige Überprüfungen und erhöhter Stromverbrauch durch den Drahtlos Netzwerkadapter verstärkt werden.

**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren. Diese Änderungen sind so konzipiert, dass die Radiofrequenz Belastung, der Stromverbrauch und die Unterbrechung des Echt Zeit Datenverkehrs über Drahtlos Netzwerke reduziert werden. Die Standardeinstellung für **autoswitch** , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert. Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist. Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt. Es wird empfohlen, den Wert des **autoswitch** -Elements, das von einer Anwendung in einem WLAN-Profil verwendet wird, auf "false" festzulegen, um die Häufigkeit der regelmäßigen Überprüfung auf neue Netzwerke zu reduzieren, es sei denn, es ist erforderlich, dass eine Anwendung diesen Wert auf "true" festgelegt.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

Das **autoswitch** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **autoswitch** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




