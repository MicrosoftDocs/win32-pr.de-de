---
description: Gibt an, ob Computer den integrierten automatischen Konfigurationsdienst (AutoConfig) zum Verwalten von Drahtlosverbindungen verwenden.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: enableAutoConfig-Element (globalFlags) (LAN_policy) für WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 77b09bf046cdbadb58c888a3084d14ed14794064bf9f11c110ccecaff105fceb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684410"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>enableAutoConfig-Element (globalFlags) (LAN_policy) für WLAN 

Das **element enableAutoConfig** (globalFlags) gibt an, ob Computer den integrierten automatischen Konfigurationsdienst (AutoConfig) zum Verwalten von Drahtlosverbindungen verwenden. Wenn **enableAutoConfig** den Wert FALSE hat, dürfen Computer autoConfig nicht zum Verwalten von Drahtlosverbindungen verwenden, und der AutoConfig-Dienst reagiert nur auf Anforderungen, um den Dienst zu aktivieren. Wenn **enableAutoConfig** den Wert TRUE auf hat, können Computer den AutoConfig-Dienst verwenden.

Dieses Element ist obligatorisch. Wenn vom AutoConfig-Dienst ein Profil erstellt wird, hat dieses Element den Standardwert TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

Das **enableAutoConfig-Element** wird durch das [**globalFlags-Element**](wlan-policyschema-globalflags-wlanpolicy-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




