---
title: MDM_Policy_User_Result01_Notifications02-Klasse
description: Die Klasse MDM \_ Policy \_ User \_ Result01 \_ Notifications02 stellt die verfügbaren Benachrichtigungsrichtlinien dar.
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- MDM_Policy_User_Result01_Notifications02-Klasse
- MDM_Policy_User_Result01_Notifications02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91143ffaba94abb42acf84f20e537ce81148bb15ab073f5f5318a6b7524633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077014"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a>MDM \_ Policy \_ User \_ Result01 \_ Notifications02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **Klasse MDM Policy User \_ \_ \_ Result01 \_ Notifications02** stellt die verfügbaren Benachrichtigungsrichtlinien dar.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a>Member

Die **MDM Policy User \_ \_ \_ Result01 \_ Notifications02-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM Policy User \_ \_ \_ Result01 \_ Notifications02-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[DisallowNotificationMirroring](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
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

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse lautet die Zeichenfolge "Notifications".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse lautet die Zeichenfolge "./User/Vendor/MSFT/Policy/Result".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                            |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>\\Mofs-DMWmiBridgeProv.dll</dt> </dl> |



 

