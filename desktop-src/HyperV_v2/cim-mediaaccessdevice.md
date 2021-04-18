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
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351195"
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

Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**Lockmedia**](cim-mediaaccessdevice-lockmedia.md) | Sperrt und entsperrt Wechselmedien in einem Medien Zugriffsgerät.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "," MIF. DMTF-Host Datenträger \| \| 001,2 "," MIF. DMTF-Host Datenträger \| \| 001,4 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Capabilitybeschreibungen**")
</dt> </dl>

Ein Array, das die Funktionen des Medien Zugriffs Geräts enthält.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Sequenzieller Zugriff** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Zufälliger Zugriff** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Unterstützt Schreib** Vorgänge (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Verschlüsselung** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Komprimierung** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Unterstützt Removeable Media** (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Manuelle Reinigung** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Automatische Bereinigung** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Smart Notification** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Unterstützt zweiseitige Medien** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Predismount-eject nicht erforderlich** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**Capabilitybeschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Funktionen**")
</dt> </dl>

Ein Array von Featurebeschreibungen für die Elemente im **Funktions Array.**

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Algorithmus oder Tools, der vom Gerät verwendet wird, um die Komprimierung zu unterstützen.

Wenn kein Komprimierungstyp angegeben ist, kann einer der folgenden Werte verwendet werden:

-   Die "unbekannte" Komprimierungs Unterstützung ist unbekannt oder nicht angegeben.
-   Komprimierte Komprimierung wird unterstützt, aber der Typ ist unbekannt oder nicht angegeben.
-   "Nicht komprimiert": das Gerät unterstützt keine Komprimierungs Funktionen.

</dd> <dt>

**Defaultblocksize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die Standard Blockgröße (in Bytes) für das Gerät.

</dd> <dt>

**Errormethodmethodologie**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Fehlererkennung und-Korrektur, der vom Gerät unterstützt wird.

</dd> <dt>

**Lastbereinigt**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Bereinigung des Geräts.

</dd> <dt>

**Loadtime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")
</dt> </dl>

Die Zeit in Millisekunden, die das Gerät zum Lesen oder Schreiben eines Mediums benötigt, nachdem das Gerät geladen wurde. Beispielsweise ist dies das Intervall für Laufwerke zwischen einem Datenträger, der nicht auf die Festplatte zeigt, dass er für Lese-/Schreibvorgänge bereit ist. Bei Bandlaufwerken beginnt dies, wenn Medien eingefügt werden und endet, wenn das Laufwerk meldet, dass es für eine Anwendung bereit ist. Dies erfolgt in der Regel am Anfang des Bands (bot).

</dd> <dt>

**Maxaccesstime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")
</dt> </dl>

Die maximale Zugriffszeit des Mediums in Millisekunden. Bei einem Laufwerk stellt dies eine vollständige Suche und eine vollständige Rotationsverzögerung dar. Bei Bandlaufwerken stellt dies eine Suche zwischen dem Anfang des Bands und dem physisch entfernten Punkt dar.

</dd> <dt>

**Maxblocksize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.

</dd> <dt>

**Maxmediasize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| sequenzieller Zugriffsgeräte \| 001,2 "," MIF. DMTF-Host Datenträger \| \| 001,5 ")
</dt> </dl>

Die maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.

</dd> <dt>

**Maxunitionbeforecforec**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Uni-Description**")
</dt> </dl>

Die maximale Anzahl von Einheiten, die verwendet werden können, bevor das Gerät bereinigt werden kann. **Unitdescription** definiert, wie der Typ der Einheit ist.

</dd> <dt>

**Mediaislocked**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn die Medien im Gerät gesperrt sind und nicht ausgewiesen werden können. andernfalls **false**. Bei nicht Wechsel Datenträgern sollte dieser Wert " **true**" lauten.

</dd> <dt>

**Minblocksize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.

</dd> <dt>

**Mountcount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Counter**
</dt> </dl>

Gibt an, wie oft Medien für die Datenübertragung bereitgestellt oder das Gerät bereinigt wurden. Wenn das Gerät Wechselmedien nicht unterstützt, sollte diese Eigenschaft auf 0 (null) festgelegt werden.

</dd> <dt>

**Unnötig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

" **true** ", wenn das Gerät bereinigt werden muss. andernfalls **false**.

> [!Note]  
> Mit der Eigenschaft **Funktionen** wird angegeben, ob eine manuelle oder automatische Bereinigung möglich ist.

 

</dd> <dt>

**"Numofmediasupportiert"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn das Gerät mehrere einzelne Medien unterstützt, definiert diese Eigenschaft die maximale Zahl, die unterstützt oder eingefügt werden kann.

</dd> <dt>

**Security**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF-Datenträger \| \| 003,22 ")
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

Schreib **geschützt (4** )


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Gesperrt** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Start Umgehung** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Start Umgehung und** schreibgeschützt (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Timeoflastmount**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das letzte Datum und die Uhrzeit, zu der die Medien auf dem Gerät bereitgestellt wurden. Diese Eigenschaft wird nur von Geräten verwendet, von denen Wechselmedien unterstützt werden.

</dd> <dt>

**Totalmounttime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit (in Sekunden), die für die Datenübertragung bereitgestellt wurde, oder zum Bereinigen des Geräts. Wenn das Gerät Wechselmedien nicht unterstützt, sollte diese Eigenschaft auf 0 (null) festgelegt werden.

</dd> <dt>

**Uncompresseddatarate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte pro Sekunde"), **Punit** ("Byte/Sekunde \* 10 ^ 3")
</dt> </dl>

Die dauerhafte Datenübertragungsrate in Kilobyte, bei der das Gerät Lese-und Schreibvorgänge für ein Medium durchführen kann. Dies ist eine dauerhafte, Rohdaten Rate. Die maximale Anzahl von Raten oder Raten mit Komprimierung sollte in dieser Eigenschaft nicht gemeldet werden.

</dd> <dt>

**Unitydescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Maxunitionbeforecforec"**,"**CIM \_ mediaaccessdevice**.**Unitsused**")
</dt> </dl>

Beschreibt den Einheitentyp der **maxunitbeforecforecund** **unitsused** -Eigenschaften.

</dd> <dt>

**Unitsused**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Unittdescription**","**CIM \_ mediaaccessdevice**.**Maxunitionbeforecforec"**)
</dt> </dl>

Die Anzahl der Einheiten, die vom Gerät verwendet werden. Diese Eigenschaft wird verwendet, um zu bestimmen, wann das Gerät bereinigt werden soll. **Unitdescription** definiert, wie der Typ der Einheit ist.

</dd> <dt>

**Unloadtime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")
</dt> </dl>

Die Zeit in Millisekunden, die das Gerät vom lesen oder Schreiben von Medien zum Entladen wechseln soll. Beispielsweise ist das Intervall für Datenträger Laufwerke das Intervall zwischen dem Drehen eines Datenträgers mit nominaler Geschwindigkeit und einem Datenträger, der nicht spinnt ist. Bei Bandlaufwerken ist dies der Zeitpunkt, an dem ein Medium von seinem bot zum vollständigen ausstehen und zum Zugriff auf ein Auswahl Element oder einen menschlichen Operator wechselt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

