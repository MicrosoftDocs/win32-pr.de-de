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
# <a name="sense_data-structure"></a><span data-ttu-id="b7d23-103">Sense- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="b7d23-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="b7d23-104">Wird verwendet, um Status-oder Fehlerinformationen als Reaktion auf einen SCSI- **Anforderungs Sense** -Befehl zu melden.</span><span class="sxs-lookup"><span data-stu-id="b7d23-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7d23-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="b7d23-106">Member</span><span class="sxs-lookup"><span data-stu-id="b7d23-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7d23-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b7d23-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-108">Der Berichtstyp.</span><span class="sxs-lookup"><span data-stu-id="b7d23-108">The report type.</span></span>



| <span data-ttu-id="b7d23-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d23-109">Value</span></span>                                                                           | <span data-ttu-id="b7d23-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b7d23-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="b7d23-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="b7d23-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="b7d23-112">Aktuelle Fehler.</span><span class="sxs-lookup"><span data-stu-id="b7d23-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="b7d23-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="b7d23-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="b7d23-114">Verzögerte Fehler.</span><span class="sxs-lookup"><span data-stu-id="b7d23-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b7d23-115">**Gültig**</span><span class="sxs-lookup"><span data-stu-id="b7d23-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-116">1, wenn das **Informations** Feld in einem Standard definiert ist. Andernfalls ist das **Informations** Feld Hersteller spezifisch und nicht durch einen Standard definiert.</span><span class="sxs-lookup"><span data-stu-id="b7d23-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-117">**Segmentnumber**</span><span class="sxs-lookup"><span data-stu-id="b7d23-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-118">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b7d23-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-119">**Senabkey**</span><span class="sxs-lookup"><span data-stu-id="b7d23-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-120">Gibt die Kategorie des Fehlers an.</span><span class="sxs-lookup"><span data-stu-id="b7d23-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="b7d23-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Keine Sense** (0x0)</span><span class="sxs-lookup"><span data-stu-id="b7d23-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>Wiederherstellungs **Fehler** (0x1)</span><span class="sxs-lookup"><span data-stu-id="b7d23-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (0x2)</span><span class="sxs-lookup"><span data-stu-id="b7d23-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Mittlerer Fehler** (0x3)</span><span class="sxs-lookup"><span data-stu-id="b7d23-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Fehler** (0x4)</span><span class="sxs-lookup"><span data-stu-id="b7d23-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>Ungültige **Anforderung** (0x5)</span><span class="sxs-lookup"><span data-stu-id="b7d23-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Einheiten Aufmerksamkeit** (0x6)</span><span class="sxs-lookup"><span data-stu-id="b7d23-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Datenschutz** (0x7)</span><span class="sxs-lookup"><span data-stu-id="b7d23-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmwarefehler** (0x9)</span><span class="sxs-lookup"><span data-stu-id="b7d23-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Abgebrochener Befehl** (0xB)</span><span class="sxs-lookup"><span data-stu-id="b7d23-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Gleich** (0xc)</span><span class="sxs-lookup"><span data-stu-id="b7d23-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volumeüberlauf** (0xD)</span><span class="sxs-lookup"><span data-stu-id="b7d23-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="b7d23-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Falsch vergleichen** (0xe)</span><span class="sxs-lookup"><span data-stu-id="b7d23-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d23-134">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b7d23-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-135">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b7d23-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-136">**Incorrectlength**</span><span class="sxs-lookup"><span data-stu-id="b7d23-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-137">1, wenn die angeforderte logische Blocklänge nicht mit der logischen Blocklänge der Daten auf dem Medium identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b7d23-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-138">**EndOf-Medien**</span><span class="sxs-lookup"><span data-stu-id="b7d23-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-139">1, wenn ein sequenzielles Zugriffsgerät das Ende des Mediums erreicht hat, oder ein Drucker nicht mehr in Papierform.</span><span class="sxs-lookup"><span data-stu-id="b7d23-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-140">**Datei Markierung**</span><span class="sxs-lookup"><span data-stu-id="b7d23-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-141">1, wenn der aktuelle Befehl eine Datei Markierung oder ein setmark erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="b7d23-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="b7d23-142">Nur für sequenzielle Zugriffsgeräte gültig.</span><span class="sxs-lookup"><span data-stu-id="b7d23-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-143">**Information**</span><span class="sxs-lookup"><span data-stu-id="b7d23-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-144">Gerätetyp-oder Befehls spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="b7d23-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-145">**Additionalsenselength**</span><span class="sxs-lookup"><span data-stu-id="b7d23-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-146">Die Länge der restlichen Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b7d23-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="b7d23-147">Die Gesamtlänge minus 7.</span><span class="sxs-lookup"><span data-stu-id="b7d23-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-148">**Commandspecificinformation**</span><span class="sxs-lookup"><span data-stu-id="b7d23-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-149">Befehls spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="b7d23-149">Command-specific data.</span></span> <span data-ttu-id="b7d23-150">Werte werden im entsprechenden Befehls Standard definiert.</span><span class="sxs-lookup"><span data-stu-id="b7d23-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-151">**Additionalsensecode**</span><span class="sxs-lookup"><span data-stu-id="b7d23-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-152">Geräte spezifischer Code, der den im Feld " **sensekey** " gemeldeten Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b7d23-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-153">**Additionalsenmencodequalifizierer**</span><span class="sxs-lookup"><span data-stu-id="b7d23-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-154">Kann weitere Details über das **additionalsensecode** -Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7d23-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-155">**Fieldreplaceableunitcode**</span><span class="sxs-lookup"><span data-stu-id="b7d23-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-156">Vender-spezifische Informationen zu der Komponente, die diesen Sense-Daten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b7d23-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="b7d23-157">**Senabkeyspecific**</span><span class="sxs-lookup"><span data-stu-id="b7d23-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="b7d23-158">Der Inhalt und das Format der spezifischen Informationen des Sense-Schlüssels werden durch den Wert des **sentskey** -Felds bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b7d23-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7d23-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7d23-159">Remarks</span></span>

<span data-ttu-id="b7d23-160">Weitere Informationen zum Sense-Datenformat finden Sie unter [SCSI Request Sense-Befehl](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .</span><span class="sxs-lookup"><span data-stu-id="b7d23-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d23-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7d23-161">Requirements</span></span>



| <span data-ttu-id="b7d23-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7d23-162">Requirement</span></span> | <span data-ttu-id="b7d23-163">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d23-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b7d23-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7d23-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d23-165">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7d23-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b7d23-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7d23-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d23-167">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7d23-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b7d23-168">Header</span><span class="sxs-lookup"><span data-stu-id="b7d23-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d23-169"><dt>SCSI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d23-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d23-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d23-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d23-171">iSCSI-Ziel-Pass-Through</span><span class="sxs-lookup"><span data-stu-id="b7d23-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="b7d23-172">SCSI \_ - \_ Durchlauf \_ direkt</span><span class="sxs-lookup"><span data-stu-id="b7d23-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




