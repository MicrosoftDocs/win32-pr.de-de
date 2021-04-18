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
# <a name="winbio_bir_header-structure"></a>Winbio-Struktur mit dem \_ \_ Header

Die Struktur des winbio-Struktur- **\_ \_ Headers** enthält den Header eines biometrischen Informationsdaten Satzes (BIR).

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

**Validfields**
</dt> <dd>

Bitmaske, die angibt, welche Felder in dieser Struktur gültig sind. Weitere Informationen finden Sie unter [**winbio \_ - \_ Feld Konstanten**](winbio-bir-field-constants.md).

</dd> <dt>

**Header Version**
</dt> <dd>

Eine **winbio \_ - \_ Version der Version** , die die Header Version angibt. Versionsnummern sind 8-Bit-Werte, bei denen die oberen vier Bits die Haupt Zahl angeben und die unteren vier Bits die neben Versionsnummer angeben. Derzeit muss es sich um eine winbio \_ CBEFF- \_ Header \_ Version (0x11) handeln.

</dd> <dt>

**Patronheaderversion**
</dt> <dd>

Eine **winbio \_ - \_ Version der Version** , die die Header Version angibt. Versionsnummern sind 8-Bit-Werte, bei denen die oberen vier Bits die Haupt Zahl angeben und die unteren vier Bits die neben Versionsnummer angeben. Derzeit muss es sich um eine winbio- \_ Patron- \_ Header \_ Version (0x11) handeln.

</dd> <dt>

**Dataflags**
</dt> <dd>

Ein-Wert, der das Format der Header Daten angibt. Hierbei kann es sich um ein bitweises **or** der folgenden Flags für Sicherheit und Verarbeitungs Ebene handeln. Weitere Informationen finden Sie unter [**winbio \_ - \_ \_ datenflags-Konstanten**](winbio-bir-data-flags-constants.md).



| Wert                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**Winbio \_ Datenflag-Daten \_ \_ Schutz**</dt> <dt>((UCHAR) 0x02)</dt> </dl>                                       | Die Daten sind verschlüsselt.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**Winbio \_ Datenflag- \_ \_ Integrität**</dt> <dt>((UCHAR) 0x01)</dt> </dl>                                 | Die Daten werden mit einem Nachrichten Authentifizierungscode (Message Authentication Code, Mac) digital signiert oder geschützt.<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**Winbio \_ \_Datenflag \_ signiert**</dt> <dt>((UCHAR) 0x04)</dt> </dl>                                          | Wenn dieses Flag und das **integritätsflag für die winbio- \_ \_ datenflag \_** festgelegt sind, werden die Daten signiert. Wenn dieses Flag nicht festgelegt ist, aber das integritätsflag der **winbio- \_ \_ \_ datenflag** festgelegt ist, wird ein Mac für die Daten berechnet.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**Winbio \_ Data \_ Flag \_ RAW**</dt> <dt>((UCHAR) 0x20)</dt> </dl>                                                   | Die Daten haben das Format, in dem Sie aufgezeichnet wurden.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**Winbio \_ \_Datenflag \_ zwischen**</dt> <dt>((UCHAR) 0x40)</dt> </dl>                        | Die Daten sind nicht RAW, aber wurden nicht vollständig verarbeitet.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**Winbio \_ \_Datenflag \_ verarbeitet**</dt> <dt>((UCHAR) 0x80)</dt> </dl>                                 | Die Daten wurden verarbeitet.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**Winbio \_ Data \_ Flag- \_ options \_ Maske \_ vorhanden**</dt> <dt>((UCHAR) 0x08)</dt> </dl> | Dieser Wert ist immer 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Type**
</dt> <dd>

Ein Wert vom Typ "winbio- \_ biometrischer \_ Typ", der den Typ der biometrischen Daten angibt, auf die im biometrischen Informations Zurzeit wird nur der **winbio- \_ \_ typfingerabdruck** unterstützt. Weitere Informationen finden Sie unter [**winbio- \_ biometrische \_ Typkonstanten**](winbio-biometric-type-constants.md).

</dd> <dt>

**Untertyp**
</dt> <dd>

