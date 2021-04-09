---
description: Die CIM \_ videocontrollerresolution-Klasse stellt die verschiedenen Video Modi dar, die von einem Videocontroller unterstützt werden können.
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
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861683"
---
# <a name="cim_videocontrollerresolution-class"></a>CIM \_ videocontrollerresolution-Klasse

Die **CIM \_ videocontrollerresolution** -Klasse stellt die verschiedenen Video Modi dar, die von einem Videocontroller unterstützt werden können. Videomodi werden durch die möglichen horizontalen und vertikalen Auflösungen, die Aktualisierungsrate, den Überprüfungs Modus und die Anzahl der Farbeinstellungen definiert, die von einem Controller unterstützt werden. Die tatsächlich verwendeten Auflösungen sind die Werte, die im [**CIM \_ Videocontroller**](cim-videocontroller.md) -Objekt angegeben sind.

Hardware, die nicht mit dem Windows-Anzeigetreiber Modell (WDDM) kompatibel ist, gibt falsche Eigenschaftswerte für Instanzen dieser Klasse zurück.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ videocontrollerresolution** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ videocontrollerresolution** -Klasse verfügt über diese Eigenschaften.

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

Horizontale Auflösung in Pixel.

</dd> <dt>

**Maxfreshshrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Maxaktushrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Maximale Aktualisierungsrate, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird (in Hertz).

</dd> <dt>

**Minfreshshrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Minfreshshrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Minimale Aktualisierungsrate, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird (in Hertz).

</dd> <dt>

**Anzahl von Farben**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentzahlofcolors**")
</dt> </dl>

Anzahl von Farben, die bei der aktuellen Auflösung unterstützt werden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**CurrentRefreshRate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Aktualisierungsrate in Hertz. Wenn ein Bereich von Raten unterstützt wird, verwenden Sie die Eigenschaften **minaktushrate** und **maxfreshshrate** , und legen Sie diese Eigenschaft auf 0 fest.

</dd> <dt>

**Scanmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentscanmode**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,5 ")
</dt> </dl>

Scanmodus, in dem der Controller arbeitet.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Nicht-Interlacing-Vorgang** (4)


</dt> <dd>

Nicht Interlacing-Vorgang

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>Zeilen Sprung **Vorgang** (5)


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

Eine ID, die als Teil des Schlüssels für die aktuelle Instanz dient.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentverticalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")
</dt> </dl>

Vertikale Auflösung des Controllers in Pixel.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

WMI implementiert die **CIM \_ videocontrollerresolution** -Klasse. Die **CIM \_ videocontrollerresolution** -Klasse ist eine dynamische Klasse.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

Beachten Sie, dass diese Klasse eine Basisklasse ist. Wenn Sie über WMI auf Ihren Videocontroller zugreifen möchten, können Sie stattdessen [**Win32 \_ Videocontroller**](win32-videocontroller.md) verwenden.

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

 

