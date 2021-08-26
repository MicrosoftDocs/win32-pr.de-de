---
description: Stellt ein Gerät dar, das Medien zum Speichern und Abrufen von Daten verwenden kann.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: CIM_MediaAccessDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bb97ded03cfc853fc0dde6ede26083be01cf218f210c31f947f315634599e179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900260"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>CIM_MediaAccessDevice-Klasse (Hyper-V-Verwaltung)

Stellt ein Gerät dar, das Medien zum Speichern und Abrufen von Daten verwenden kann.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>Member

Die **CIM \_ MediaAccessDevice-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ MediaAccessDevice-Klasse** verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | Sperrt und entsperrt Wechselmedien auf einem Medienzugriffsgerät.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ MediaAccessDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Storage Devices \| 001.9", "MIF. DMTF \| Storage Devices \| 001.11", "MIF. DMTF \| Storage Geräte \| 001.12", "MIF. DMTF \| Disks \| 003.7", "MIF. \|DMTF-Hostdatenträger \| 001.2", "MIF. \|DMTF-Hostdatenträger \| 001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")
</dt> </dl>

Ein Array, das die Funktionen des Medienzugriffsgeräts enthält.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Sequenzieller Zugriff** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Zufälliger Zugriff** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Unterstützt das Schreiben** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Verschlüsselung** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Komprimierung** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Unterstützt entfernbare Medien** (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Manuelle Bereinigung** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Automatische Bereinigung** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**SMART-Benachrichtigung** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Unterstützt doppelseitige Medien** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Predismount Eject Not Required (12) (Bereitstellung vorab** aufheben nicht erforderlich (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funktionen**")
</dt> </dl>

Ein Array von Featurebeschreibungen für die Elemente im **Capabilities-Array.**

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Algorithmus oder Tools, der vom Gerät zur Unterstützung der Komprimierung verwendet wird.

Wenn kein Komprimierungstyp angegeben ist, kann einer der folgenden Werte verwendet werden:

-   Die Komprimierungsunterstützung "Unbekannt" ist unbekannt oder nicht angegeben.
-   Die komprimierte Komprimierung wird unterstützt, aber der Typ ist unbekannt oder nicht angegeben.
-   "Nicht komprimiert" unterstützt das Gerät keine Komprimierungsfunktionen.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("Byte")
</dt> </dl>

Die Standardblockgröße für das Gerät in Bytes.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der vom Gerät unterstützten Fehlererkennung und -korrektur.

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der letzten Bereinigung des Geräts.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")
</dt> </dl>

Die Zeit in Millisekunden, die das Gerät benötigt, um ein Medium lesen oder schreiben zu können, nachdem das Gerät mit dem Laden begonnen hat. Bei Datenträgerlaufwerken ist dies z. B. das Intervall zwischen einem Datenträger, der nicht auf den Datenträger rotiert und meldet, dass er für Lese-/Schreibvorgänge bereit ist. Bei Bandlaufwerken beginnt dies, wenn Medien eingefügt werden, und endet, wenn das Laufwerk meldet, dass es für eine Anwendung bereit ist. Dies befindet sich in der Regel am Bandanfangsbereich (BOT).

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")
</dt> </dl>

Die maximale Zugriffszeit des Mediums in Millisekunden. Für ein Laufwerk stellt dies vollständige Such- und vollständige Rotationsverzögerung dar. Bei Bandlaufwerken stellt dies eine Suche vom Anfang des Bands bis zum physisch entferntesten Punkt dar.

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("Byte")
</dt> </dl>

Die maximale Blockgröße (in Bytes) für Medien, auf die vom Gerät zugegriffen wird.

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Sequential Access Devices \| 001.2", "MIF. \|DMTF-Hostdatenträger \| 001.5")
</dt> </dl>

Die maximale Größe von Medien in Kilobytes, die von diesem Gerät unterstützt werden.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")
</dt> </dl>

Die maximale Anzahl von Einheiten, die verwendet werden können, bevor das Gerät bereinigt werden soll. **UnitsDescription** definiert, wie der Einheitentyp ist.

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn das Medium auf dem Gerät gesperrt ist und nicht eingefügt werden kann; andernfalls **FALSE.** Für Nicht-Wechselmedien sollte dieser Wert **true** sein.

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")
</dt> </dl>

Die minimale Blockgröße in Byte für Medien, auf die vom Gerät zugegriffen wird.

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Counter**
</dt> </dl>

Gibt an, wie oft Medien für die Datenübertragung oder zum Bereinigten des Geräts bereitgestellt wurden. Wenn das Gerät keine Wechselmedien unterstützt, sollte diese Eigenschaft auf 0 (null) festgelegt werden.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn das Gerät bereinigen muss; andernfalls **FALSE.**

> [!Note]  
> Die **Capabilities-Eigenschaft** gibt an, ob eine manuelle oder automatische Bereinigung möglich ist.

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn das Gerät mehrere einzelne Medien unterstützt, definiert diese Eigenschaft die maximale Anzahl, die unterstützt oder eingefügt werden kann.

</dd> <dt>

**Sicherheit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Disks \| 003.22")
</dt> </dl>

Die Betriebssicherheit für das Gerät.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (3)


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**Schreibgeschützt** (4)


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Gesperrt** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Startumgehung** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Startumgehung und Schreibgeschützt** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Medieneinrichtung auf dem Gerät. Diese Eigenschaft wird nur von Geräten verwendet, die Wechselmedien unterstützen.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit in Sekunden, die das Medium für die Datenübertragung oder zum Bereinigten des Geräts bereitgestellt wurde. Wenn das Gerät keine Wechselmedien unterstützt, sollte diese Eigenschaft auf 0 (null) festgelegt werden.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes pro Sekunde"), **PUnit** ("byte/second \* 10^3")
</dt> </dl>

Die dauerhafte Datenübertragungsrate in Kilobyte, mit der das Gerät ein Medium lesen und auf dieses schreiben kann. Dies ist eine dauerhafte Rohdatenrate. Maximale Raten oder Raten mit Komprimierung sollten in dieser Eigenschaft nicht gemeldet werden.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM \_ MediaAccessDevice**.**UnitsUsed**")
</dt> </dl>

Beschreibt den Einheitentyp der **Eigenschaften MaxUnitsBeforeCleaning und** **UnitsUsed.**

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**", "**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")
</dt> </dl>

Die Anzahl der vom Gerät verwendeten Einheiten. Diese Eigenschaft wird verwendet, um zu bestimmen, wann das Gerät bereinigt werden soll. **UnitsDescription definiert,** wie der Einheitentyp ist.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **PUnit** ("second \* 10^-3")
</dt> </dl>

Die Zeit in Millisekunden, die das Gerät benötigt, um vom Lesen oder Schreiben von Medien zum Entladen zu überschreiben. Bei Laufwerken ist dies beispielsweise das Intervall zwischen einem Datenträger, der sich mit nominaler Geschwindigkeit dreht, und einem Datenträger, der sich nicht dreht. Bei Bandlaufwerken ist dies die Zeit, in der ein Medium vom BOT bis zur vollständigen Ausdringung und zum Zugriff auf ein Auswahlelement oder einen menschlichen Bediener wechseln kann.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

