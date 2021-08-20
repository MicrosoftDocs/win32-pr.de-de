---
description: Wird verwendet, um Status- oder Fehlerinformationen als Reaktion auf einen SCSI Request Sense-Befehl zu melden.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: SENSE_DATA-Struktur (Scsi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: 2f6b3bd9fd4353e396bc7fe4ff7273e598704d1348062fec1c2f64aed9380686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075953"
---
# <a name="sense_data-structure"></a>SENSE \_ DATA-Struktur

Wird verwendet, um Status- oder Fehlerinformationen als Reaktion auf einen SCSI Request **Sense-Befehl** zu melden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ErrorCode**
</dt> <dd>

Der Berichtstyp.



| Wert                                                                           | Bedeutung                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | Aktuelle Fehler.<br/>  |
| <dl> <dt>0x71</dt> </dl> | Verzögerte Fehler.<br/> |



 

</dd> <dt>

**Gültig**
</dt> <dd>

1, wenn das Feld **Information** in einem Standard definiert ist; Andernfalls ist das Feld **Information** herstellerspezifisch und nicht durch einen Standard definiert.

</dd> <dt>

**SegmentNumber**
</dt> <dd>

Veraltet.

</dd> <dt>

**SenseKey**
</dt> <dd>

Gibt die Kategorie des Fehlers an.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Wiederhergestellter Fehler** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (0x2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Mittlerer Fehler** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardwarefehler** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Ungültige Anforderung** (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmwarefehler** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Abgebrochener Befehl** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Gleich** (0xC)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volumeüberlauf** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Fehlkomparierung** (0xE)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1, wenn die angeforderte länge des logischen Blocks nicht mit der Länge des logischen Blocks der Daten auf dem Medium übereinstimmt.

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1, wenn ein Gerät mit sequenziellem Zugriff das Medienende erreicht hat oder ein Drucker nicht aus papieriert ist.

</dd> <dt>

**FileMark**
</dt> <dd>

1, wenn der aktuelle Befehl ein Dateizeichen oder ein Setmark erreicht hat. Nur für Geräte mit sequenziellem Zugriff gültig.

</dd> <dt>

**Information**
</dt> <dd>

Gerätetyp- oder befehlsspezifische Daten.

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

Die Länge des Rests der Struktur in Bytes. Die Gesamtlänge minus 7.

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

Befehlsspezifische Daten. Werte werden im entsprechenden Befehlsstandard definiert.

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

Gerätespezifischer Code, der den im **Feld SenseKey** gemeldeten Fehler beschreibt.

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

Kann zusätzliche Details zum Feld **AdditionalSenseCode** enthalten.

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

Automatenspezifische Informationen über die Komponente, die diesen Sinndaten zugeordnet ist.

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

Inhalt und Format der für den Sinnschlüssel spezifischen Informationen werden durch den Wert des **SenseKey-Felds** bestimmt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Format der Sinndaten finden Sie unter [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Scsi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[iSCSI-Zielpass-Through](/powershell/module/iscsi)
</dt> <dt>

[\_SCSI-PASS-THROUGH \_ \_ DIRECT](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




