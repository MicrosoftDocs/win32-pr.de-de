---
description: Die hwconfig- \_ NIC-Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050366"
---
# <a name="hwconfig_nic-class"></a>Hwconfig- \_ NIC-Klasse

Die **hwconfig- \_ NIC** -Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Member

Die **hwconfig- \_ NIC** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **hwconfig- \_ NIC** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

NICNAME
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Der Name der Netzwerkschnittstellenkarte.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hwconfig**](hwconfig.md)
</dt> </dl>

 

 




