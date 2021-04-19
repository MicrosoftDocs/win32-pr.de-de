---
description: Die CIM \_ -ElementSetting-Klasse stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: CIM_ElementSetting-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342600"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a>CIM_ElementSetting-Klasse (cimwin32-WMI-Anbieter)

Die **CIM- \_ ElementSetting** -Klasse stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a>Member

Die **CIM- \_ ElementSetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ ElementSetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die Rolle des [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekts der **CIM \_ Element Setting** -Zuordnung. Das zugeordnete verwaltete System Element stellt das Element bereit, das die-Element Einstellung implementiert.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die Rolle des [**CIM- \_ Einstellungs**](cim-setting.md) Objekts der **CIM- \_ ElementSetting** -Zuordnung. Die zugehörige Einstellung gibt die Einstellung an, die die-Element Einstellung implementiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu Klassen, die von **CIM \_ Element Setting** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




