---
title: WINBIO_BIR_HEADER Struktur (winbio \_ types. h)
description: Enthält den Header eines biometrischen Informationsdaten Satzes (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103700"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="106f8-104">Winbio-Struktur mit dem \_ \_ Header</span><span class="sxs-lookup"><span data-stu-id="106f8-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="106f8-105">Die Struktur des winbio-Struktur- **\_ \_ Headers** enthält den Header eines biometrischen Informationsdaten Satzes (BIR).</span><span class="sxs-lookup"><span data-stu-id="106f8-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="106f8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="106f8-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="106f8-107">Member</span><span class="sxs-lookup"><span data-stu-id="106f8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="106f8-108">**Validfields**</span><span class="sxs-lookup"><span data-stu-id="106f8-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-109">Bitmaske, die angibt, welche Felder in dieser Struktur gültig sind.</span><span class="sxs-lookup"><span data-stu-id="106f8-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="106f8-110">Weitere Informationen finden Sie unter [**winbio \_ - \_ Feld Konstanten**](winbio-bir-field-constants.md).</span><span class="sxs-lookup"><span data-stu-id="106f8-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="106f8-111">**Header Version**</span><span class="sxs-lookup"><span data-stu-id="106f8-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-112">Eine **winbio \_ - \_ Version der Version** , die die Header Version angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="106f8-113">Versionsnummern sind 8-Bit-Werte, bei denen die oberen vier Bits die Haupt Zahl angeben und die unteren vier Bits die neben Versionsnummer angeben.</span><span class="sxs-lookup"><span data-stu-id="106f8-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="106f8-114">Derzeit muss es sich um eine winbio \_ CBEFF- \_ Header \_ Version (0x11) handeln.</span><span class="sxs-lookup"><span data-stu-id="106f8-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="106f8-115">**Patronheaderversion**</span><span class="sxs-lookup"><span data-stu-id="106f8-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-116">Eine **winbio \_ - \_ Version der Version** , die die Header Version angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="106f8-117">Versionsnummern sind 8-Bit-Werte, bei denen die oberen vier Bits die Haupt Zahl angeben und die unteren vier Bits die neben Versionsnummer angeben.</span><span class="sxs-lookup"><span data-stu-id="106f8-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="106f8-118">Derzeit muss es sich um eine winbio- \_ Patron- \_ Header \_ Version (0x11) handeln.</span><span class="sxs-lookup"><span data-stu-id="106f8-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="106f8-119">**Dataflags**</span><span class="sxs-lookup"><span data-stu-id="106f8-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-120">Ein-Wert, der das Format der Header Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="106f8-121">Hierbei kann es sich um ein bitweises **or** der folgenden Flags für Sicherheit und Verarbeitungs Ebene handeln.</span><span class="sxs-lookup"><span data-stu-id="106f8-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="106f8-122">Weitere Informationen finden Sie unter [**winbio \_ - \_ \_ datenflags-Konstanten**](winbio-bir-data-flags-constants.md).</span><span class="sxs-lookup"><span data-stu-id="106f8-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="106f8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="106f8-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="106f8-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="106f8-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="106f8-125"><dt>**Winbio \_ Datenflag-Daten \_ \_ Schutz**</dt> <dt>((UCHAR) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="106f8-126">Die Daten sind verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="106f8-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="106f8-127"><dt>**Winbio \_ Datenflag- \_ \_ Integrität**</dt> <dt>((UCHAR) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="106f8-128">Die Daten werden mit einem Nachrichten Authentifizierungscode (Message Authentication Code, Mac) digital signiert oder geschützt.</span><span class="sxs-lookup"><span data-stu-id="106f8-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="106f8-129"><dt>**Winbio \_ \_Datenflag \_ signiert**</dt> <dt>((UCHAR) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="106f8-130">Wenn dieses Flag und das **integritätsflag für die winbio- \_ \_ datenflag \_** festgelegt sind, werden die Daten signiert.</span><span class="sxs-lookup"><span data-stu-id="106f8-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="106f8-131">Wenn dieses Flag nicht festgelegt ist, aber das integritätsflag der **winbio- \_ \_ \_ datenflag** festgelegt ist, wird ein Mac für die Daten berechnet.</span><span class="sxs-lookup"><span data-stu-id="106f8-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="106f8-132"><dt>**Winbio \_ Data \_ Flag \_ RAW**</dt> <dt>((UCHAR) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="106f8-133">Die Daten haben das Format, in dem Sie aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="106f8-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="106f8-134"><dt>**Winbio \_ \_Datenflag \_ zwischen**</dt> <dt>((UCHAR) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="106f8-135">Die Daten sind nicht RAW, aber wurden nicht vollständig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="106f8-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="106f8-136"><dt>**Winbio \_ \_Datenflag \_ verarbeitet**</dt> <dt>((UCHAR) 0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="106f8-137">Die Daten wurden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="106f8-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="106f8-138"><dt>**Winbio \_ Data \_ Flag- \_ options \_ Maske \_ vorhanden**</dt> <dt>((UCHAR) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="106f8-139">Dieser Wert ist immer 1.</span><span class="sxs-lookup"><span data-stu-id="106f8-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="106f8-140">**Type**</span><span class="sxs-lookup"><span data-stu-id="106f8-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-141">Ein Wert vom Typ "winbio- \_ biometrischer \_ Typ", der den Typ der biometrischen Daten angibt, auf die im biometrischen Informations</span><span class="sxs-lookup"><span data-stu-id="106f8-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="106f8-142">Zurzeit wird nur der **winbio- \_ \_ typfingerabdruck** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="106f8-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="106f8-143">Weitere Informationen finden Sie unter [**winbio- \_ biometrische \_ Typkonstanten**](winbio-biometric-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="106f8-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="106f8-144">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="106f8-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-145">Ein-Wert des **Typs "winbio \_ biometrische \_ SubType** ", der den dem biometrischen Daten zugeordneten unter Faktor angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="106f8-146">Weitere Informationen finden Sie unter Hinweise und [**\_ biometrische \_ subtypkonstanten von winbio**](winbio-biometric-subtype-constants.md).</span><span class="sxs-lookup"><span data-stu-id="106f8-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="106f8-147">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="106f8-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-148">Eine **winbio \_ - \_ zwecks-zwecks** -Maske, die die beabsichtigte Verwendung der Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="106f8-149">Hierbei kann es sich um einen bitweisen **or** -Operator der folgenden Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="106f8-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="106f8-150">Weitere Informationen finden Sie unter [**winbio-und- \_ Zweck- \_ Konstanten**](winbio-bir-purpose-constants.md).</span><span class="sxs-lookup"><span data-stu-id="106f8-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="106f8-151">Überprüfung von winbio- \_ Zwecken \_</span><span class="sxs-lookup"><span data-stu-id="106f8-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="106f8-152">Zweck der winbio- \_ \_ Identifizierung</span><span class="sxs-lookup"><span data-stu-id="106f8-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="106f8-153">winbio- \_ Aufgabe \_ registrieren</span><span class="sxs-lookup"><span data-stu-id="106f8-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="106f8-154">winbio- \_ Zweck \_ für die \_ über \_ Prüfung</span><span class="sxs-lookup"><span data-stu-id="106f8-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="106f8-155">winbio- \_ Zweck \_ \_ zur \_ Identifizierung registrieren</span><span class="sxs-lookup"><span data-stu-id="106f8-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="106f8-156">Überprüfung von winbio- \_ Zwecken \_</span><span class="sxs-lookup"><span data-stu-id="106f8-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="106f8-157">**Dataquality**</span><span class="sxs-lookup"><span data-stu-id="106f8-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-158">Ein-Wert, der die relative Qualität der biometrischen Daten im biometrischen Informationsdaten Satz (BIR) angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="106f8-159">Dies kann eine ganze Zahl zwischen 0 und 100 oder einem der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="106f8-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="106f8-160">Weitere Informationen finden Sie unter [**winbio \_ - \_ Qualitäts Konstanten**](winbio-bir-quality-constants.md).</span><span class="sxs-lookup"><span data-stu-id="106f8-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="106f8-161">Wert</span><span class="sxs-lookup"><span data-stu-id="106f8-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="106f8-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="106f8-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="106f8-163"><dt>**Winbio \_ Data \_ Quality \_ nicht \_ festgelegt**</dt> <dt>((winbio- \_ \_ Qualität)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="106f8-164">Qualitätsmessungen werden vom BIR-Ersteller unterstützt, aber im Bir ist kein Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="106f8-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="106f8-165"><dt>**Winbio \_ Data \_ Quality \_ \_ wird nicht unterstützt**</dt> <dt>((winbio- \_ \_ Qualität)-2)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="106f8-166">Qualitätsmessungen werden vom BIR-Ersteller nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="106f8-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="106f8-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="106f8-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-168">Das Datum und die Uhrzeit in koordinierter Weltzeit (Greenwich Mean Time), dass der BIR erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="106f8-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="106f8-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="106f8-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-170">Der Zeitraum, für den der BIR gültig ist.</span><span class="sxs-lookup"><span data-stu-id="106f8-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="106f8-171">**Begindate**</span><span class="sxs-lookup"><span data-stu-id="106f8-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-172">Das Datum und die Uhrzeit, in koordinierter Weltzeit, dass die Gültigkeitsdauer beginnt.</span><span class="sxs-lookup"><span data-stu-id="106f8-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="106f8-173">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="106f8-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-174">Das Datum und die Uhrzeit in koordinierter Weltzeit, bei der der BIR nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="106f8-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="106f8-175">**Biometricdataformat**</span><span class="sxs-lookup"><span data-stu-id="106f8-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-176">Eine [**winbio- \_ registrierte \_ Format**](winbio-registered-format.md) Struktur, die das Daten Format des Standarddaten Blocks in der [**winbio \_ -Struktur "winbio**](winbio-bir.md) ..." angibt.</span><span class="sxs-lookup"><span data-stu-id="106f8-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="106f8-177">Die Member des **winbio- \_ registrierten \_ Formats** dürfen nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="106f8-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="106f8-178">Sie können die folgenden Konstanten verwenden, um die Fehlerüberprüfung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="106f8-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="106f8-179">Wert</span><span class="sxs-lookup"><span data-stu-id="106f8-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="106f8-180">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="106f8-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="106f8-181"><dt>**Winbio \_ Kein \_ Format \_ Besitzer \_ verfügbar**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="106f8-182">Es wurde kein IBIA-zugewiesener (International biometrische Industry Association) zugewiesener Besitzer Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="106f8-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="106f8-183"><dt>**Winbio \_ Kein \_ \_ Formattyp \_ verfügbar**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="106f8-184">Es wurde kein Formattyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="106f8-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="106f8-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="106f8-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="106f8-186">Eine [**winbio- \_ registrierte \_ Format**](winbio-registered-format.md) Struktur, die die Produkt-ID der Komponente angibt, die den Standarddaten Block im Bir generiert hat.</span><span class="sxs-lookup"><span data-stu-id="106f8-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="106f8-187">Die Member des **winbio- \_ registrierten \_ Formats** können NULL sein.</span><span class="sxs-lookup"><span data-stu-id="106f8-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="106f8-188">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="106f8-188">Remarks</span></span>

<span data-ttu-id="106f8-189">Der *SubType* -Parameter gibt den untergeordneten Faktor an, der den biometrischen Daten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="106f8-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="106f8-190">Derzeit unterstützt die Windows-Biometrieframework (WBF) nur die Fingerabdruck Erfassung und verwendet die folgenden Konstanten, um untergeordnete Typinformationen darzustellen:</span><span class="sxs-lookup"><span data-stu-id="106f8-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="106f8-191">Winbio \_ ANSI \_ 381 Torys \_ \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="106f8-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="106f8-192">Winbio \_ ANSI \_ 381 \_ POS, \_ RH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="106f8-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="106f8-193">Winbio \_ ANSI \_ 381 POS-Zeige- \_ \_ \_ \_ Finger</span><span class="sxs-lookup"><span data-stu-id="106f8-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="106f8-194">Winbio \_ ANSI \_ 381 \_ Torpo- \_ \_ \_ Mittelfinger</span><span class="sxs-lookup"><span data-stu-id="106f8-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="106f8-195">Winbio \_ ANSI \_ 381 \_ POS, \_ RH- \_ Klingel \_ Finger</span><span class="sxs-lookup"><span data-stu-id="106f8-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="106f8-196">Winbio \_ ANSI \_ 381 Torys \_ \_ RH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="106f8-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="106f8-197">Winbio \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="106f8-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="106f8-198">Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ Index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="106f8-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="106f8-199">Winbio \_ ANSI \_ 381 \_ POS \_ - \_ Mittel \_ Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="106f8-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="106f8-200">Winbio \_ ANSI \_ 381 Torys LH- \_ \_ \_ Klingel \_ Finger</span><span class="sxs-lookup"><span data-stu-id="106f8-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="106f8-201">Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ wenig \_ Finger</span><span class="sxs-lookup"><span data-stu-id="106f8-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="106f8-202">Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern</span><span class="sxs-lookup"><span data-stu-id="106f8-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="106f8-203">Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern</span><span class="sxs-lookup"><span data-stu-id="106f8-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="106f8-204">Winbio \_ ANSI \_ 381 \_ POS \_ zwei \_ Daumen</span><span class="sxs-lookup"><span data-stu-id="106f8-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="106f8-205">Versuchen Sie nicht, den Wert zu überprüfen, der für den *SubType* -Parameterwert angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="106f8-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="106f8-206">Der Windows-Biometrie-Dienst überprüft den angegebenen Wert vor der Übergabe an Ihre Implementierung.</span><span class="sxs-lookup"><span data-stu-id="106f8-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="106f8-207">Wenn der Wert " **winbio \_ SubType \_ No \_ Information** " oder " **winbio \_ SubType \_ any**" lautet, überprüfen Sie ggf. ggf.</span><span class="sxs-lookup"><span data-stu-id="106f8-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="106f8-208">Wenn eine der folgenden Bits bestätigt wird, ist die Struktur des **winbio.- \_ \_ Headers** nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="106f8-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="106f8-209">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="106f8-209">Requirements</span></span>



| <span data-ttu-id="106f8-210">Anforderung</span><span class="sxs-lookup"><span data-stu-id="106f8-210">Requirement</span></span> | <span data-ttu-id="106f8-211">Wert</span><span class="sxs-lookup"><span data-stu-id="106f8-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="106f8-212">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="106f8-212">Minimum supported client</span></span><br/> | <span data-ttu-id="106f8-213">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="106f8-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="106f8-214">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="106f8-214">Minimum supported server</span></span><br/> | <span data-ttu-id="106f8-215">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="106f8-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="106f8-216">Header</span><span class="sxs-lookup"><span data-stu-id="106f8-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="106f8-217"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="106f8-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="106f8-218">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="106f8-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106f8-219">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="106f8-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="106f8-220">**Subtypkonstanten von winbio- \_ Biometrie \_**</span><span class="sxs-lookup"><span data-stu-id="106f8-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="106f8-221">**winbio \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="106f8-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="106f8-222">**Winbio \_ - \_ \_ datenflags-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="106f8-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="106f8-223">**Winbio \_ Bir- \_ Feld Konstanten**</span><span class="sxs-lookup"><span data-stu-id="106f8-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="106f8-224">**Winbio-und- \_ \_ Zweck-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="106f8-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="106f8-225">**Winbio \_ Bir- \_ Qualitäts Konstanten**</span><span class="sxs-lookup"><span data-stu-id="106f8-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="106f8-226">**Winbio \_ - \_ Version Version-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="106f8-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





