---
description: Die CIM \_ VideoControllerResolution-Klasse stellt die verschiedenen Videomodi dar, die ein Videocontroller unterstützen kann.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: CIM_VideoControllerResolution-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af943df981ca2043e83dfcdd3daade0a1c13b63222a163d7e6ecf1d6110396e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420377"
---
# <a name="cim_videocontrollerresolution-class"></a>CIM \_ VideoControllerResolution-Klasse

Die **CIM \_ VideoControllerResolution-Klasse** stellt die verschiedenen Videomodi dar, die ein Videocontroller unterstützen kann. Videomodi werden durch die möglichen horizontalen und vertikalen Auflösungen, die Aktualisierungsrate, den Scanmodus und die Anzahl der von einem Controller unterstützten Farbeinstellungen definiert. Die tatsächlich verwendeten Auflösungen sind die im [**CIM \_ VideoController-Objekt**](cim-videocontroller.md) angegebenen Werte.

Hardware, die nicht mit Windows Display Driver Model (WDDM) kompatibel ist, gibt ungenaue Eigenschaftswerte für Instanzen dieser Klasse zurück.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>Member

Die **CIM \_ VideoControllerResolution-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ VideoControllerResolution-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Monitorauflösungen \| 002.2"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")
</dt> </dl>

Horizontale Auflösung in Pixel.

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Monitorauflösungen \| 002.7"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Maximale Aktualisierungsrate, wenn ein Bereich von Raten mit den angegebenen Auflösungen in Hertz unterstützt wird.

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Monitorauflösungen \| 002.6"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Minimale Aktualisierungsrate, wenn ein Bereich von Raten mit den angegebenen Auflösungen in Hertz unterstützt wird.

</dd> <dt>

**NumberOfColors**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")
</dt> </dl>

Anzahl von Farben, die bei der aktuellen Auflösung unterstützt werden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Monitor-Auflösungen \| 002.4"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Aktualisierungsrate in Hertz. Wenn ein Tarifbereich unterstützt wird, verwenden Sie die Eigenschaften **MinRefreshRate** und **MaxRefreshRate,** und legen Sie diese Eigenschaft auf 0 fest.

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Monitor Resolution \| 002.5")
</dt> </dl>

Scanmodus, in dem der Controller ausgeführt wird.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Nicht geschachtelter Vorgang** (4)


</dt> <dd>

Nicht geschachtelter Vorgang

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced-Vorgang** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Eine ID, die als Teil des Schlüssels für die aktuelle Instanz dient.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Monitorauflösungen \| 002.3"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")
</dt> </dl>

Die vertikale Auflösung des Controllers in Pixel.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert die **CIM \_ VideoControllerResolution-Klasse.** Die **CIM \_ VideoControllerResolution-Klasse** ist eine dynamische Klasse.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

Beachten Sie, dass diese Klasse eine Basisklasse ist. Wenn Sie versuchen, über WMI auf Ihren Videocontroller zuzugreifen, können Sie stattdessen [**Win32 \_ VideoController**](win32-videocontroller.md) verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> </dl>

 

