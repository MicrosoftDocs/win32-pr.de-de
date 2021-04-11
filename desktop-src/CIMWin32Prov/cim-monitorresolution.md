---
description: Die CIM- \_ monitorresolution-Klasse stellt die Beziehung zwischen horizontaler und vertikaler Auflösung und der Aktualisierungsrate und dem Überprüfungs Modus für einen Desktop Monitor dar. Werte werden im Videocontroller Objekt angegeben.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: CIM_MonitorResolution-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958472"
---
# <a name="cim_monitorresolution-class"></a>CIM- \_ monitorresolution-Klasse

Die **CIM- \_ monitorresolution** -Klasse stellt die Beziehung zwischen horizontaler und vertikaler Auflösung und der Aktualisierungsrate und dem Überprüfungs Modus für einen Desktop Monitor dar. Werte werden im Videocontroller Objekt angegeben.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>Member

Die **CIM- \_ monitorresolution** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ monitorresolution** -Klasse verfügt über diese Eigenschaften.

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

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Happthorizontalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")
</dt> </dl>

Horizontale Auflösung des Monitors in Pixel.

</dd> <dt>

**Maxfreshshrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Maxaktushrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Die maximale Aktualisierungsrate des Monitors in Hertz, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird.

</dd> <dt>

**Minfreshshrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Minfreshshrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Die minimale Aktualisierungsrate des Monitors in Hertz, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird.

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**CurrentRefreshRate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Die Aktualisierungsrate des Monitors in Hertz. Wenn ein Bereich von Raten unterstützt wird, verwenden Sie die Eigenschaften **minaktushrate** und **maxfreshshrate** , und legen Sie diese Eigenschaft auf 0 fest.

</dd> <dt>

**Scanmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentscanmode**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,5 ")
</dt> </dl>

Der Scanmodus, den der Monitor verwendet.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Nicht unterstützt** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

**Nicht-Interlacing-Vorgang** (4)


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

Zeilen Sprung **Vorgang** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Dient als Teil des Schlüssels für die aktuelle-Instanz.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentverticalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")
</dt> </dl>

Vertikale Auflösung des Monitors in Pixel.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> </dl>

 

