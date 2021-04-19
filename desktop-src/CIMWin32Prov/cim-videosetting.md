---
description: Die CIM- \_ videosetting-Klasse ordnet das CIM \_ videocontrollerresolution-Einstellungs Objekt dem Controller zu, auf den es angewendet wird.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: CIM_VideoSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343200"
---
# <a name="cim_videosetting-class"></a>CIM- \_ videosetting-Klasse

Die **CIM- \_ videosetting** -Klasse ordnet das [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Einstellungs Objekt dem Controller zu, auf den es angewendet wird.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a>Member

Die **CIM- \_ videosetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ videosetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Videocontroller**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")
</dt> </dl>

Ein [**CIM- \_ Videocontroller**](cim-videocontroller.md) , der den Videocontroller beschreibt.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ videocontrollerresolution**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Setting")
</dt> </dl>

Eine [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) , in der die Auflösungen, Aktualisierungs Raten, der Überprüfungs Modus und die Anzahl der Farben beschrieben werden, die für den Controller festgelegt werden können.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die von **CIM \_ videosetting** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> </dl>

 

