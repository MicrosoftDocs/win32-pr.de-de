---
description: Die CIM \_ -Einstellungs Klasse stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: CIM_Setting-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861020"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a>CIM_Setting-Klasse (cimwin32-WMI-Anbieter)

Die **CIM- \_ Einstellungs** Klasse stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar. Einem verwalteten System Element können mehrere Einstellungs Objekte zugeordnet werden. Die aktuellen Betriebswerte für die Parameter eines Elements werden durch Eigenschaften im-Element selbst oder durch Eigenschaften in seinen Zuordnungen reflektiert. Diese Eigenschaften müssen nicht mit den Werten übereinstimmen, die im Einstellungs Objekt vorhanden sind. Beispielsweise kann ein Modem eine Einstellungs Baudrate von 56 Kilobyte pro Sekunde aufweisen, aber mit 19,2 Kilobyte pro Sekunde.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Einstellungs** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Einstellungs** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die von **CIM- \_ Einstellungen** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

