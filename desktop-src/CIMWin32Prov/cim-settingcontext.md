---
description: Die CIM \_ SettingContext-Klasse ordnet Konfigurationsobjekte Einstellungsobjekten zu.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: CIM_SettingContext-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: df59bff8be90d3db3ac6dfde638120779850f2691bd3e93826c57f829d034a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919510"
---
# <a name="cim_settingcontext-class"></a>CIM \_ SettingContext-Klasse

Die **CIM \_ SettingContext-Klasse** ordnet Konfigurationsobjekte Einstellungsobjekten zu. Beispielsweise können sich die Einstellungen eines Netzwerkadapters basierend auf dem Standort oder Netzwerk ändern, an den bzw. das das Hostcomputersystem angefügt ist. In diesem Fall hat das Computersystem zwei verschiedene Konfigurationsobjekte, die den Unterschieden in der Netzwerkkonfiguration für die beiden Netzwerksegmente entsprechend sind. Eine Konfiguration würde ein Einstellungsobjekt für den Netzwerkadapter aggregieren, wenn es in einem Segment ausgeführt wird. Während die andere Konfiguration ein anderes Netzwerkadaptereinstellungsobjekt aggregieren würde, das für ein anderes Segment spezifisch ist. Beachten Sie, dass viele Computereinstellungen unabhängig von der Netzwerkkonfiguration sind. Beispielsweise würden beide Konfigurationen das gleiche Einstellungsobjekt für die Monitorauflösung des Computersystems aggregieren.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a>Member

Die **CIM \_ SettingContext-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SettingContext-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Konfiguration**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Aggregieren**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf das Konfigurationsobjekt, das die Einstellung aggregiert.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine aggregierte Einstellung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

