---
title: WINBIO_BIR_HEADER -Struktur (Winbio \_ types.h)
description: Enthält den Header eines biometrischen Informationsdatensatz (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER Struktur Windows Biometrieframework-API
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
ms.openlocfilehash: d2166a206dd1590f83e16bc67482d3b42e24717efae4c44e54a99b9aa7d83b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911083"
---
# <a name="winbio_bir_header-structure"></a>WINBIO \_ BIR \_ HEADER-Struktur

Die **WINBIO \_ BIR \_ HEADER-Struktur** enthält den Header eines biometrischen Informationsdatensatzes (BIR).

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**ValidFields**
</dt> <dd>

Bitmaske, die angibt, welche Felder in dieser Struktur gültig sind. Weitere Informationen finden Sie unter [**WINBIO \_ BIR \_ FIELD-Konstanten**](winbio-bir-field-constants.md).

</dd> <dt>

**Header Version**
</dt> <dd>

Eine **WINBIO \_ BIR \_ VERSION-Konstante,** die die Headerversion angibt. Versionsnummern sind 8-Bit-Werte, bei denen die oberen vier Bits die Hauptzahl und die unteren vier Bits die Nebenversionsnummer angeben. Derzeit muss dies WINBIO \_ CBEFF \_ HEADER \_ VERSION (0x11) sein.

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Eine **WINBIO \_ BIR \_ VERSION-Konstante,** die die Headerversion angibt. Versionsnummern sind 8-Bit-Werte, bei denen die oberen vier Bits die Hauptzahl und die unteren vier Bits die Nebenversionsnummer angeben. Derzeit muss dies WINBIO \_ HEADER \_ VERSION \_ (0x11) sein.

</dd> <dt>

**DataFlags**
</dt> <dd>

Ein -Wert, der das Format der Headerdaten angibt. Dies kann ein **bitweises OR** der folgenden Sicherheits- und Verarbeitungsebenenflags sein. Weitere Informationen finden Sie unter [**WINBIO \_ BIR DATA \_ \_ FLAGS Constants**](winbio-bir-data-flags-constants.md).



| Wert                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ DATENSCHUTZ \_ FÜR \_ DATENFLAGS**</dt> <dt>((UCHAR)0x02)</dt> </dl>                                       | Die Daten sind verschlüsselt.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ DATENFLAGINTEGRITÄT**</dt> <dt>((UCHAR)0x01)</dt> </dl>                                 | Die Daten werden digital signiert oder durch einen Nachrichtenauthentifizierungscode (Message Authentication Code, MAC) geschützt.<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ \_ \_ DATENFLAG SIGNIERT**</dt> <dt>((UCHAR)0x04)</dt> </dl>                                          | Wenn dieses Flag und das **FLAG WINBIO \_ DATA FLAG \_ \_ INTEGRITY** festgelegt sind, werden die Daten signiert. Wenn dieses Flag nicht festgelegt ist, aber das **FLAG WINBIO \_ DATA FLAG \_ \_ INTEGRITY** festgelegt ist, wird ein MAC über die Daten berechnet.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ RAW**</dt> <dt>((UCHAR)0x20)</dt> </dl>                                                   | Die Daten haben das Format, mit dem sie erfasst wurden.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt> </dl>                        | Die Daten sind nicht unformatiert, wurden aber nicht vollständig verarbeitet.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ PROCESSED**</dt> <dt>((UCHAR)0x80)</dt> </dl>                                 | Die Daten wurden verarbeitet.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG OPTION MASK \_ \_ \_ PRESENT**</dt> <dt>((UCHAR)0x08)</dt> </dl> | Dieser Wert ist immer 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Typ**
</dt> <dd>

Ein WINBIO BIOMETRIC TYPE-Wert, der den Typ der biometrischen Daten angibt, \_ \_ auf die im biometrischen Informationsdatensatz verwiesen wird. Derzeit wird **nur WINBIO \_ TYPE \_ FINGERPRINT** unterstützt. Weitere Informationen finden Sie unter [**WINBIO \_ BIOMETRIC TYPE \_ Constants**](winbio-biometric-type-constants.md).

</dd> <dt>

**Untertyp**
</dt> <dd>

Ein **WINBIO \_ BIOMETRIC \_ SUBTYPE-Wert,** der den unteren Faktor angibt, der den biometrischen Daten zugeordnet ist. Weitere Informationen finden Sie unter Hinweise und [**WINBIO \_ BIOMETRIC \_ SUBTYPE Constants**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Zweck**
</dt> <dd>

Eine **WINBIO \_ BIR \_ PURPOSE-Maske,** die die beabsichtigte Verwendung der Daten angibt. Dies kann ein **bitweises OR** der folgenden Werte sein. Weitere Informationen finden Sie unter [**WINBIO \_ BIR PURPOSE \_ Constants**](winbio-bir-purpose-constants.md).

-   WINBIO \_ PURPOSE \_ VERIFY
-   WINBIO \_ PURPOSE \_ IDENTIFY
-   WINBIO \_ PURPOSE \_ ENROLL
-   WINBIO \_ PURPOSE \_ ENROLL \_ FOR \_ VERIFICATION
-   WINBIO \_ PURPOSE \_ ENROLL \_ FOR \_ IDENTIFICATION
-   \_WINBIO-ZWECKÜBERWACHUNG \_

</dd> <dt>

**DataQuality**
</dt> <dd>

Ein -Wert, der die relative Qualität der biometrischen Daten im biometrischen Informationsdatensatz (BIR) angibt. Dies kann eine ganze Zahl zwischen 0 und 100 oder einer der folgenden Werte sein. Weitere Informationen finden Sie unter [**WINBIO \_ BIR QUALITY \_ Constants**](winbio-bir-quality-constants.md).



| Wert                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ DATA \_ QUALITY \_ NOT \_ SET**</dt> <dt>((WINBIO \_ BIR \_ QUALITY)-1)</dt> </dl>                   | Qualitätsmessungen werden vom BIR-Ersteller unterstützt, aber in BIR ist kein Wert festgelegt.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ DATA \_ QUALITY \_ NOT \_ SUPPORTED**</dt> <dt>((WINBIO BIR QUALITY)-2) (NICHT UNTERSTÜTZTE DATENQUALITÄT ((WINBIO \_ BIR \_ QUALITY)-2))</dt> </dl> | Qualitätsmessungen werden vom BIR-Ersteller nicht unterstützt.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

Das Datum und die Uhrzeit in koordinierte Weltzeit (Greenwich Mean Time), zu der das BIR erstellt wurde.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Der Zeitraum, für den das BIR gültig ist.

<dl> <dt>

**BeginDate**
</dt> <dd>

Das Datum und die Uhrzeit in koordinierte Weltzeit, zu der die Gültigkeitsdauer beginnt.

</dd> <dt>

**EndDate**
</dt> <dd>

Das Datum und die Uhrzeit in koordinierte Weltzeit, ab dem das BIR nicht mehr gültig ist.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Eine [**WINBIO \_ REGISTERED \_ FORMAT-Struktur,**](winbio-registered-format.md) die das Datenformat des Standarddatenblocks in der [**WINBIO \_ BIR-Struktur**](winbio-bir.md) angibt. Die **WINBIO \_ REGISTERED \_ FORMAT-Member** dürfen nicht 0 (null) sein. Sie können die folgenden Konstanten verwenden, um die Fehlerüberprüfung zu vereinfachen.



| Wert                                                                                                                                                                                                                                                                                      | Bedeutung                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ KEIN \_ \_ FORMATBESITZER \_ VERFÜGBAR**</dt> <dt>((USHORT)0)</dt> </dl> | Es wurde kein IBIA-Besitzerwert (International Biometric Industry Association) angegeben.<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ KEIN \_ \_ FORMATTYP \_ VERFÜGBAR**</dt> <dt>((USHORT)0)</dt> </dl>    | Es wurde kein Formattyp angegeben.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Eine [**WINBIO \_ REGISTERED \_ FORMAT-Struktur,**](winbio-registered-format.md) die die Produkt-ID der Komponente angibt, die den Standarddatenblock im BIR generiert hat. Die **WINBIO \_ REGISTERED \_ FORMAT-Member** können 0 (null) sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der *Parameter Subtype* gibt den Unterfaktor an, der den biometrischen Daten zugeordnet ist. Derzeit unterstützt das Windows Biometric Framework (WBF) nur die Fingerabdruckerfassung und verwendet die folgenden Konstanten, um Untertypinformationen zu darstellen:

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LSFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LENK-ZEIGEFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LENK-MITTELFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LN-RINGFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS RH VIER \_ \_ \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS – VIER \_ \_ \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> Versuchen Sie nicht, den für den *Subtype-Parameterwert* angegebenen Wert zu überprüfen. Der Windows Biometrics Service überprüft den angegebenen Wert, bevor er an Ihre Implementierung übergeben wird. Wenn der Wert **WINBIO \_ SUBTYPE \_ NO \_ INFORMATION** oder **WINBIO \_ SUBTYPE \_ ANY** ist, überprüfen Sie ggf. .

 

Wenn eines der folgenden Bits bestätigt wird, wird die **WINBIO \_ BIR \_ HEADER-Struktur** nicht ordnungsgemäß gebildet.


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ BIOMETRIC \_ SUBTYPE Constants**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**WINBIO \_ BIR \_ DATA \_ FLAGS-Konstanten**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ FIELD-Konstanten**](winbio-bir-field-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ PURPOSE-Konstanten**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ QUALITY-Konstanten**](winbio-bir-quality-constants.md)
</dt> <dt>

[**WINBIO \_ \_ BIR-VERSIONSkonstanten**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





