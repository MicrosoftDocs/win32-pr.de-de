---
description: Die CIM \_ settingcontext-Klasse ordnet Konfigurationsobjekte Einstellungs Objekten zu.
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
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958269"
---
# <a name="cim_settingcontext-class"></a>CIM \_ settingcontext-Klasse

Die **CIM \_ settingcontext** -Klasse ordnet Konfigurationsobjekte Einstellungs Objekten zu. Beispielsweise können sich die Einstellungen eines Netzwerkadapters je nach Standort oder Netzwerk ändern, an das das Host Computersystem angefügt ist. In diesem Fall würde das Computersystem zwei verschiedene Konfigurationsobjekte aufweisen, die den Unterschieden in der Netzwerkkonfiguration für die beiden Netzwerksegmente entsprechen. Eine Konfiguration würde ein Einstellungs Objekt für den Netzwerkadapter bei der Arbeit in einem Segment aggregieren. während die andere Konfiguration ein anderes Netzwerkadapter-Einstellungs Objekt aggregiert, das für ein anderes Segment spezifisch ist. Beachten Sie, dass viele Computereinstellungen unabhängig von der Netzwerkkonfiguration sind. Beispielsweise würden beide Konfigurationen das gleiche Einstellungs Objekt für die Monitor Auflösung des Computer Systems aggregieren.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ settingcontext** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ settingcontext** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Konfiguration**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf das Konfigurationsobjekt, das die Einstellung aggregiert.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine aggregierte Einstellung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

