---
description: Wird verwendet, um Status-oder Fehlerinformationen als Reaktion auf einen SCSI-Anforderungs Sense-Befehl zu melden.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: SENSE_DATA Struktur (SCSI. h)
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
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106361781"
---
# <a name="sense_data-structure"></a>Sense- \_ Datenstruktur

Wird verwendet, um Status-oder Fehlerinformationen als Reaktion auf einen SCSI- **Anforderungs Sense** -Befehl zu melden.

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

1, wenn das **Informations** Feld in einem Standard definiert ist. Andernfalls ist das **Informations** Feld Hersteller spezifisch und nicht durch einen Standard definiert.

</dd> <dt>

**Segmentnumber**
</dt> <dd>

Veraltet.

</dd> <dt>

**Senabkey**
</dt> <dd>

Gibt die Kategorie des Fehlers an.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Keine Sense** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>Wiederherstellungs **Fehler** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (0x2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Mittlerer Fehler** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Fehler** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>Ungültige **Anforderung** (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Einheiten Aufmerksamkeit** (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Datenschutz** (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmwarefehler** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Abgebrochener Befehl** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Gleich** (0xc)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volumeüberlauf** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Falsch vergleichen** (0xe)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Incorrectlength**
</dt> <dd>

1, wenn die angeforderte logische Blocklänge nicht mit der logischen Blocklänge der Daten auf dem Medium identisch ist.

</dd> <dt>

**EndOf-Medien**
</dt> <dd>

1, wenn ein sequenzielles Zugriffsgerät das Ende des Mediums erreicht hat, oder ein Drucker nicht mehr in Papierform.

</dd> <dt>

**Datei Markierung**
</dt> <dd>

1, wenn der aktuelle Befehl eine Datei Markierung oder ein setmark erreicht hat. Nur für sequenzielle Zugriffsgeräte gültig.

</dd> <dt>

**Information**
</dt> <dd>

Gerätetyp-oder Befehls spezifische Daten.

</dd> <dt>

**Additionalsenselength**
</dt> <dd>

Die Länge der restlichen Struktur in Bytes. Die Gesamtlänge minus 7.

</dd> <dt>

**Commandspecificinformation**
</dt> <dd>

Befehls spezifische Daten. Werte werden im entsprechenden Befehls Standard definiert.

</dd> <dt>

**Additionalsensecode**
</dt> <dd>

Geräte spezifischer Code, der den im Feld " **sensekey** " gemeldeten Fehler beschreibt.

</dd> <dt>

**Additionalsenmencodequalifizierer**
</dt> <dd>

Kann weitere Details über das **additionalsensecode** -Feld enthalten.

</dd> <dt>

**Fieldreplaceableunitcode**
</dt> <dd>

Vender-spezifische Informationen zu der Komponente, die diesen Sense-Daten zugeordnet ist.

</dd> <dt>

**Senabkeyspecific**
</dt> <dd>

Der Inhalt und das Format der spezifischen Informationen des Sense-Schlüssels werden durch den Wert des **sentskey** -Felds bestimmt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Sense-Datenformat finden Sie unter [SCSI Request Sense-Befehl](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>SCSI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[iSCSI-Ziel-Pass-Through](/powershell/module/iscsi)
</dt> <dt>

[SCSI \_ - \_ Durchlauf \_ direkt](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