Ein-Wert des **Typs "winbio \_ biometrische \_ SubType** ", der den dem biometrischen Daten zugeordneten unter Faktor angibt. Weitere Informationen finden Sie unter Hinweise und [**\_ biometrische \_ subtypkonstanten von winbio**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Zweck**
</dt> <dd>

Eine **winbio \_ - \_ zwecks-zwecks** -Maske, die die beabsichtigte Verwendung der Daten angibt. Hierbei kann es sich um einen bitweisen **or** -Operator der folgenden Werte handeln. Weitere Informationen finden Sie unter [**winbio-und- \_ Zweck- \_ Konstanten**](winbio-bir-purpose-constants.md).

-   Überprüfung von winbio- \_ Zwecken \_
-   Zweck der winbio- \_ \_ Identifizierung
-   winbio- \_ Aufgabe \_ registrieren
-   winbio- \_ Zweck \_ für die \_ über \_ Prüfung
-   winbio- \_ Zweck \_ \_ zur \_ Identifizierung registrieren
-   Überprüfung von winbio- \_ Zwecken \_

</dd> <dt>

**Dataquality**
</dt> <dd>

Ein-Wert, der die relative Qualität der biometrischen Daten im biometrischen Informationsdaten Satz (BIR) angibt. Dies kann eine ganze Zahl zwischen 0 und 100 oder einem der folgenden Werte sein. Weitere Informationen finden Sie unter [**winbio \_ - \_ Qualitäts Konstanten**](winbio-bir-quality-constants.md).



| Wert                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**Winbio \_ Data \_ Quality \_ nicht \_ festgelegt**</dt> <dt>((winbio- \_ \_ Qualität)-1)</dt> </dl>                   | Qualitätsmessungen werden vom BIR-Ersteller unterstützt, aber im Bir ist kein Wert festgelegt.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**Winbio \_ Data \_ Quality \_ \_ wird nicht unterstützt**</dt> <dt>((winbio- \_ \_ Qualität)-2)</dt> </dl> | Qualitätsmessungen werden vom BIR-Ersteller nicht unterstützt.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

Das Datum und die Uhrzeit in koordinierter Weltzeit (Greenwich Mean Time), dass der BIR erstellt wurde.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Der Zeitraum, für den der BIR gültig ist.

<dl> <dt>

**Begindate**
</dt> <dd>

Das Datum und die Uhrzeit, in koordinierter Weltzeit, dass die Gültigkeitsdauer beginnt.

</dd> <dt>

**EndDate**
</dt> <dd>

Das Datum und die Uhrzeit in koordinierter Weltzeit, bei der der BIR nicht mehr gültig ist.

</dd> </dl> </dd> <dt>

**Biometricdataformat**
</dt> <dd>

Eine [**winbio- \_ registrierte \_ Format**](winbio-registered-format.md) Struktur, die das Daten Format des Standarddaten Blocks in der [**winbio \_ -Struktur "winbio**](winbio-bir.md) ..." angibt. Die Member des **winbio- \_ registrierten \_ Formats** dürfen nicht NULL sein. Sie können die folgenden Konstanten verwenden, um die Fehlerüberprüfung zu vereinfachen.



| Wert                                                                                                                                                                                                                                                                                      | Bedeutung                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**Winbio \_ Kein \_ Format \_ Besitzer \_ verfügbar**</dt> <dt>((UShort) 0)</dt> </dl> | Es wurde kein IBIA-zugewiesener (International biometrische Industry Association) zugewiesener Besitzer Wert angegeben.<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**Winbio \_ Kein \_ \_ Formattyp \_ verfügbar**</dt> <dt>((UShort) 0)</dt> </dl>    | Es wurde kein Formattyp angegeben.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Eine [**winbio- \_ registrierte \_ Format**](winbio-registered-format.md) Struktur, die die Produkt-ID der Komponente angibt, die den Standarddaten Block im Bir generiert hat. Die Member des **winbio- \_ registrierten \_ Formats** können NULL sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der *SubType* -Parameter gibt den untergeordneten Faktor an, der den biometrischen Daten zugeordnet ist. Derzeit unterstützt die Windows-Biometrieframework (WBF) nur die Fingerabdruck Erfassung und verwendet die folgenden Konstanten, um untergeordnete Typinformationen darzustellen:

-   Winbio \_ ANSI \_ 381 Torys \_ \_ unbekannt
-   Winbio \_ ANSI \_ 381 \_ POS, \_ RH \_ Thumb
-   Winbio \_ ANSI \_ 381 POS-Zeige- \_ \_ \_ \_ Finger
-   Winbio \_ ANSI \_ 381 \_ Torpo- \_ \_ \_ Mittelfinger
-   Winbio \_ ANSI \_ 381 \_ POS, \_ RH- \_ Klingel \_ Finger
-   Winbio \_ ANSI \_ 381 Torys \_ \_ RH \_ Little \_ Finger
-   Winbio \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb
-   Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ Index \_ Finger
-   Winbio \_ ANSI \_ 381 \_ POS \_ - \_ Mittel \_ Fingerabdruck
-   Winbio \_ ANSI \_ 381 Torys LH- \_ \_ \_ Klingel \_ Finger
-   Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ wenig \_ Finger
-   Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern
-   Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern
-   Winbio \_ ANSI \_ 381 \_ POS \_ zwei \_ Daumen

> [!IMPORTANT]
>
> Versuchen Sie nicht, den Wert zu überprüfen, der für den *SubType* -Parameterwert angegeben wurde. Der Windows-Biometrie-Dienst überprüft den angegebenen Wert vor der Übergabe an Ihre Implementierung. Wenn der Wert " **winbio \_ SubType \_ No \_ Information** " oder " **winbio \_ SubType \_ any**" lautet, überprüfen Sie ggf. ggf.

 

Wenn eine der folgenden Bits bestätigt wird, ist die Struktur des **winbio.- \_ \_ Headers** nicht ordnungsgemäß formatiert.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**Subtypkonstanten von winbio- \_ Biometrie \_**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**winbio \_ Bir**](winbio-bir.md)
</dt> <dt>

[**Winbio \_ - \_ \_ datenflags-Konstanten**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**Winbio \_ Bir- \_ Feld Konstanten**](winbio-bir-field-constants.md)
</dt> <dt>

[**Winbio-und- \_ \_ Zweck-Konstanten**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**Winbio \_ Bir- \_ Qualitäts Konstanten**](winbio-bir-quality-constants.md)
</dt> <dt>

[**Winbio \_ - \_ Version Version-Konstanten**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





