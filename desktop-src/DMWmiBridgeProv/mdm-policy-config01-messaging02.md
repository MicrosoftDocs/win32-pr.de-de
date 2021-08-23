---
title: MDM_Policy_Config01_Messaging02-Klasse
description: Die MDM \_ Policy \_ Config01 \_ Messaging02-Klasse ermöglicht das Sichern und Wiederherstellen von SMS und Messaging Everywhere. Mit dieser Richtlinie kann eine Organisation diese Features deaktivieren, um zu vermeiden, dass Informationen auf Servern gespeichert werden, die sich außerhalb ihrer Kontrolle befinden.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- MDM_Policy_Config01_Messaging02-Klasse
- MDM_Policy_Config01_Messaging02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5bd1b3d32ae63ffbcc1b4410fec853293f6c8794604d6e2859420025a84b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825640"
---
# <a name="mdm_policy_config01_messaging02-class"></a>MDM \_ Policy \_ Config01 \_ Messaging02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die MDM \_ Policy \_ Config01 \_ Messaging02-Klasse ermöglicht das Sichern und Wiederherstellen von SMS und Messaging Everywhere. Mit dieser Richtlinie kann eine Organisation diese Features deaktivieren, um zu vermeiden, dass Informationen auf Servern gespeichert werden, die sich außerhalb ihrer Kontrolle befinden.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a>Member

Die **MDM \_ Policy \_ Config01 \_ Messaging02-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ Policy \_ Config01 \_ Messaging02-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[AllowMessageSync](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

