---
description: Die \_ HWConfig-NIC-Klasse ist die Ereignistypklasse für Netzwerkschnittstellenkarten-Konfigurationsereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394724"
---
# <a name="hwconfig_nic-class"></a>\_HWConfig-NIC-Klasse

Die **\_ HWConfig-NIC-Klasse** ist die Ereignistypklasse für Netzwerkschnittstellenkarten-Konfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Member

Die **\_ HWConfig-NIC-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ HWConfig-NIC-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Name der Netzwerkschnittstellenkarte.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




